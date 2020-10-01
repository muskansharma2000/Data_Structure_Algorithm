# Data Structure & Algorithm
Language : C


Ps:Share some of your algoritms ^_^
Shortest path by Dijkstra added to dynamic programming 
sudo code:
  function Dijkstra(Graph, source):
       dist[source]  := 0                     // Distance from source to source
       for each vertex v in Graph:            // Initializations
           if v ≠ source
               dist[v]  := infinity           // Unknown distance function from source to v
               previous[v]  := undefined      // Previous node in optimal path from source
           end if 
           add v to Q                         // All nodes initially in Q
       end for
      
      while Q is not empty:                  // The main loop
          u := vertex in Q with min dist[u]  // Source node in first case
          remove u from Q 
          
          for each neighbor v of u:           // where v has not yet been removed from Q.
              alt := dist[u] + length(u, v)
              if alt < dist[v]:               // A shorter path to v has been found
                  dist[v]  := alt 
                  previous[v]  := u 
              end if
          end for
      end while
      return dist[], previous[]
  end function
