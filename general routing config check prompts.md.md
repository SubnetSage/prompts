### General Routing Protocol Configuration
1. **Verify OSPF Configuration:**
   ```
   Analyze the following Cisco router configuration and check if OSPF is properly configured. Identify any issues with OSPF area assignments, network statements, or authentication settings:
   ```
2. **Review EIGRP Configuration:**
   ```
   Examine the EIGRP configuration in the following Cisco router setup. Ensure that the EIGRP process is properly configured with correct AS numbers, network statements, and authentication settings:
   ```
3. **Check BGP Configuration:**
   ```
   Review the BGP configuration in this Cisco router. Verify that BGP neighbors, AS numbers, network statements, and route policies are correctly configured:
   ```
4. **Evaluate RIP Configuration:**
   ```
   Analyze the RIP configuration in this Cisco router. Ensure that RIP version, network statements, and timers are properly configured:
   ```

### Specific Configuration Checks
1. **OSPF Area Assignment:**
   ```
   Verify that all interfaces in the following Cisco router configuration are correctly assigned to the appropriate OSPF areas:
   ```
2. **EIGRP Network Statements:**
   ```
   Check if the network statements in the EIGRP configuration of this Cisco router correctly include all necessary interfaces and subnets:
   ```
3. **BGP Neighbor Relationships:**
   ```
   Review the BGP neighbor relationships in the following Cisco router configuration. Ensure that all neighbors are correctly defined and reachable:
   ```

### Advanced Configuration Checks
1. **OSPF Route Summarization:**
   ```
   Analyze the OSPF route summarization settings in this Cisco router configuration. Ensure that summarization is properly configured to reduce routing table size:
   ```
2. **EIGRP Authentication:**
   ```
   Check if EIGRP authentication is correctly configured in the following Cisco router setup. Ensure that all interfaces use the correct authentication key-chains:
   ```
3. **BGP Route Filtering:**
   ```
   Review the BGP route filtering policies in this Cisco router configuration. Verify that route maps, prefix lists, and access lists are correctly applied to control BGP advertisements:
   ```

### Example Configuration for Analysis:
```
hostname Router
!
router ospf 1
 log-adjacency-changes
 network 10.0.0.0 0.0.0.255 area 0
 network 192.168.1.0 0.0.0.255 area 1
!
router eigrp 100
 network 10.0.0.0
 network 172.16.0.0
!
router bgp 65001
 bgp log-neighbor-changes
 neighbor 192.168.1.1 remote-as 65002
 neighbor 192.168.1.2 remote-as 65003
!
interface Loopback0
 ip address 10.0.0.1 255.255.255.255
!
interface FastEthernet0/0
 ip address 192.168.1.1 255.255.255.0
 duplex auto
 speed auto
!
end
```
