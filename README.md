# crackyourinternship#include<iostream>
#include<vector>
#include<queue>
using namespace std;
bool DFSRec(vector<int>adj[],bool visited[],int s,int parent){
    visited[s] = true;
    for(int u : adj[s]){
        if (visited[u] == false)
        {
            /* code */if ((adj,visited,u,0) == true)
            {
                /* code */return true;
            }
            else if (u != parent)
            {
                /* code */return true;
            }
            
        }
        
    }
    return false;
}
bool DFS(vector<int>adj[],int v){
    bool visited[v];
    for (int i = 0; i < v; i++)
    {
        /* code */visited[i] = false;
    }
    for (int i = 0; i < v; i++)
    {
        /* code */if (visited[i] == false)
        {
            /* code */if(DFSRec(adj,visited,i,-1) == true) {
                return true;
            }
        }
        
    }
    return false;
}
void add(vector<int>adj[],int u,int v){
    adj[u].push_back(v);
    adj[v].push_back(u);
}
int main()
{
    int v = 5;
    vector<int>adj[v];
    add(adj,0,1);
    add(adj,1,2);
    add(adj,1,4);
    // add(adj,2,1);
    add(adj,2,3);
    // add(adj,3,2)??;
cout<<boolalpha<<DFS(adj,v);

    return 0;
}
