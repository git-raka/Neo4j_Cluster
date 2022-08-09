# Cluster-Neo4j

dbms.mode=CORE
causal_clustering.discovery_type=LIST
causal_clustering.minimum_core_cluster_size_at_formation=3
causal_clustering.minimum_core_cluster_size_at_runtime=2
causal_clustering.initial_discovery_members=192.168.1.147:5000, 192.168.1.140:5000, 192.168.1.142:5000
causal_clustering.discovery_advertised_address=192.168.1.147:5000
causal_clustering.transaction_advertised_address=192.168.1.147:6000
causal_clustering.raft_advertised_address=192.168.1.147:7000
dbms.security.procedures.unrestricted=apoc.*,gds.*,bloom.*
dbms.security.procedures.allowlist=apoc.*,gds.*,bloom.*
apoc.import.file.enabled=true
apoc.import.file.use_neo4j_config=true
dbms.default_listen_address=0.0.0.0
dbms.default_advertised_address=192.168.1.147

# READ-REPLICA

dbms.mode=READ_REPLICA
causal_clustering.initial_discovery_members=192.169.1.248:5000,192.169.1.177:5000,192.169.1.107:5000
causal_clustering.discovery_advertised_address=192.169.1.192:5000
causal_clustering.transaction_advertised_address=192.169.1.192:6000
causal_clustering.raft_advertised_address=192.169.1.192:7000
