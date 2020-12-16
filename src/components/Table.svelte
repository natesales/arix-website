<script>
    const peers = [
        {
            asn: 44977,
            callsign: "K7ARX",
            name: "ARIX",
            port: 10,
            ipv4: "44.190.42.2",
            ipv6: "2a0e:8f00:fddd::2"
        },
        {
            asn: 34553,
            callsign: "KJ7DMC",
            name: "Nathan Sales",
            port: 10,
            ipv4: "44.190.42.3",
            ipv6: "2a0e:8f00:fddd::3"
        },
        {
            asn: 6556,
            callsign: "KC7GDY",
            name: "Airgapped",
            port: 10,
            ipv4: "44.190.42.4",
            ipv6: "2a0e:8f00:fddd::4"
        },
        {
            asn: 49134,
            callsign: "VE7ALB",
            name: "10VPN Research Network",
            port: 1,
            ipv4: "44.190.42.5",
            ipv6: "2a0e:8f00:fddd::5"
        },
        {
            asn: 60564,
            callsign: "KC7GDY",
            name: "AZSignShop",
            port: 10,
            ipv4: "44.190.42.6",
            ipv6: "2a0e:8f00:fddd::6"
        },
        {
            asn: 112,
            callsign: "K7ARX",
            name: "AS112",
            port: 10,
            ipv4: "44.190.42.252",
            ipv6: "2a0e:8f00:fddd::252"
        },
        {
            asn: 47192,
            callsign: "K7ARX",
            name: "ARIX Route Servers",
            port: 10,
            ipv4: "44.190.42.253",
            ipv6: "2a0e:8f00:fddd::253"
        },
        {
            asn: 47192,
            callsign: "K7ARX",
            name: "ARIX Route Servers",
            port: 10,
            ipv4: "44.190.42.254",
            ipv6: "2a0e:8f00:fddd::254"
        }
    ];
</script>

<main class="pb-7">
    <div class="align-middle justify-center flex">
        <div class="border border-gray-300 rounded-md">
            <table class="divide-y divide-gray-200 ">
                <thead>
                    <tr>
                        <th class="px-6 py-3 text-left text-s leading-4 font-medium text-gray-600">Network</th>
                        <th class="px-6 py-3 text-left text-s leading-4 font-medium text-gray-600">Trustee Callsign</th>
                        <th class="px-6 py-3 text-left text-s leading-4 font-medium text-gray-600">ASN</th>
                        <th class="px-6 py-3 text-left text-s leading-4 font-medium text-gray-600">Port</th>
                        <th class="px-6 py-3 text-left text-s leading-4 font-medium text-gray-600">IPv4 Address</th>
                        <th class="px-6 py-3 text-left text-s leading-4 font-medium text-gray-600">IPv6 Address</th>
                    </tr>
                </thead>
                <tbody class="bg-white divide-y divide-gray-200">
                    {#each peers as peer}
                    <tr>
                        <td class="px-6 py-4 whitespace-no-wrap leading-5 text-gray-600">{peer.name}</td>
                        <td class="px-6 py-4 whitespace-no-wrap leading-5 text-gray-600">{peer.callsign}</td>
                        <td class="px-6 py-4 whitespace-no-wrap leading-5 text-gray-600">{peer.asn}</td>
                        <td class="px-6 py-4 whitespace-no-wrap leading-5 text-gray-600">{peer.port}G</td>
                        <td class="px-6 py-4 whitespace-no-wrap leading-5 text-gray-600">{peer.ipv4}</td>
                        <td class="px-6 py-4 whitespace-no-wrap leading-5 text-gray-600">{peer.ipv6}</td>
                    </tr>
                    {/each}
                </tbody>
            </table>
        </div>
    </div>
</main>
