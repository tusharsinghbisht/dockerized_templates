.PHONY: dev-config dev-up dev-down config-prod prod-up prod-down prod-build prod-logs clean

dev-config:
	docker-compose -f docker-compose.dev.yml config

dev-up:
	docker-compose -f docker-compose.dev.yml up 

dev-down:
	docker-compose -f docker-compose.dev.yml down

config-prod:
	docker-compose -f docker-compose.prod.yml config

prod-up:
	docker-compose -f docker-compose.prod.yml up -d

prod-down:
	docker-compose -f docker-compose.prod.yml down

prod-build:
	docker-compose -f docker-compose.prod.yml build

prod-logs:
	docker-compose -f docker-compose.prod.yml logs -f

clean:
	docker system prune -f