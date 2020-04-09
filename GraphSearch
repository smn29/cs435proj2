import java.util.*;
import java.util.HashMap;
import java.util.HashSet;
import java.util.Arraylist;
import java.util.Stack;
import java.util.LinkedList; 
import java.util.Queue; 

public class GraphSearch{
  public ArrayList<Node> DFSRec(final Node start, final Node end){
    ArrayList<Node> aln = new Arraylist<Node>();
    int size = aln.size();
  
    if(start == end){
      return null;
    }

    aln.add(start);
    start.isvisited = true;
    HashMap<Integer, Node> map = start.nodes.data();
    for(Node node: map){
      if(!node.isvisited()){
        DFSRec(node, end);
      }
      if(aln.get(size-1) == end){
        return aln;
      }
    }
    return null; 
  }

  public ArrayList<Node> DFSIter(final Node start, final Node end){
    ArrayList<Node> aln = new Arraylist<Node>();
    int size = aln.size();
  
    if(start == end){
      return null;
    }
    //used Geeks for Geeks as reference: https://www.geeksforgeeks.org/iterative-depth-first-traversal/

    Stack<node> stack = new Stack<Node>();
    stack.push(start);
    start.isvisited = true;
    while(!stack.empty()){
      Node node = stack.peek();
      aln.add(node);
      HashMap<Integer, Node> map = start.nodes.data();
      for(Node n: map){
        if(!node.isvisited()){
          node.setTrue();
          stack.push(n);
        }
        if(aln.get(size-1) == end){
          return aln;
        }
      } 
    }
    return null;
    }

  public ArrayList<Node> BFTRec(final Graph graph, Node n) {
    ArrayList<Node> aln = new Arraylist<Node>();
    Queue<Node> q = new LinkedList<>(); 
    HashSet<Node> set = graph.getAllNodes();

    for(Node n: set){
      if(!n.isvisited){
        n.setTrue();
        q.add(n);
        Node node = q.pop();
        aln.add(node);
        HashMap<Integer, Node> nodemap = node.nodes();
        for(Node next: nodemap.data()){
          if(!next.isvisited()){
            next.setTrue();
            q.add(next)
            BFTRec(graph, next);
          }
        }
      }
    }

    return aln;

  }

  public ArrayList<Node> BFTIter(final Graph graph){
    ArrayList<Node> aln = new Arraylist<Node>();
    Queue<Node> q = new LinkedList<>(); 
    HashSet<Node> set = graph.getAllNodes();

    for(Node n: set){
      if(!n.isvisited){
        n.setTrue();
        q.add(n);
      }
      while(!q.isEmpty()){
        Node node = q.pop();
        aln.add(node);
        HashMap<Integer, Node> nodemap = node.nodes();
        for(Node next: nodemap.data()){
          if(!next.isvisited()){
            next.setTrue();
            q.add(next)
      }
    }
  }
  
  return aln;
}
