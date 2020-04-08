import java.util.*;
import java.util.HashMap;
import java.util.HashSet;

public class Graph{
  HashSet<Node> nodeset;
  HashMap<Integer, Node> nodegraph;

  public Graph(){
    nodeset = new HashSet<Node>();
    nodegraph = new HashMap<Integer, Node>();
  }

  public void addNode(final int nodeVal){
    Node n = new Node(nodeVal);
    nodeset.add(n);
    nodegraph.put(nodeVal, n);
  }

  public void addUndirectedEdge(final Node first, final Node second){
    fval = first.data();
    sval = second.data();
    if(nodegraph.containsValue(first)&&nodegraph.containsValue(second)){
      first.nodes.put(sval, second);
      second.nodes.put(fval, first);
    }
  }

  public void removeUndirectedEdge(final Node first, final Node second){
    fval = first.data();
    sval = second.data();
    if(nodegraph.containsValue(first)&&nodegraph.containsValue(second)){
      first.nodes.remove(fval);
      second.nodes.remove(sval);
    }
  }

  public HashSet<Node> getAllNodes(){
    return nodeset;
  }
}
