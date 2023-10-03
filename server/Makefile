postgresinit:
	docker run --name postgres15 -p 5432:5432 -e POSTGRES_USER=root -e POSTGRES_PASSWORD=root -d postgres:15-alpine

postgres:
	docker exec -it postgres15 psql

createdb:
	docker exec -it postgres15 createdb --username=root --owner=root go-chat-app

dropdb:
	docker exec -it postgres15 dropdb go-chat-app

.PHONY: postgresinit postgres createdb dropdb