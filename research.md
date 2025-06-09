---
layout: page
title: research
permalink: /research/
---

<div style="text-align: left; margin-bottom: 1em;">
  <h3 style="color:rgb(238, 188, 108);font-weight: normal;">
    1-	Inference of preference measures in economic decision making
  </h3>
</div>

Optimal decision-making in volatile environments requires the brain to effectively represent uncertainty. While expected utility theory provides a framework for understanding choices under uncertainty, its limitations have motivated the exploration of alternative normative and descriptive theories. However, the specific preference measure employed by the brain remains unclear. 

<div style="text-align: center; margin-top: 10px;">
  <img src="/files/economic_preferences.gif" alt="economic_preferences" style="width: 70%; height: auto; margin-bottom: 10px;">
</div>

In this project, we introduce a novel approach for identifying an agent’s underlying preference measure. We hypothesize that reward distributions are encoded via the expected values of the encoding functions of dopaminergic neurons, an encoding scheme known as distributed distributional coding (DDC). We begin by demonstrating that this hypothesis aligns broadly with dopamine responses observed in the ventral tegmental area (VTA). We then propose a DDC-based network architecture accompanied by a simple learning rule capable of inferring a wide range of preference measures employed by agents in economic decision-making.

<div style="text-align: center; margin-top: 10px;">
  <img src="/files/learning_expected_utility.gif" alt="learning_expected_utility" style="width: 90%; height: auto; margin-bottom: 10px;">
</div>

<hr style="border: none; border-top: 2px solid #757575; width: 100%; margin: 10px auto;">

<!------------------------------------------------------------->

<div style="text-align: left; margin-bottom: 1em;">
  <h3 style="color:rgb(238, 188, 108); font-weight: normal;">
    2-	Dopaminergic computation of economic preferences
  </h3>
</div>

Various frameworks have been proposed to characterize how the brain represents reward distributions. Distributed distributional coding (DDC) posits that dopamine neurons represent reward distributions via the expected values of their encoding functions. We introduce a biologically plausible recursive update rule that operates on received reward instances and demonstrate that the responses of dopamine neurons converge to the DDC representation of the reward distribution.
A linear projection of dopamine neurons computes the expected utility of the reward distribution, where the utility function is embedded within the synaptic readout weights. We further show that a broad spectrum of preference measures, such as expected tail gain and compound utility-risk measures, can be efficiently computed via mapping the parallel readouts of dopamine neurons.

<div style="text-align: center; margin-top: 10px;">
  <img src="/files/dopaminergic_computation.gif" alt="dopaminergic_computation" style="width: 90%; height: auto; margin-bottom: 10px;">
</div>

<hr style="border: none; border-top: 2px solid #757575; width: 100%; margin: 10px auto;">

<!------------------------------------------------------------->

<div style="text-align: left; margin-bottom: 1em;">
  <h3 style="color:rgb(238, 188, 108); font-weight: normal;">
    3-	Learning efficient distributional codes
  </h3>
</div>

The precise mechanisms by which the brain learns efficient representations for uncertainty and probability distributions remain unresolved. In this project, we consider distributed distributional codes (DDC) to represent a probability distribution and propose an information-theoretic approach for learning DDC encoding functions. We assume that the distributional beliefs have a sparse representation in some basis and employ a generative model with hierarchical priors to model noisy DDC values. We find a posterior distribution over the distributional beliefs that are consistent with the observed DDC values. The encoding functions are modified to minimize agent’s uncertainty about the belief. This is achieved by minimizing the entropy of the posterior distribution over the beliefs. We show that the learned encoding functions can capture some of the properties of neuronal tuning functions.

<div style="text-align: center; margin-top: 10px;">
  <img src="/files/learning_distributional_representations.gif" alt="learning_distributional_representations" style="width: 90%; height: auto; margin-bottom: 10px;">
</div>

<hr style="border: none; border-top: 2px solid #757575; width: 100%; margin: 10px auto;">

<!------------------------------------------------------------->

<div style="text-align: left; margin-bottom: 1em;">
  <h3 style="color:rgb(238, 188, 108); font-weight: normal;">
    4-	Spatial navigation under uncertainty
  </h3>
</div>

Spatial navigation is conducted through combining path integration signals with incoming sensory modalities. The noise and intrinsic ambiguity of the sensory signals together with the noisy path integration system lead to positional uncertainty. To behave optimally in a navigation task, the agents should take into account the uncertainty of the input signals and infer a distributional belief about their location. Different frameworks have been suggested for the representation of positional uncertainty in the brain, such as sampling, probabilistic population codes, and distributed distributional codes (DDC). However, it remains unclear how the brain represents positional beliefs and how the hippocampus employs these representations to perform spatial navigation. 
We assume that given the history of sensory observations and efference copies of the motor commands, the posterior distribution over the location is represented by the DDC values. We show that the agent can update the DDC values recursively and conduct probabilistic localization. Furthermore, we demonstrate that using a DDC-based learning rule, the agent can gradually learn the task’s generative structure, encompassing the state transition matrix and the emission probabilities.

<div style="text-align: center; margin-top: 10px;">
  <img src="/files/spatial_navigation.gif" alt="spatial_navigation" style="width: 90%; height: auto; margin-bottom: 10px;">
</div>

<hr style="border: none; border-top: 2px solid #757575; width: 100%; margin: 10px auto;">

<!------------------------------------------------------------->

<div style="text-align: left; margin-bottom: 1em;">
  <h3 style="color:rgb(238, 188, 108); font-weight: normal;">
    5-	Planning under uncertainty
  </h3>
</div>

We have previously demonstrated how an agent can utilize distributed distributional codes (DDC) to perform probabilistic localization and structural learning. A central task in spatial navigation involves planning trajectories to reach designated goal locations. The neural mechanisms that support planning under uncertainty remain relatively unexplored. 
After learning the transition structure of the environment, the value iteration algorithm can be used to derive the optimal value function for each location in the environment. In a setting without positional uncertainty, an agent could simply follow the action that maximizes the value at each location to reach its target. However, since the true location is a latent variable, the agent must rely on the DDC values of the posterior distribution over location.
We show that for each action, a weighted sum of the DDC values provides the expected value of that action, and by choosing the action corresponding to the highest expected value function, the animal can find an effective policy for planning. The simulations confirm that by following this DDC-based policy, the animal can take the positional uncertainty into account and reach the goal efficiently. 

<div style="text-align: center; margin-top: 10px;">
  <img src="/files/planning.gif" alt="planning" style="width: 60%; height: auto; margin-bottom: 10px;">
</div>

<hr style="border: none; border-top: 2px solid #757575; width: 100%; margin: 10px auto;">

<!------------------------------------------------------------->

<div style="text-align: left; margin-bottom: 1em;">
  <h3 style="color:rgb(238, 188, 108); font-weight: normal;">
    6-	Information flow in dynamic synapses
  </h3>
</div>

Chemical synapses transmit information by releasing vesicles packed with neurotransmitter. Synaptic release is not a reliable process, as sometimes action potentials fail to trigger the release, or vesicles are released spontaneously. We use a binary asymmetric channel to model a single release site. This model encompasses different modes of release in a synapse: synchronous spike-evoked release and asynchronous release; spontaneous release is also subsumed under asynchronous release. Short-term plasticity changes synaptic release probabilities based on the release history and spiking activity profile of the synapse. We extend our model to plastic synapses by adding a memory to the binary asymmetric channel; the state of the channel is determined by its memory content. We calculate the mutual information rate and energy-normalized information rate of the synapse analytically. We then employ this analytical framework to investigate the functional role of short-term depression and facilitation, the energy-rate trade-off, and the effect of asynchronous and spontaneous release on synaptic transmission.

<div style="text-align: center; margin-top: 10px;">
  <img src="/files/synaptic_information_flow.gif" alt="synaptic_information_flow" style="width: 90%; height: auto; margin-bottom: 10px;">
</div>

<hr style="border: none; border-top: 2px solid #757575; width: 100%; margin: 10px auto;">

<!------------------------------------------------------------->

<div style="text-align: left; margin-bottom: 1em;">
  <h3 style="color:rgb(238, 188, 108); font-weight: normal;">
    7-	Spike detection through fractal dimension analysis
  </h3>
</div>

Various algorithms have been proposed for spike detection and sorting in extracellular recording. Nevertheless, it is still challenging to detect spikes in low signal-to-noise ratio (SNR) regimes. We study the fractal properties of extracellular signals and demonstrate that the fractal dimension of the spike segments of the extracellular signal is on average lower than the fractal dimension of the noise segments. We incorporate this idea into a new spike detection algorithm, called fractal detector. We simulate extracellular signals using a dataset of spike shapes and model the noise signal by two components corresponding to thermal noise and inter-spike noise. We compare the performance of the fractal detector with the commonly used spike detectors (threshold detector, PCA-wavelet detector, and matched filter detector). We show that in low SNR regime, the fractal detector outperforms the other spike detectors.

<div style="text-align: center; margin-top: 10px;">
  <img src="/files/fractal_detector.gif" alt="fractal_detector" style="width: 90%; height: auto; margin-bottom: 10px;">
</div>

<hr style="border: none; border-top: 2px solid #757575; width: 100%; margin: 10px auto;">

<!------------------------------------------------------------->


<div style="text-align: left; margin-bottom: 1em;">
  <h3 style="color:rgb(238, 188, 108); font-weight: normal;">
    8-	Spatial network coding
  </h3>
</div>

In conventional data networks, nodes function as passive relays, forwarding received packets to the next hop based on destination information. In contrast, when network coding is employed, intermediate nodes are allowed to compute and transmit functions of incoming packets. This strategy can increase the network’s information throughput in certain communication scenarios. 
We study the capacity of a multicast session in an interference-free broadcast erasure network, under a class of network coding schemes referred to as spatial network coding. In this class of coding, nodes are prohibited from performing coding on successive data units of a link; only data units arriving on different incoming links to a node may be combined. We prove that the capacity of a unicast session is equal to the statistical mean of the minimum cut rate of the corresponding random graph, where the notions of graph model and minimum cut rate are extended to apply to broadcast networks. We then extend the analysis and show that the capacity of a multicast session in a broadcast erasure network is equal to the minimum of the capacities of the constituent unicast sessions.

<div style="text-align: center; margin-top: 10px;">
  <img src="/files/spatial_network_coding.gif" alt="spatial_network_coding" style="width: 90%; height: auto; margin-bottom: 10px;">
</div>
