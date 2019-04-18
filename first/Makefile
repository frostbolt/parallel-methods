# 0 - последовательное умножение матрицы
# 1 - обычное умножение матрицы openmp
# 2 - необычное умножение матрицы openmp
TYPE_MUL = -DMATRTIX_MUL=2

COMPILER = mpicxx

FLAGS = -std=c++0x -O2 -Wall -Wextra -Wpedantic -fopenmp
#FLAGS = -std=c++11

OS := $(shell uname)
ifeq ($(OS),Darwin)
	COMPILER = g++-8
endif

ifdef SYSTEMROOT
    RM = del /Q
else
    RM = rm -f
endif


default: 
	$(COMPILER) -c $(FLAGS) $(TYPE_MUL) gz.cpp -o gz

clean:
	$(RM) *.o all
