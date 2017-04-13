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


## Paper


[Hybrid Code Networks: practical and efficient end-to-end dialog control with supervised and reinforcement learning](https://arxiv.org/abs/1702.03274)


## TODO

- [ ] Train on OOV data
- [ ] Apply Reinforcement Learning (Policy Gradients)
