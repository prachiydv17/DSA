#include <iostream>
using namespace std;

class Graph
{
    int adj[20][20];
    int n;
    bool visited[20];

public:
    Graph()
    {
        n = 0;
        for (int i = 0; i < 20; i++)
            visited[i] = false;
    }

    void createGraph()
    {
        cout << "\nEnter number of vertices: ";
        cin >> n;

        for (int i = 0; i < n; i++)
        {
            for (int j = 0; j < n; j++)
            {
                adj[i][j] = 0;
            }
        }

        int edges;
        cout << "Enter number of edges: ";
        cin >> edges;

        cout << "Enter edges (source destination):\n";

        for (int i = 0; i < edges; i++)
        {
            int u, v;
            cin >> u >> v;

            adj[u][v] = 1;
            adj[v][u] = 1;
        }

        cout << "\nGraph created successfully!\n";
    }

    void displayMatrix()
    {
        cout << "\nAdjacency Matrix:\n";

        for (int i = 0; i < n; i++)
        {
            for (int j = 0; j < n; j++)
            {
                cout << adj[i][j] << " ";
            }
            cout << endl;
        }
    }

    void DFS(int start)
    {
        visited[start] = true;
        cout << start << " ";

        for (int i = 0; i < n; i++)
        {
            if (adj[start][i] == 1 && !visited[i])
            {
                DFS(i);
            }
        }
    }

    void DFSTraversal()
    {
        if (n == 0)
        {
            cout << "\nPlease create the graph first!\n";
            return;
        }

        for (int i = 0; i < 20; i++)
        {
            visited[i] = false;
        }

        int start;
        cout << "\nEnter starting vertex: ";
        cin >> start;

        if (start < 0 || start >= n)
        {
            cout << "Invalid starting vertex!\n";
            return;
        }

        cout << "DFS Traversal: ";
        DFS(start);
        cout << endl;
    }
};

int main()
{
    Graph g;
    int choice;

    do
    {
        cout << "\n===== Graph Menu =====";
        cout << "\n1. Create a Graph";
        cout << "\n2. Display Graph (Adjacency Matrix)";
        cout << "\n3. DFS Traversal";
        cout << "\n4. Exit";
        cout << "\nEnter your choice: ";
        cin >> choice;

        switch (choice)
        {
        case 1:
            g.createGraph();
            break;

        case 2:
            g.displayMatrix();
            break;

        case 3:
            g.DFSTraversal();
            break;

        case 4:
            cout << "\nExiting program...\n";
            break;

        default:
            cout << "\nInvalid choice! Please try again.\n";
        }

    } while (choice != 4);

    return 0;
}
