# Lab 01 — VPN Connectivity

## Objective
Establish secure private connectivity between
two computers located in Ireland and Brazil.

## Environment
- BR-01: HP ProBook 4530s, Windows 10 Pro
- IE-01: Personal workstation
- VPN: Tailscale
- Protocol: WireGuard

## Implementation
- Installed Tailscale on both computers.
- Connected both devices to the same Tailnet.
- Identified their private IP addresses.
- Tested connectivity in both directions.

## Results
- [x] Brazil device connected
- [x] Ireland device connected
- [x] IP addresses identified
- [x] Connectivity tested
- [x] Bidirectional communication verified

## Lessons Learned
- Private IP addressing
- VPN connectivity
- Network latency
- Remote connectivity troubleshooting

## Evidence
Screenshots of connectivity tests.

## Network Diagnostics

### Ireland — IE-01

- UDP: Available
- IPv4: Available
- IPv6: Not available in current network
- Mapping varies by destination IP: True
- Captive portal: Not detected
- Nearest DERP: London
- DERP latency to London: approximately 76.6 ms

### Brazil — BR-01

- UDP: Available
- IPv4: Available
- IPv6: Available
- Mapping varies by destination IP: False
- Captive portal: Not detected
- Nearest DERP: São Paulo
- DERP latency to São Paulo: approximately 6.7 ms

### Connectivity

- Bidirectional Tailscale connectivity established.
- Initial connectivity was relayed through DERP.
- Direct connectivity was not established during the initial test.

### Troubleshooting Notes

The Ireland workstation is connected through a mobile hotspot. The network characteristics may make direct peer connectivity more difficult.

The Brazil Windows host reported a Tailscale DNS configuration permission warning. This issue is pending investigation.

### Lessons Learned

- UDP availability does not guarantee direct peer connectivity.
- NAT characteristics can affect peer-to-peer connectivity.
- DERP provides an encrypted relay fallback.
- Network latency varies depending on the route and relay location.
- Connectivity and DNS configuration are separate troubleshooting areas.
