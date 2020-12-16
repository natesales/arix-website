<script>
    import Table from "../components/Table.svelte";
</script>

<main>
    <div class="text-center p-10">
        <h1 class="text-6xl font-extrabold">
            The Amateur Radio
            <br />
            <span
                class="bg-clip-text text-transparent bg-gradient-to-l from-blue-500 to-blue-300 p-6">
                Internet Exchange
            </span>
        </h1>
        <p class="text-xl text-gray-600 max-w-2xl mx-auto pt-7">
            ARIX is an experimental internet exchange point for licensed amateur
            radio operators. ARIX is purely experimental for the use of
            networking research, development, and education.
        </p>
    </div>

    <p class="py-3 text-center text-gray-700 text-xl">ARIX Members</p>
    <Table />

    <div class="max-w-screen-xl mx-auto px-4 border-t border-white">
        <h1 class="text-3xl py-3 pt-7">Connectivity</h1>
        <p class="pb-2">
            Connections be obtained via 802.11 wireless or other particpating IP
            protocols. You're welcome to integrate something other than
            Ethernet, but the route servers are TCP/IP only and most peers are
            as well. Currently the supported interconnection methods are as
            follows:
        </p>

        <ul class="list-disc">
            <li>2.4GHz 802.11n - Portland, OR</li>
            <li>2.4GHz/5GHz 802.11n - Flagstaff, AZ</li>
            <li>1GigE/10GigE - Fremont, CA</li>
        </ul>

        <h1 class="text-3xl py-3 pt-7">Contact</h1>
        <p class="pb-2">
            The ARIX team can be contacted by email at noc@arix.dev or on #arix
            on freenode
        </p>

        <h1 class="text-3xl py-3 pt-7">Policy</h1>
        <p class="pb-2">
            If an ARIX member cause issues for the exchange, other members, or
            the internet at large, intentionally or unintentionally, the
            offending port may be brought down until the issue is corrected.
        </p>
        <ul class="list-disc">
            <li>
                Only IPv4, IPv6, ARP, and NDP Layer 2 protocols are permitted.
            </li>
            <li>Only one MAC address per port without prior authorization.</li>
        </ul>

        <h1 class="text-3xl py-3 pt-7">Route Servers</h1>
        <p class="pb-2">
            ARIX operates dual stack route servers to aid members in their
            peering endevours. See the members table above for peering
            information.
        </p>

        <h2 class="text-xl">IRR</h2>
        <p class="pb-5">
            All ARIX peering macros are contained in AS47192:AS-ARIX if you
            would like to IRR prefix-filter the route servers.
        </p>

        <h2 class="text-xl">RPKI</h2>
        <p class="pb-5">
            AMPRNet IP space is not currently RPKI signed, but in the hope that
            it will be in the future, ARIX route servers currently reject IPv4
            and IPv6 RPKI invalids.
        </p>

        <h2 class="text-xl">BGP Communities</h2>
        <p class="pb-5">
            RFC 8326 GRACEFUL_SHUTDOWN is supported. Routes tagged with
            community (65535:0) will have LOCAL_PREF set to 0. Additionally,
            routes tagged with communty (47192:0) will not be announced to any
            peer.
        </p>

        <h2 class="text-xl">Prefix Length</h2>
        <p class="pb-5">
            Networks must be a minimum size of IPv4 /24 and IPv6 /48. Any more
            specific prefixes will be rejected.
        </p>

        <h2 class="text-xl">Prefix Limits</h2>
        <p class="pb-5">
            The route servers have a max prefix import policy of 100 routes or
            less for both IPv4 and IPv6. If you run Amateur Radio services on
            more than 100 prefixes let us know.
        </p>

        <h2 class="text-xl">IPv4</h2>
        <p class="pb-5">
            Only routes within AMPRNet ranges (44.0.0.0/9 and 44.128.0.0/10) are
            accepted by the route servers. All other IPv4 networks are rejected.
            Additionally, any prefix overlapping the peering LAN
            (44.190.42.0/24) will be rejected.
        </p>
        <h2 class="text-xl">IPv6</h2>
        <p class="pb-5">
            Because there is no "offical" IPv6 network for amateur radio
            operators, most IPv6 networks in the range of 2000::/3 are accepted.
            The route servers block some IPv6 networks (::/8, 0100::/64,
            2001:2::/48, 2001:10::/28, 2001:db8::/32, 2002::/16, 3ffe::/16,
            fc00::/7, fe80::/10, fec0::/10, ff00::/8). (All more specific
            prefixes are rejected) Additionally, any prefix overlapping the
            peering LAN (2a0e:8f00:fddd::/64) will be rejected.
        </p>
    </div>
</main>
