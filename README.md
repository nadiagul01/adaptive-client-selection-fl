Adaptive Client Selection for Fair and Efficient Federated Learning

A lightweight client-selection framework (ACS) for federated learning that improves accuracy, convergence speed, and fairness simultaneously in non-IID settings.

Overview

Random client selection in federated learning leads to biased global models, slow convergence, and unfair client participation under non-IID data. ACS ranks clients using a composite score based on dataset size, label entropy, and gradient divergence, combined with a fairness-aware participation penalty.

Key Highlights


Composite client score (dataset size, label entropy, gradient divergence; weighted 0.4/0.35/0.25) with a fairness-aware participation penalty to prevent over-selection of dominant clients.
Dual-weighted aggregation scheme weighting updates by both data quantity and quality score.
Evaluated on CIFAR-10 (25 clients, Dirichlet α=0.5, 120 rounds) against FedAvg, FedHD, and cost-aware selection.
Reached 50% validation accuracy in just 10 rounds — 2.5× faster than FedAvg, 44% faster than FedHD — with a final accuracy of 63.42%.
Improved long-term participation fairness to a Jain's fairness index of 0.92 (vs. 0.75 for FedAvg), without Shapley-value computation, multi-armed bandits, or mixed-integer programming.

