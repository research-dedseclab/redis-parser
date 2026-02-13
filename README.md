# redis-parser
The Redis Forensic Parser extracts forensic artifacts from Redis environments. It supports both standalone and distributed setups (master/replica) and works with multiple evidence sources:  RDB snapshots (dump.rdb) AOF files (appendonly.aof) redis-server.log MONITOR streams ACL LOG (authentication and access violations)  Memory snapshots 
 Requirements
Python 3.8 or higher
Redis 6.x or 7.x test environment
Optional tools for memory dumps:
gcore (Linux)
procdump (Windows)
Python dependencies
pip install pyyaml
