#include <iostream>
using namespace std;

class Stack {
    int stack[10];
    int top;

public:
    Stack() {
        top = -1;
    }

    void push(int value) {
        if (top == 9) {
            cout << "Stack Overflow" << endl;
        } else {
            top++;
            stack[top] = value;
        }
    }

    void pop() {
        if (top == -1) {
            cout << "Stack Underflow" << endl;
        } else {
            cout << "Deleted element: " << stack[top] << endl;
            top--;
        }
    }

    void peek() {
        if (top == -1) {
            cout << "Stack is Empty" << endl;
        } else {
            cout << "Top element: " << stack[top] << endl;
        }
    }

    void display() {
        if (top == -1) {
            cout << "Stack is Empty" << endl;
        } else {
            cout << "Stack Elements: ";
            for (int i = top; i >= 0; i--) {
                cout << stack[i] << " ";
            }
            cout << endl;
        }
    }
};

int main() {
    Stack s;
    int choice, value;

    do {
        cout << "\n1. Push\n2. Pop\n3. Peek\n4. Display\n5. Exit\n";
        cout << "Enter your choice: ";
        cin >> choice;

        switch (choice) {
            case 1:
                cout << "Enter value: ";
                cin >> value;
                s.push(value);
                break;

            case 2:
                s.pop();
                break;

            case 3:
                s.peek();
                break;

            case 4:
                s.display();
                break;

            case 5:
                cout << "Program Ended";
                break;

            default:
                cout << "Invalid Choice";
        }

    } while (choice != 5);

    return 0;
}
