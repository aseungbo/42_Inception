NAME	= inception

DB_PATH		:= ./data
HOST_LINK	:=

# DB_PATH		:= /home/seuan/data
# HOST_LINK	:= "127.0.0.1	seuan.42.fr" > /etc/hosts

all		:	$(NAME)

$(NAME)	:
	@echo "Inception setup start"
	mkdir -p $(DB_PATH)/mariadb/
	mkdir -p $(DB_PATH)/wordpress/
	@sudo echo $(HOST_LINK)
	docker-compose -f ./srcs/docker-compose.yaml up --build -d

# docker-compose down and remove volumes
clean	: 
	docker-compose -f ./srcs/docker-compose.yaml down --rmi "all" --volumes

## 마운트에 사용된 local volume 삭제.
fclean	: clean 
	rm -rf $(DB_PATH)/mariadb/.setup
	rm -rf $(DB_PATH)/mariadb/*
	rm -rf $(DB_PATH)/wordpress/.setup
	rm -rf $(DB_PATH)/wordpress/*

re	: fclean all

.PHONY	: all clean fclean re
