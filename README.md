Redis Forensic Parser is a Python-based forensic analysis tool designed to extract and correlate artifacts from Redis environments.
It supports both standalone and distributed (master/replica) setups and works with multiple Redis evidence sources commonly encountered during incident response and digital forensics investigations.

✨ Features

Supports Redis 6.x and 7.x

Works with standalone and distributed (replication) environments

Extracts and correlates forensic artifacts from multiple sources

Designed for incident response, threat hunting, and post-compromise analysis

📂 Supported Evidence Sources

The parser can analyze the following Redis artifacts:

RDB snapshots (dump.rdb)

AOF files (appendonly.aof)

Redis server logs (redis-server.log)

MONITOR command streams

ACL LOG

Authentication failures

Authorization violations

Memory snapshots

Live process memory dumps

🧰 Requirements
System Requirements

Python 3.8 or higher

Redis 6.x or 7.x (for testing and validation)

Optional Tools (for Memory Acquisition)

Depending on the operating system, the following tools may be used to acquire Redis memory dumps:

Linux

gcore

Windows

procdump

📦 Installation
Clone the Repository
git clone https://github.com/<your-username>/redis-parser.git
cd redis-parser

Install Python Dependencies
pip install pyyaml


Additional dependencies may be added in future releases. A requirements.txt file is recommended for production use.

🚀 Usage

Usage examples will vary depending on the evidence source being analyzed.

General execution pattern:

python redis_parser.py --input <path_to_artifact> --type <artifact_type>


Example:

python redis_parser.py --input dump.rdb --type rdb


Supported artifact types include:

rdb

aof

log

monitor

acl

memory

🧪 Testing Environment

The tool has been tested against:

Redis 6.x

Redis 7.x

Standalone Redis instances

Master/Replica configurations

🔍 Use Cases

Redis compromise investigations

Detection of unauthorized access or persistence

Timeline reconstruction of Redis activity

Analysis of credential abuse and ACL violations

Memory forensics on live Redis instances
