# Copyright (C) 2008 Michael Jackson
#
# Use, modification and distribution is subject to the Boost Software
# License, Version 1.0. (See accompanying file LICENSE_1_0.txt or copy at
# http://www.boost.org/LICENSE_1_0.txt)

ryppl_additional_test_dependencies(graph BOOST_DEPENDS test assign)

ryppl_test_run(transitive_closure_test)
ryppl_test_compile(adj_list_cc)
ryppl_test_run(adj_list_edge_list_set)
ryppl_test_compile(adj_matrix_cc)
ryppl_test_run(bfs)
ryppl_test_compile(bfs_cc)
ryppl_test_run(bellman-test)
ryppl_test_run(betweenness_centrality_test DEPENDS ryppl_graph SHARED)
ryppl_test_run(csr_graph_test)
ryppl_test_run(dag_longest_paths)
ryppl_test_run(dfs)
ryppl_test_compile(dfs_cc)
ryppl_test_compile(dijkstra_cc)
ryppl_test_run(dijkstra_heap_performance ARGS 10000 DEPENDS ryppl_graph SHARED)
ryppl_test_run(dominator_tree_test)
ryppl_test_run(relaxed_heap_test ARGS 5000 15000)
ryppl_test_compile(edge_list_cc)
ryppl_test_compile(filtered_graph_cc)
ryppl_test_run(generator_test)
ryppl_test_run(graph)
ryppl_test_compile(graph_concepts)
ryppl_test_run(graphviz_test 
  DEPENDS ryppl_test_exec_monitor ryppl_graph STATIC)
ryppl_test_run(gursoy_atun_layout_test)
ryppl_test_run(layout_test)
ryppl_test_run(serialize DEPENDS ryppl_serialization)
ryppl_test_compile(reverse_graph_cc)
ryppl_test_run(sequential_vertex_coloring)
ryppl_test_run(subgraph)
ryppl_test_run(isomorphism)
ryppl_test_run(adjacency_matrix_test)
ryppl_test_compile(vector_graph_cc)
ryppl_test_compile(copy)
ryppl_test_compile(property_iter)
ryppl_test_run(bundled_properties)
ryppl_test_run(floyd_warshall_test)
ryppl_test_run(astar_search_test)
ryppl_test_run(biconnected_components_test)
ryppl_test_run(cuthill_mckee_ordering)
ryppl_test_run(king_ordering)
ryppl_test_run(matching_test)
ryppl_test_run(mcgregor_subgraphs_test)
# ryppl_test_run(max_flow_test)
# ryppl_test_run(kolmogorov_max_flow_test) TODO: Boost 1.34.x only

# GraphML Tests - not for Boost 1.34.x
#include(FindEXPAT)
#if (EXPAT_FOUND)
#  include_directories(${EXPAT_INCLUDE_DIRS})
#  ryppl_test_run(graphml_test LIBRARIES ryppl_graph)
#endif (EXPAT_FOUND)

# Stanford GraphBase Tests
if ($ENV{SDB})
  include_directories("$ENV{SDB}")
  ryppl_test_compile(stanford_graph_cc)
endif ($ENV{SDB})

# LEDA tests
if ($ENV{LEDA})
  include_directories("$ENV{LEDA}/incl")
  ryppl_test_compile(leda_graph_cc)
endif ($ENV{LEDA}) 
