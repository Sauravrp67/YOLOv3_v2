 - **Pretrained Model Weights Download**

	- [DarkNet-53 Backbone](https://drive.google.com/file/d/1duXcafb2QgORHDO1w-7E1UusLfWInwgA/view?usp=drive_link)
	- [DarkNet-53-tiny Backbone](https://drive.google.com/file/d/13X39tcmNnYghvdBiosma7gsfwCxjsFQx/view?usp=drive_link)

## [Usage]

####  Anchor Clustering   
 - extract anchor box from all instances boxes.

 ```python
python kmedoids_anchor.py --exp my_test --data voc.yaml  --n-cluster 9
 ```
#### Model Training 
 - Train model using this command. You can train on your custom dataset, but the dataset must be in the structure inside yaml. 

```python
python train.py --exp my_test --data voc.yaml --multiscale(optional) --scratch(optional)
```

#### Evaluation
 - You can run evaluation using this command

```python
python val.py --exp my_test --data voc.yaml --ckpt-name best.pt
```
