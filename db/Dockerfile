# MySQL pre-loaded with HeavenMS's schema + item/drop/shop data, so the
# container is ready to serve on first boot -- no init Job needed in k8s.
# Matches the sql/ order from upstream's own docker-compose.yml (mysql runs
# /docker-entrypoint-initdb.d/*.sql alphabetically on an empty data dir, which
# already sorts db_database.sql -> db_drops.sql -> db_shopupdate.sql).
FROM mysql:5.6
COPY sql/db_database.sql sql/db_drops.sql sql/db_shopupdate.sql /docker-entrypoint-initdb.d/
