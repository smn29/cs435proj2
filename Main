import java.util.*;
import java.util.HashMap;
import java.util.HashSet;
import java.util.Random;
import java.util.ArrayList;

public class Main {
  public static void main(String[] args) {
    BFTRecLinkedList(10000);
    BFTIterLinkedList(10000);
  }

  public Graph createRandomUnweightedGraphIter(int x){
    Graph g = new Graph();
    Random rand = new random();
    HashSet<Node> set = g.getAllNodes();
    for(int i = 0; i < x; i++){
      g.addNode(i);
      Node n = g.nodegraph.get(i);
      for(Node node: set){
        ri = rand.nextInt(n);      
        if((ri%2 == 0)){
          g.addUndirectedEdge(n, node);
        }
      }
    }
    return g;
  }

  public Graph createLinkedList(int n){
    Graph g = new Graph();
    for(int i = 1; i <= n; i++){
      g.addNode(i);
      Node pos = g.nodegraph.get(i);
      g.addNode(i+1);
      Node next = g.nodegraph.get(i+1);
      pos.nodes.put(next.data(), next);
    }
  }

  public static ArrayList<Node> BFTRecLinkedList(final int n){
		return GraphSearch.BFTRec(createLinkedList(n));
	}
	
	public static ArrayList<Node> BFTIterLinkedList(final int n){
		return GraphSearch.BFTIter(createLinkedList(n));
	}
}
