## LAB 1
### Introduction
* Modify input tensor of Resnet50 & run shape inference to get the shape of all tensors.  
* Show the results by Netron (https://netron.app/).
### How to reproduce the result
1. ```docker-compose up -d``` and http://localhost:8323/, you may change the port and image/container name in the yaml file.
2. Execute LAB1.ipynb in the jupyter.
3. ONNX file is in the ./model, and you can see the result by pushing the model to Netron (https://netron.app/).

### Result
#### Run shape inference to get the shape of all tensors
The following informations are the shapes of all tensors, and you can see the complete log in the LAB1.ipynb .
```txt
After shape inference: 

[name: "resnetv17_conv0_fwd"
type {
  tensor_type {
    elem_type: 1
    shape {
      dim {
        dim_value: 1
      }
      dim {
        dim_value: 64
      }
      dim {
        dim_value: 112
      }
      dim {
        dim_value: 112
      }
    }
  }
}
....
```
#### Netron
Before modifying input:
<img src="https://i.imgur.com/ZZRP7Ib.png">

After modifying input:
<img src="https://i.imgur.com/tdf6mSS.png">
