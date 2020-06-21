# xnornet_plusplus

Code for training binary networks on imagenet. 
Xnornet algorithm(https://arxiv.org/abs/1603.05279) is one of the most cited works for training a quantized neural network with 1 bit weight and 1 bit activation. There are numerous work on quantization of neural networks that refer xnornet. Xnornet++(https://arxiv.org/abs/1909.13863) is one such work. As the name suggesets, it is an improvement over the xnornet in terms of accuracy. This code simulates the xnornet++ paper. 
Binarized networks are infamous for not being very easy to get the network converge. Hopefully this code will help you get started with network quantization

## Accuracy on Imagenet Validation
|  Network  | Top1(%) |
|-----------|---------|
| Resnet-18 |    56.8 |

## Dependencies

 - Pytorch - 1.5.0 
 - TensorboardX
   pip install tensorboardx 
 

## Training

Download imagenet dataset 
Run the following command to train a resnet-18 network 

    python main.py path_to_imagenet_dataset -a resnet18_preact_bin --lr 1e
    -3 --optimizer adam --weight-decay 1e-5 --workers 16 --model_dir data/binary_1 --batch-size 256
## Acknowledgement

[https://github.com/jiecaoyu/XNOR-Net-PyTorch](https://github.com/jiecaoyu/XNOR-Net-PyTorch)

[https://github.com/pytorch/examples/blob/0.3.1/imagenet/main.py](https://github.com/pytorch/examples/blob/0.3.1/imagenet/main.py)