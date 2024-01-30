<div align="center">
<h1>InstantID: Zero-shot Identity-Preserving Generation in Seconds</h1>



## Download
For face encoder, you need to manually download via this [URL](https://github.com/deepinsight/insightface/issues/1896#issuecomment-1023867304) to `models/antelopev2` as the default link is invalid.
Make sure the antelopev2.zip is unizipped to antelopev2 dir under model dir. For my demo I have mounted google drive and unzipped antelopev2 under /content/drive/MyDrive/models. You can choose own directory structure if you want.


## Start a gradio demo
Run the following command:
In my case the antelopev2 dir is under /content/drive/MyDrive/models
Run the command once we have proper directory structure
```python
python gradio_demo/app.py --face_analysis_root /content/drive/MyDrive/ 
```

## Usage Tips
- For higher similarity, increase the weight of controlnet_conditioning_scale (IdentityNet) and ip_adapter_scale (Adapter).
- For over-saturation, decrease the ip_adapter_scale. If not work, decrease controlnet_conditioning_scale.
- For higher text control ability, decrease ip_adapter_scale.
- For specific styles, choose corresponding base model makes differences.
- We have not supported multi-person yet, will only use the largest face as reference pose.
- We provide a [style template](https://github.com/ahgsql/StyleSelectorXL/blob/main/sdxl_styles.json) for reference.

## Community Resources

### Replicate Demo
- [zsxkib/instant-id](https://replicate.com/zsxkib/instant-id)

### WebUI
- [Mikubill/sd-webui-controlnet](https://github.com/Mikubill/sd-webui-controlnet/discussions/2589)

### ComfyUI
- [ZHO-ZHO-ZHO/ComfyUI-InstantID](https://github.com/ZHO-ZHO-ZHO/ComfyUI-InstantID)
- [huxiuhan/ComfyUI-InstantID](https://github.com/huxiuhan/ComfyUI-InstantID)

### Windows
- [sdbds/InstantID-for-windows](https://github.com/sdbds/InstantID-for-windows)

## Acknowledgements
- InstantID is developed by InstantX Team at Xiaohongshu Inc, all copyright reserved.
- Our work is highly inspired by [IP-Adapter](https://github.com/tencent-ailab/IP-Adapter) and [ControlNet](https://github.com/lllyasviel/ControlNet). Thanks for their great works!
- Thanks [ZHO-ZHO-ZHO](https://github.com/ZHO-ZHO-ZHO), [huxiuhan](https://github.com/huxiuhan), [sdbds](https://github.com/sdbds), [zsxkib](https://replicate.com/zsxkib) for their generous contributions.
- Thanks to the [HuggingFace](https://github.com/huggingface) gradio team for their free GPU support!
- Thanks to the [ModelScope](https://github.com/modelscope/modelscope) team for their free GPU support!

## Disclaimer
The code of InstantID is released under [Apache License](https://github.com/InstantID/InstantID?tab=Apache-2.0-1-ov-file#readme) for both academic and commercial usage. **However, both manual-downloading and auto-downloading face models from insightface are for non-commercial research purposes only** accoreding to their [license](https://github.com/deepinsight/insightface?tab=readme-ov-file#license). Users are granted the freedom to create images using this tool, but they are obligated to comply with local laws and utilize it responsibly. The developers will not assume any responsibility for potential misuse by users.

## Declaration
🚨🚨🚨 We solemnly clarify that [FAKE][FAKE][FAKE] http://instantid.org [FAKE][FAKE][FAKE] is not authorized and has no relationship with us. It is infringing and quite misleading, and has never contacted us for official cooperation. Please be aware of your personal privacy and subscription fraud. We reserve all legal rights.

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=InstantID/InstantID&type=Date)](https://star-history.com/#InstantID/InstantID&Date)


## Cite
If you find InstantID useful for your research and applications, please cite us using this BibTeX:

```bibtex
@article{wang2024instantid,
  title={InstantID: Zero-shot Identity-Preserving Generation in Seconds},
  author={Wang, Qixun and Bai, Xu and Wang, Haofan and Qin, Zekui and Chen, Anthony},
  journal={arXiv preprint arXiv:2401.07519},
  year={2024}
}
```

For any question, please feel free to contact us via haofanwang.ai@gmail.com or wangqixun.ai@gmail.com.
