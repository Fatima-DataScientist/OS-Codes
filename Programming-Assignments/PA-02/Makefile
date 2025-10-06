# Makefile for PA-02 : lsv1.0.0
CC = gcc
CFLAGS = -Wall -Wextra -Wpedantic -std=c11 -g

SRC = lsv1.0.0.c
OBJ_DIR = obj
BIN_DIR = bin
TARGET = $(BIN_DIR)/lsv1.0.0

OBJS = $(OBJ_DIR)/lsv1.0.0.o

.PHONY: all clean run

all: $(TARGET)

$(OBJ_DIR)/%.o: %.c
	mkdir -p $(OBJ_DIR)
	$(CC) $(CFLAGS) -c $< -o $@

$(TARGET): $(OBJS)
	mkdir -p $(BIN_DIR)
	$(CC) $(CFLAGS) $^ -o $@

run: $(TARGET)
	./$(TARGET)

clean:
	rm -rf $(OBJ_DIR)/*.o $(TARGET)

