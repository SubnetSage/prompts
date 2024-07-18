Certainly! Here are several example prompts that can guide an AI to perform different analyses on a Cisco router configuration. These prompts can be used to examine various aspects of the configuration for security, performance, and compliance.

### Security Analysis
1. **Identify Security Issues:**
   ```
   Analyze the following Cisco router configuration for potential security vulnerabilities. Provide suggestions for improving security:
   ```
2. **Check for Strong Passwords:**
   ```
   Review the Cisco router configuration and verify if strong passwords are used. Highlight any weak passwords and recommend stronger alternatives:
   ```
3. **Evaluate Access Control:**
   ```
   Examine the access control settings in this Cisco router configuration. Ensure that only authorized users have access and suggest any necessary changes:
   ```

### Performance Analysis
1. **Optimize Interface Configuration:**
   ```
   Analyze the interface configuration of this Cisco router for performance optimization. Provide recommendations for improving interface performance:
   ```
2. **Review Routing Configuration:**
   ```
   Evaluate the routing configuration in this Cisco router. Identify any suboptimal routes and suggest improvements:
   ```
3. **Check Resource Utilization:**
   ```
   Analyze the resource utilization settings (CPU, memory, etc.) in this Cisco router configuration. Provide suggestions for optimizing resource usage:
   ```

### Compliance Analysis
1. **Verify Compliance with Best Practices:**
   ```
   Review the Cisco router configuration for compliance with industry best practices. Highlight any deviations and recommend corrections:
   ```
2. **Check for Regulatory Compliance:**
   ```
   Analyze the Cisco router configuration for compliance with regulatory requirements (e.g., PCI-DSS, HIPAA). Identify any non-compliant settings and suggest modifications:
   ```
3. **Assess Security Policies:**
   ```
   Examine the security policies in this Cisco router configuration for compliance with corporate security standards. Recommend changes to align with these standards:
   ```

### Configuration Analysis
1. **Identify Configuration Errors:**
   ```
   Review the following Cisco router configuration for errors or misconfigurations. Highlight any issues and provide recommendations for correction:
   ```
2. **Evaluate AAA Configuration:**
   ```
   Analyze the AAA (Authentication, Authorization, Accounting) configuration in this Cisco router. Ensure it is properly set up and secure:
   ```
3. **Check for Redundant Configurations:**
   ```
   Examine the Cisco router configuration for redundant or unnecessary settings. Suggest any configurations that can be removed or consolidated:
   ```

### Example Configuration for Analysis:
```
aaa new-model
!
radius-server host 1.0.0.9 auth-port 1812 acct-port 1813 key radiuskey2024
radius-server timeout 10
!
aaa authentication login default group radius local
aaa authentication enable default group radius enable
aaa authorization exec default group radius local
aaa accounting exec default start-stop group radius
!
line con 0
 exec-timeout 0 0
 privilege level 15
 logging synchronous
 login authentication default
line aux 0
 exec-timeout 0 0
 privilege level 15
 logging synchronous
 login authentication default
line vty 0 4
 login authentication default
 transport input ssh
line vty 5 15
 login authentication default
 transport input ssh
!
ip domain-name example.com
crypto key generate rsa modulus 2048
ip ssh version 2
!
end
```
