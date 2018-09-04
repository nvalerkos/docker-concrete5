# Concrete5 Installed with LAMP.
> Based on https://hub.docker.com/r/mattrayner/lamp/


## To Build image:

	docker build . -t concrete5

## Automatically adding source code
> First install include the INIT_CONCRETE5=true as ENV to extract the concrete5 source code to /app/

	docker run -p "80:80" -e INIT_CONCRETE5=true -v ${PWD}/app:/app -v ${PWD}/mysql:/var/lib/mysql --name project_name_goes_here  nvalerkos/concrete5

## Otherwise:
	
	docker run -p "80:80" -v ${PWD}/app:/app -v ${PWD}/mysql:/var/lib/mysql   --name project_name_goes_here nvalerkos/concrete5

## Stop it:

	docker stop project_name_goes_here

## If you want to just start it after exited:

	docker start project_name_goes_here
