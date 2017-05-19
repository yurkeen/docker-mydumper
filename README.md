## MYDUMPER
Alpine Linux based mydumper Docker image to quickly backup and restore mysql databases.

## Usage

```$ docker exec -it mydumper-container mydumper --help

  mydumper [OPTION*] multi-threaded MySQL dumping

Help Options:
  -?, --help                  Show help options

Application Options:
  -B, --database              Database to dump
  -T, --tables-list           Comma delimited table list to dump (does not exclude regex option)
  -o, --outputdir             Directory to output files to
  -s, --statement-size        Attempted size of INSERT statement in bytes, default 1000000
  -r, --rows                  Try to split tables into chunks of this many rows. This option turns off --chunk-filesize
  -F, --chunk-filesize        Split tables into chunks of this output file size. This value is in MB
  -c, --compress              Compress output files
  -e, --build-empty-files     Build dump files even if no data available from table
  -x, --regex                 Regular expression for 'db.table' matching
  -i, --ignore-engines        Comma delimited list of storage engines to ignore
  -m, --no-schemas            Do not dump table schemas with the data
  -d, --no-data               Do not dump table data
  -G, --triggers              Dump triggers
  -E, --events                Dump events
  -R, --routines              Dump stored procedures and functions
  -W, --no-views              Do not dump VIEWs
  -k, --no-locks              Do not execute the temporary shared read lock.  WARNING: This will cause inconsistent backups
  --no-backup-locks           Do not use Percona backup locks
  --less-locking              Minimize locking time on InnoDB tables.
  -l, --long-query-guard      Set long query timer in seconds, default 60
  -K, --kill-long-queries     Kill long running queries (instead of aborting)
  -D, --daemon                Enable daemon mode
  -I, --snapshot-interval     Interval between each dump snapshot (in minutes), requires --daemon, default 60
  -L, --logfile               Log file name to use, by default stdout is used
  --tz-utc                    SET TIME_ZONE='+00:00' at top of dump to allow dumping of TIMESTAMP data when a server has data in different time zones or data is being moved between servers with different time zones, defaults to on use --skip-tz-utc to disable.
  --skip-tz-utc
  --use-savepoints            Use savepoints to reduce metadata locking issues, needs SUPER privilege
  --success-on-1146           Not increment error count and Warning instead of Critical in case of table doesn't exist
  --lock-all-tables           Use LOCK TABLE for all, instead of FTWRL
  -U, --updated-since         Use Update_time to dump only tables updated in the last U days
  --trx-consistency-only      Transactional consistency only
  --complete-insert           Use complete INSERT statements that include column names
  -h, --host                  The host to connect to
  -u, --user                  Username with the necessary privileges
  -p, --password              User password
  -P, --port                  TCP/IP port to connect to
  -S, --socket                UNIX domain socket file to use for connection
  -t, --threads               Number of threads to use, default 4
  -C, --compress-protocol     Use compression on the MySQL connection
  -V, --version               Show the program version and exit
  -v, --verbose               Verbosity of output, 0 = silent, 1 = errors, 2 = warnings, 3 = info, default 2
  --defaults-file             Use a specific defaults file
```
