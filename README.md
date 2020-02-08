# Local community detection in graph

FlowPro finds the community of a node in a complex network without the knowledge of the entire graph

Matlab Code: https://www.mathworks.com/matlabcentral/fileexchange/45868-local-community-detection-via-a-flow-propagation-flowpro-method

We propose a flow propagation algorithm (FlowPro) that finds the community of a node in a complex network without the knowledge of the entire graph. The novelty of the proposed approach is the fact that FlowPro is local and it does not require the knowledge of the entire graph as most of the existing methods from literature. This makes possible the application of FlowPro in extremely large graphs or in cases where the entire graph is unknown like in most social networks.
This code is a simple (not speed optimized) and Non Distributed implementation of FlowPro
based on the papers [1] and [2]. You can find more details in www.csd.uoc.gr/~cpanag

Files:
getCommunityFlowPro.m: implemetation of the method
getHighestDiff2.m: function that gives the community accrding to the stored flow
getCommunityFlowProSize.m:implemetation of the method when the size of community is given
data.mat: Synthetic Data (D) with N = 1000, Comm = 10, degree = 20, local/degree = 0.65
with ground truth (COMM) (see paper [1] for the parameters).
usage to run FlowPro for INIT = 1 :

load data;
[Cluster,per,S,maxITE,totalSMS] = getCommunityFlowPro(D,COMM,1);

usage to run FlowPro using for INIT = 1 and size of community = 100:

load data;
[ClusterSize,perSize] = getCommunityFlowProSize(D,COMM,100,1);

We will appreciate if you cite our paper [1] in your work:

[1] C. Panagiotakis, H. Papadakis and P. Fragopoulou, FlowPro: A Flow Propagation Method for Single Community Detection, IEEE Consumer Communications and Networking Conference, 2014.

[2] C. Panagiotakis, H. Papadakis and P. Fragopoulou, CoViFlowPro: A Community Visualization method based on a Flow Propagation Algorithm, International Conference on Bio-inspired Information and Communications Technologies (formerly BIONETICS) - BICT 2014, 2014.

[3] C. Panagiotakis, H. Papadakis, and P. Fragopoulou, Local Community Detection via Flow Propagation, International conference on Advances in Social Network Analysis and Mining (ASONAM), 2015.
