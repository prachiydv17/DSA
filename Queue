#include <iostream>
using namespace std;

class Queue {
    int queue[10];
    int front, rear;

public:
    Queue() {
        front = -1;
        rear = -1;
    }

    void enqueue(int value) {
        if (rear == 9) {
            cout << "Queue Overflow" << endl;
        } else {
            if (front == -1)
                front = 0;
            rear++;
            queue[rear] = value;
        }
    }

    void dequeue() {
        if (front == -1 || front > rear) {
            cout << "Queue Underflow" << endl;
        } else {
            cout << "Deleted element: " << queue[front] << endl;
            front++;
        }
    }

    void peek() {
        if (front == -1 || front > rear) {
            cout << "Queue is Empty" << endl;
        } else {
            cout << "Front element: " << queue[front] << endl;
        }
    }

    void display() {
        if (front == -1 || front > rear) {
            cout << "Queue is Empty" << endl;
        } else {
            cout << "Queue Elements: ";
            for (int i = front; i <= rear; i++) {
                cout << queue[i] << " ";
            }
            cout << endl;
        }
    }
};

int main() {
    Queue q;
    int choice, value;

    do {
        cout << "\n1. Enqueue\n2. Dequeue\n3. Peek\n4. Display\n5. Exit\n";
        cout << "Enter your choice: ";
        cin >> choice;

        switch (choice) {
            case 1:
                cout << "Enter value: ";
                cin >> value;
                q.enqueue(value);
                break;

            case 2:
                q.dequeue();
                break;

            case 3:
                q.peek();
                break;

            case 4:
                q.display();
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
