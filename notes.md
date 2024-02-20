
## Evaluation against single human CSE

- gt bbox roi pooling for original DensePose

```python

# inference 
CUDA_VISIBLE_DEVICES=2 python apply_net.py show configs/base_config.yaml model_final_1d3314.pkl "../../evals/pose_dataset" dp_vertex,bbox -v --output inference_results

# validation
CUDA_VISIBLE_DEVICES=2 python train_net.py --config-file configs/base_config.yaml --eval-only MODEL.WEIGHTS model_final_1d3314.pkl
```