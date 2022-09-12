This let's you create a docker image and update an ECS task and update the running service with the updated task.

This assumes you have run the code in headversity_devops_infra at least once to have the foundation layed down.

Assuming you didn't change the task/service/cluster names in the headversity_devops_infra code, the only thing that would require changing would be the file "ecs-task-def.json".

The content of this file can be taken directly from the task defintion created in the web console's ecs section. (There is a json output of the definition that can be copied)

Once this file is set correctly all you would need to do is run the github action and the docker image will get updated and pushed to ecr and the ecs task will get updated and the service restarted with the updated task.