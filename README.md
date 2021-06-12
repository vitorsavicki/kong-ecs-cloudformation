# kong-ecscloudformation

order to install:
1 - database-security-group.yml
2 - kong-ecs-security-groups.yml
3 - kong-elb-security-groups copy.yml
4 - ecs-profiles.yml
5 - kong.database.stack.yml
6 - kong.stack.yml

In first install run database migration:
# Kong
aws ecs run-task --cluster Kong --task-definition kongmigration-dev --count 1

# Konga
aws ecs run-task --cluster Kong --task-definition kongamigration-dev --count 1