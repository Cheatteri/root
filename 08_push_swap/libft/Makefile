# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: jhakala <jhakala@student.hive.fi>          +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/10/16 11:07:07 by jhakala           #+#    #+#              #
#    Updated: 2020/01/10 21:50:26 by jhakala          ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = libft.a

SRC = ft_atoi.c ft_bzero.c ft_isalnum.c ft_isalpha.c ft_isascii.c \
	ft_isdigit.c ft_isprint.c ft_itoa.c ft_memalloc.c ft_memccpy.c \
	ft_memchr.c ft_memcmp.c ft_memcpy.c ft_memdel.c ft_memmove.c \
	ft_memset.c ft_putchar_fd.c ft_putchar.c ft_putendl_fd.c ft_putendl.c \
	ft_putnbr_fd.c ft_putnbr.c ft_putstr_fd.c ft_putstr.c ft_strcat.c \
	ft_strchr.c ft_strclr.c ft_strcmp.c ft_strcpy.c ft_strdel.c \
	ft_strdup.c ft_strequ.c ft_striter.c ft_striteri.c ft_strjoin.c \
	ft_strlcat.c ft_strlen.c ft_strmap.c ft_strmapi.c ft_strncat.c \
	ft_strncmp.c ft_strncpy.c ft_strnequ.c ft_strnew.c ft_strnstr.c \
	ft_strrchr.c ft_strsplit.c ft_strstr.c ft_strsub.c ft_strtrim.c \
	ft_tolower.c ft_toupper.c ft_lstnew.c ft_lstdelone.c ft_lstdel.c \
	ft_lstadd.c ft_lstiter.c ft_lstmap.c ft_swap_content.c ft_swap_address.c \
	ft_countdigit.c ft_lstcontent.c ft_lstprint.c ft_lstrev.c get_next_line.c \
	ft_wordlen.c ft_atoi_base.c \
	f_printf.c f_parse.c f_flags_handle.c f_length_types.c f_write.c f_writef.c \
	f_type_bases.c f_flags_utils.c \
	type_c.c type_d.c type_s.c type_o.c type_x.c type_f.c

OBJ = $(SRC:.c=.o)

S_DIR = src
O_DIR = obj

SRCS = $(addprefix $(S_DIR)/, $(SRC))
OBJS = $(addprefix $(O_DIR)/, $(OBJ))

HEAD = includes/

all: $(NAME)


$(O_DIR)/%.o: $(S_DIR)/%.c
	@/bin/mkdir -p $(O_DIR)
	@gcc -Wall -Wextra -Werror -c -I $(HEAD) $< -o $@

$(NAME): $(OBJS)
	@ar rcs $@ $^
	@ranlib $@
	@echo libft done.

clean:
	@/bin/rm -rf $(O_DIR)
	@echo clean done.

fclean: clean
	@/bin/rm -f $(NAME)
	@echo fclean done.

re: fclean all
