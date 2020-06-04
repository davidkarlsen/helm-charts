barman
======
Chart for Barman PostgreSQL Backup and Recovery Manager

Current chart version is `0.0.2`

Source code can be found [here](http://www.pgbarman.org/)



## Chart Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| barman.backupDir | string | `"/var/lib/barman"` | Barman home directory |
| barman.backupMethod | string | `"postgres"` | Barman backup method |
| barman.backupOptions | string | `"concurrent_backup"` | Barman backup options |
| barman.backupSchedule | string | `"0 4 * * *"` | Barman backup schedule |
| barman.backups[0].backupMethod | string | `"postgres"` | Barman backup method |
| barman.backups[0].databaseSlotName | string | `"barman"` | Database slot name to be created/used |
| barman.backups[0].lastBackupMaximumAge | string | `"1 day"` | Barman last backup maximum age |
| barman.backups[0].postgresql.host | string | `"postgresql"` | Postgresql host |
| barman.backups[0].postgresql.port | int | `5432` | Postgresql port |
| barman.backups[0].postgresql.replicationPassword | string | `"barman"` | Postgresql replication password |
| barman.backups[0].postgresql.replicationUser | string | `"barman"` | Postgresql replication user |
| barman.backups[0].postgresql.superUser | string | `"postgres"` | Postgresql super user |
| barman.backups[0].postgresql.superUserDatabase | string | `"postgres"` | Postgresql super user database |
| barman.backups[0].postgresql.superUserPassword | string | `"postgres"` | Postgresql super user password |
| barman.backups[0].retentionPolicy | string | `"RECOVERY WINDOW of 1 MONTH"` | Barman retention policy |
| barman.barmanUser | string | `"barman"` | Barman user |
| barman.compression | string | `"gzip"` | Barman backup compression |
| barman.databaseSlotName | string | `"barman"` | Database slot name to be created/used |
| barman.lastBackupMaximumAge | string | `"1 day"` | Barman last backup maximum age |
| barman.retentionPolicy | string | `"RECOVERY WINDOW of 1 MONTH"` | Barman retention policy |
| image.pullPolicy | string | `"Always"` | Image pull policy |
| image.repository | string | `"ubcctlt/barman"` | Image repository |
| image.tag | string | `"latest"` | Image tag |
| persistence.data.accessMode | string | `"ReadWriteOnce"` | Access mode for persistent storage |
| persistence.data.enabled | bool | `true` | Enable persistent storage for backup data |
| persistence.data.size | string | `"20Gi"` | Size of storage volume |
| persistence.data.storageClass | string | `""` | Storage class |
| persistence.recover.accessMode | string | `"ReadWriteOnce"` | Access mode for persistent storage |
| persistence.recover.enabled | bool | `false` | Enable persistent storage for recovery |
| persistence.recover.size | string | `"4Gi"` | Size of storage volume |
| persistence.recover.storageClass | string | `""` | Storage class |
| resources | object | `{}` | Resource limits and requests |