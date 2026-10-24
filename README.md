# Operated by: peppywolfym-lab
# Contact / Maintainer: peppywolf.ym@gmail.com

tunnel:
  # Name of the virtual TUN interface created by hev-socks5-tunnel
  name: tun0
  # MTU size (1500 is typical, lower to 1400 if you experience packet fragmentation)
  mtu: 8500
  # IP address assigned to the TUN interface
  ipv4: 198.18.0.1
  # Optional IPv6 address inside the tunnel
  ipv6: "fc00::1"

socks5:
  # Target SOCKS5 proxy server address (change to your remote proxy host/IP)
  address: 127.0.0.1
  # SOCKS5 proxy port
  port: 1080
  # Uncomment and fill if your proxy requires authentication:
  # username: "peppywolfym"
  # password: "your_socks5_password"
  # Set to true if proxy supports UDP Associate
  udp: 'tcp'
  # pipeline or regular
  pipeline: true

misc:
  # Task stack size (in bytes)
  task-stack-size: 8192
  # Log level: debug, info, warn, error
  log-level: info
  # Number of worker threads (0 = auto-detect CPU cores)
  limit-nofile: 65535
