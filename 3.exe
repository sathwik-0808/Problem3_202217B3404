#include <stdio.h>
#include <stdlib.h>
 
#define MAX 100 // Define stack size
 
typedef struct Stack {
    int data[MAX];
    int top;
} Stack;
 
// Function prototypes
void push(Stack* stack, int value);
int pop(Stack* stack);
int isFull(Stack* stack);
int isEmpty(Stack* stack);
void display(Stack* stack);
void push(Stack* stack, int value) {
    if (isFull(stack)) {
        printf("Stack overflow! Cannot push %d\n", value);
    } else {
        stack->data[++stack->top] = value;
        printf("%d pushed onto stack\n", value);
    }
}
int pop(Stack* stack) {
    if (isEmpty(stack)) {
        printf("Stack underflow! Cannot pop\n");
        return -1;
    } else {
        return stack->data[stack->top--];
    }
}
int isFull(Stack* stack) {
    return stack->top == MAX - 1;
}
 
int isEmpty(Stack* stack) {
    return stack->top == -1;
}
void display(Stack* stack) {
    if (isEmpty(stack)) {
        printf("Stack is empty\n");
    } else {
        printf("Stack elements: ");
        for (int i = 0; i <= stack->top; i++) {
            printf("%d ", stack->data[i]);
        }
        printf("\n");
    }
}
int main() {
    Stack stack;
stack.top = -1;
    int choice, value;
 
    while (1) {
        printf("\nStack Operations:\n");
        printf("1. Push\n");
        printf("2. Pop\n");
        printf("3. Display\n");
        printf("4. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);
 
        switch (choice) {
            case 1:
                printf("Enter value to push: ");
                scanf("%d", &value);
                push(&stack, value);
                break;
            case 2:
                value = pop(&stack);
                if (value != -1) {
                    printf("%d popped from stack\n", value);
                }
                break;
            case 3:
                display(&stack);
                break;
            case 4:
                exit(0);
            default:
                printf("Invalid choice, please try again\n");
        }
    }
    return 0;
}