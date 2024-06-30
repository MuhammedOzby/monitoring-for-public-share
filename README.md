# Notlar

> Cloudflare ile tünel yapılmaktadır bunun yerine kendinizde bir proxy kullanabilirsiniz.
> Örnek olarak sadece yerel ağ üzerinde kullanacaksanı Swag&duckdns ile kullanılabilir. Nginx proxy başka bir alternatif olarak kullanılabilir.

Kullanmak için direk çalıştırabilirsiniz. Varsayılan ayarlar kullanılmıştır. [Şifre alanlarını kullanmadan önce güncelleyin](README.md#L12)

- Mikrotik IP adresi: [prometheus.yml#40](./prometheus/prometheus.yml#L40)
- Kendinize özel bir snmp auth eklemeniz gerekirse şuraya bakın: https://github.com/brunsgaard/snmp-exporter/tree/master?tab=readme-ov-file#authentication
  - Buraya ekleyebilirsiniz: [snmp.yml#auths](./snmp-exporter/snmp.yml#L8)
  - Örnek olarak standart (community:public, version:2): [snmp.yml#auths](./snmp-exporter/snmp.yml#L3)
- Grafana ayarlar (Şifrenizi değiştirin.): [.grafana](./environments/.grafana)

## Notlar

Docker üzerinde portlar dışarıya açık değildir. Reverse proxy kullanılması tavsiye edilir. Nginx Proxy manager, swag vd. gibi.

Dashboardlar için şu adreslere bakabilirsiniz:

- Node Exporter: https://github.com/rfmoz/grafana-dashboards
- Cadvisor: https://grafana.com/grafana/dashboards/19792-cadvisor-dashboard/
- Mikrotik: https://grafana.com/grafana/dashboards/14420-mikrotik-monitoring/
