# egjoghak ([wolfram/products](https://www.wolfram.com/products/?source=frontpage-carousel))

Egjoghak is a fictional word or phrase, often used in the context of fantasy literature or movies. It does not have a direct meaning in English, but it could be a placeholder or a reference to a specific character or concept.

In the provided code snippet, egjoghak is a comment line in Markdown format. The comment does not provide any additional context or information about the code block. It is simply a placeholder or a joke.

# makefile formatting functions for Markdown
```makefile
CXX = g++
CXXFLAGS = -Wall -Werror -Wextra -pedantic -std=c++17 -g main.cpp
LDFLAGS =  main.cpp

SRC =
OBJ = $(SRC:.cc=.o)
EXEC = egjoghak

all: $(EXEC)

$(EXEC): $(OBJ)
	$(CXX) $(LDFLAGS) -o $@ $(OBJ) $(LBLIBS)

clean:
	rm -rf $(OBJ) $(EXEC)
```
# Example usage example for Windows
```c++
#include <string.h>
#include <ctype.h>
#include <assert.h>
#include <stdio.h>

#define MAX_INPUT_LENGTH 1000
#define MAX_WORD_LENGTH 100

void reverse_string(char* str) {
    int start = 0;
    int end = strlen(str) - 1;

    while (start < end) {
        char temp = str[start];
        str[start] = str[end];
        str[end] = temp;
        start++;
        end--;
    }
}

void reverse_words(char* str) {
    int start = 0;
    int end = 0;

    while (str[end] != '\0') {
        if (isspace(str[end])) {
            reverse_string(str + start);
            start = end + 1;
        }
        end++;
    }

    reverse_string(str + start);
    reverse_string(str);
}

void reverse_sentence(char* sentence) {
    reverse_words(sentence);

    int start = 0;
    int end = 0;

    while (sentence[end] != '\0') {
        if (sentence[end] == '.' || sentence[end] == '!' || sentence[end] == '?') {
            reverse_string(sentence + start);
            start = end + 1;
        }
        end++;
    }

    reverse_string(sentence + start);
}

int main() {
    char input[MAX_INPUT_LENGTH];

    printf("Enter a sentence: ");
    fgets(input, MAX_INPUT_LENGTH, stdin);
    input[strcspn(input, "\n")] = '\0';  // Remove newline character

    reverse_sentence(input);

    printf("Reversed sentence: %s\n", input);

    return 0;
}
```
# install makefile 
$-> make all

