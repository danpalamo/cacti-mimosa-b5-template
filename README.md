***Tested with firmware 1.5.1, all working fine. However, Mimosa is not supporting 64-bit traffic counters, so currently not advising bothering with monitoring traffic OID's.

***Tested with b11, all working fine.

***Tested with b24, all working fine.

# cacti-mimosa-b5-template
A basic cacti host template for Mimosa B5 backhaul radio equipment.
Compatible and tested with b5/b5c firmware 1.4.6.
Please note that firmware 1.4.4 is not fully compatible.
Lastly, devices added with previous versions of the template will need to be removed and re-added with the new template, losing historical data. There is a manual workaround, but it is an absurd amount of work.

***Somewhere along the line to firmware 1.4.6, mimosaRxPower and mimosaSNR behavior changed and breaks the current cacti template. Once the expected behavior is confirmed by Mimosa, I will update the template for future versions.

~~Devices will need to select 'create graphs for this host', see image.

![create-new-graphs](https://github.com/danpalamo/cacti-mimosa-b5-template/blob/master/cacti-mimosa-b5-template-create-new-graphs.png)

## expected import output:

#### CDEF
- [success] Divide by 100 [update]
- [success] Divide by 10 [new]
- [success] Total All Data Sources [update]
- [success] Multiply by 0.4 [update]
- [success] Total All Data Sources, Multiply by 0.4 [update]
- [success] Turn Bytes into Bits [update]

#### GPRINT Preset
- [success] Normal [update]
- [success] Exact Numbers [update]

#### Data Input Method
- [success] Get SNMP Data [update]
- [success] Get SNMP Data (Indexed) [update]

#### Data Template
- [success] Mimosa B5 - RX SNR Chain 1 [new]
- [success] Mimosa B5 - RX SNR Chain 2 [new]
- [success] Mimosa B5 - RX SNR Chain 3 [new]
- [success] Mimosa B5 - RX SNR Chain 4 [new]
- [success] Mimosa B5 - RX Packet Error Rate [new]
- [success] Mimosa B5 - TX Packet Error Rate [new]
- [success] Mimosa B5 - RX-1 PHY Rate [new]
- [success] Mimosa B5 - RX-2 PHY Rate [new]
- [success] Mimosa B5 - RX-3 PHY Rate [new]
- [success] Mimosa B5 - RX-4 PHY Rate [new]
- [success] Mimosa B5 - TX-1 PHY Rate [new]
- [success] Mimosa B5 - TX-2 PHY Rate [new]
- [success] Mimosa B5 - TX-3 PHY Rate [new]
- [success] Mimosa B5 - TX-4 PHY Rate [new]
- [success] Mimosa B5 - RX RSSI Chain 1 [new]
- [success] Mimosa B5 - RX RSSI Chain 2 [new]
- [success] Mimosa B5 - RX RSSI Chain 3 [new]
- [success] Mimosa B5 - RX RSSI Chain 4 [new]
- [success] Mimosa B5 - Satellites - GPS [new]
- [success] Mimosa B5 - Satellites - GLONASS [new]
- [success] Mimosa B5 - RX EVM Chain 1 [new]
- [success] Mimosa B5 - RX EVM Chain 2 [new]
- [success] Mimosa B5 - RX EVM Chain 3 [new]
- [success] Mimosa B5 - RX EVM Chain 4 [new]
- [success] Interface - Traffic [update]
- [success] Interface - Errors/Discards [update]
- [success] Interface - Unicast Packets [update]
- [success] Interface - Non-Unicast Packets [update]

#### Graph Template
- [success] Mimosa - B5 RX SNR Values [new]
- [success] Mimosa - B5 Error Rate Packet [new]
- [success] Mimosa - B5 PHY RX Rates [new]
- [success] Mimosa - B5 PHY TX Rates [new]
- [success] Mimosa - B5 RX RSSI [new]
- [success] Mimosa - B5 Satellites [new]
- [success] Mimosa - B5 EVM RX [new]
- [success] Mimosa - B5 MAC RX Rates [new]
- [success] Mimosa - B5 MAC TX Rates [new]
- [success] Interface - Traffic (bits/sec) [update]
- [success] Interface - Errors/Discards [update]
- [success] Interface - Unicast Packets [update]
- [success] Interface - Non-Unicast Packets [update]
- [success] Interface - Traffic (bytes/sec) [update]
- [success] Interface - Traffic (bits/sec, 95th Percentile) [update]
- [success] Interface - Traffic (bits/sec, Total Bandwidth) [update]
- [success] Interface - Traffic (bytes/sec, Total Bandwidth) [update]

#### Data Query
- [success] SNMP - Interface Statistics [update]

#### Host Template
- [success] Mimosa B5 [new]
