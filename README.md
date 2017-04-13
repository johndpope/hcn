# Hybrid Code Networks


![](https://img.shields.io/badge/tensorflow-1.0.1-green.svg) ![](https://img.shields.io/badge/gensim-2.0.0-blue.svg)

![](https://raw.githubusercontent.com/voicy-ai/DialogStateTracking/master/images/hcn-block-diagram.png)


## Setup


```bash
# install prerequisites
sudo -H pip3 install -r requirements.txt
cd data/ 
bash get_w2c_src.sh
```

## Execution


```bash
# training
python3 train.py
# training stops when accuracy on dev set becomes > 0.99
#  trained model is saved to ckpt/

# interaction 
python3 interact.py
# checkpoint from ckpt/ is loaded
#  start interaction
```

## Sample Interaction


![](https://raw.githubusercontent.com/voicy-ai/DialogStateTracking/master/images/hcn-interaction.png)

### TODO

- [ ] Train on OOV data
- [ ] Apply Reinforcement Learning (Policy Gradients)


## Paper

[Hybrid Code Networks](https://arxiv.org/abs/1702.03274) : practical and efficient end-to-end dialog control with supervised and reinforcement learning

End-to-end learning of recurrent neural networks (RNNs) is an attractive solution for dialog systems; however, current techniques are data-intensive and require thousands of dialogs to learn simple behaviors. We introduce Hybrid Code Networks (HCNs), which combine an RNN with domain-specific knowledge encoded as software and system action templates. Compared to existing end-to-end approaches, HCNs considerably reduce the amount of training data required, while retaining the key benefit of inferring a latent representation of dialog state. In addition, HCNs can be optimized with supervised learning, reinforcement learning, or a mixture of both. HCNs attain state-of-the-art performance on the bAbI dialog dataset, and outperform two commercially deployed customer-facing dialog systems.
