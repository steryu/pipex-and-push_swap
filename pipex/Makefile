SRCS		= pipex.c pipex_utils.c

OBJS		= $(SRCS:.c=.o)

CC			= gcc
CFLAGS		= -Wall -Werror -Wextra

NAME		= pipex
LIBFT 		= ./libft/libft.a

all:		$(NAME)

$(LIBFT):
	$(MAKE) -C ./libft

$(NAME): 	$(OBJS) $(LIBFT)
	$(CC) $(CFLAGS) $(OBJS) $(LIBFT) -o $(NAME)
	@echo "\033[0;32mDone!"

clean: 
	rm -f $(OBJS) $(LIBFT)
	$(MAKE) -C libft/ clean

fclean: 	clean 
	rm -f $(NAME)
	$(MAKE) -C libft/ fclean

re:			fclean all

.PHONY: 	all clean fclean re
