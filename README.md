These variables should be set:


Host vars:

[pgsql-cluster]

192.168.152.122 hostname=irontrade-pgsql-01


Example group vars:

[pgsql-cluster:vars]

archive_command: "/bin/true"

pgsql_base_config: templates/postgresql.base.conf

pgsql_version: "9.6"

pgsql_archive_command: ""

patroni_scope: "patroni-cluster-name"

patroni_rest_password: "rest-password"

patroni_postgres_password: "superadmin-password"

patroni_replicator_password: "replicator-password"

patroni_interface: "br-lan"

consul_addr: "localhost:8500"


pgbouncer_config: pgbouncer


keepalived_vip: "10.0.0.1"

keepalived_interface: "eth0"

keepalived_routerid: 100



haproxy_base_config: templates/haproxy.cfg.j2

pgbouncer_enabled: false


prometheus_node: yes

prometheus_pgsql: yes

