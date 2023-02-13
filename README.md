# NodeMonitor

Prometheus 監視

## Installing

```bash
git clone git@github.com:Grawlily/NodeMonitor.git
```

```bash
cd NodeMonitor
chmod +x setup-monitor.sh
./setup-monitor.sh
```

## Port Open

- Using ufw command

```bash
ufw allow 9100
```

- Using iptables with OCI

```
sudo vim /etc/iptables/rules.v4

# Add
-A INPUT -p tcp -m state --state NEW -m tcp --dport 9100 -j ACCEPT
```

```bash
sudo /sbin/iptables-restore < /etc/iptables/rules.v4
```
