# Countermeasures

This document describes the security hardening steps taken, particularly the implementation of WPA3-SAE.

## WPA2 Baseline Observation

The initial test environment utilized WPA2-Personal, which lacked built-in protection for management frames.

**WPA2 Router Baseline:**
![WPA2 Router Baseline](../evidence/07-wpa3-hardening/05-wpa2-router-baseline.png)

## Implementing WPA3-SAE

To address the observed disruption, the router's wireless security configuration was migrated to WPA3-SAE (Simultaneous Authentication of Equals). 

**WPA3-SAE Router Configuration:**
![WPA3 SAE Hardening](../evidence/07-wpa3-hardening/12-wpa3-sae-hardening.png)

Protected Management Frames (PMF / IEEE 802.11w) are directly relevant to deauthentication/disassociation resilience. However, the available portfolio evidence does not independently establish the precise PMF configuration used during this assessment (e.g., whether it was set to Optional or Required), though it is generally mandated by the WPA3 standard.

**WPA3 Client Reconnection Validation:**
The client successfully connected using the new configuration.
![WPA3 Client Validation](../evidence/07-wpa3-hardening/13-wpa3-client-validation.png)

## Retesting and Validation

Following the configuration change, the controlled deauthentication test was repeated.

**Controlled WPA3 Retest:**
![WPA3 Deauth Retest](../evidence/08-retest/14-wpa3-deauth-retest.png)

**Post-Hardening Result:**
During this specific retest, the client maintained connectivity without observable disruption.
![Post-Hardening Result](../evidence/08-retest/15-post-hardening-result.png)
