TEST_HOST   ?= 127.0.0.1
TEST_PORT   ?= 3306

DB_USERNAME ?= upperio_tests
DB_PASSWORD ?= upperio_secret
DB_NAME     ?= upperio_tests

all: setup reset-db

setup:
	mysql -uroot -h"$(TEST_HOST)" -P$(TEST_PORT) < setup.sql

reset-db:
	mysql -u"$(DB_USERNAME)" -p"$(DB_PASSWORD)" -h"$(TEST_HOST)" -P$(TEST_PORT) "$(DB_NAME)" < structs.sql
