# Test Plan

This document outlines the testing stages, tools utilized, and the established baselines before executing the controlled deauthentication test.

## Security Baseline Configuration

The initial configuration of the authorized home network was established as a WPA2-Personal (CCMP/PSK) baseline, representing a standard residential wireless security posture prior to testing.

**Router WPA2 Configuration:**
![WPA2 Router Baseline](../evidence/07-wpa3-hardening/05-wpa2-router-baseline.png)

**Client WPA2 Association:**
The target client device was verified to be connected using this configuration.
![WPA2 Client Baseline](../evidence/04-client-identification/04-wpa2-client-baseline.png)

## Connectivity Baseline

Before initiating any testing, normal connectivity between the target client and the local gateway was verified to establish a behavioral baseline.

**Baseline Connectivity (Pre-Test):**
![Baseline Connectivity](../evidence/06-connectivity-impact/08-baseline-connectivity.png)

## Execution of Controlled Test

With the environment established and baseline connectivity verified, the test plan involves executing a controlled deauthentication test using the `aireplay-ng` tool against the authorized client device to observe the impact on its connection.

**Executing the Attack:**
![Controlled Deauthentication Test](../evidence/05-deauthentication-test/09-controlled-deauth-test.png)
