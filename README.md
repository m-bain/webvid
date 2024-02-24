# WebVid Dataset 🕸🎥
### [Project Page](https://www.robots.ox.ac.uk/~vgg/research/frozen-in-time/) | [Demo (Live Search)](http://meru.robots.ox.ac.uk/frozen-in-time/)

Large-scale text-video dataset, **containing 10 million video-text pairs** scraped from the stock footage sites. This dataset was used for large-scale pretraining to achieve state-of-the-art end-to-end retrieval in our frozen-in-time work: the code of which can be found [here](https://github.com/m-bain/frozen-in-time)

## ❌ DATASET NO LONGER AVAILABLE ❌

Due to a cease and desist request from the friendly Shutterstock.com <-🤡 . Webvid is no longer publicly available. I'm sorry. Apparently me providing urls + short captions infringes on their copyright, because people have been using it for non-commerical purposes.

If this hinders your academic research, please send your complaints to Shutterstock.com

Tip: There may or may not be alternative sources elsewhere on the internet if you look in the right places🤗, but these have no connection to me ;)

### video2dataset:
1. `pip install video2dataset`
2. Example downloading [script](https://github.com/iejMac/video2dataset/blob/main/examples/download_webvid.sh). video2dataset has many options for subsampling the input data (FPS, resolution, cut detection, optical flow, etc.) so this script can be greatly modified to enrich/standardize the output dataset.
3. Load into nicely batched tensors like [this](https://github.com/iejMac/video2dataset/blob/main/examples/dataloader_example.py)


## Download CLIP Features ⬇️

CLIP ViT-B/32 Features of this dataset, extracted at 1FPS are available to download at https://huggingface.co/datasets/iejMac/CLIP-WebVid, credit to [iejMac](https://www.github.com/iejMac). The pipeline for extracting clip features can be found here https://github.com/iejMac/clip-video-encode, see the example at the bottom of [this README](https://github.com/iejMac/clip-video-encode/tree/main/clip_video_encode/dataset).

N.B: CLIP features could be slightly biased / degraded due to the watermarks, which were not removed during extraction.


## Disclaimer ⚠️

We note that data sourced from the web may be prone to biases and may contain graphic content. Please be careful of unintended societal, gender, racial and other biases when training or deploying models trained on this data.


## Cite 📋

If you use this dataset in your research, please cite:


[Frozen in Time: A Joint Video and Image Encoder for End-to-End Retrieval](https://arxiv.org/abs/2104.00650)

Max Bain, Arsha Nagrani, Gül Varol, Andrew Zisserman.
```bibtex
@InProceedings{Bain21,
  author       = "Max Bain and Arsha Nagrani and G{\"u}l Varol and Andrew Zisserman",
  title        = "Frozen in Time: A Joint Video and Image Encoder for End-to-End Retrieval",
  booktitle    = "IEEE International Conference on Computer Vision",
  year         = "2021",
}
```


## FAQs 🙋

**Q1**: Can you provide the original videos for download?

**A1**: ~~Since we do not own the videos in the dataset, we cannot legally provide them to you. The video owner(s) can choose to delete it at anytime, in which case the video will no longer be available in the dataset. Due to this, unfortunately, some videos in the dataset will be lost over time, and we are unable to help with this issue. However, the sources are official and we expect the large majority of videos to be available for the forseeable future.~~ As of 23 Feb 2024, we cannot even provide the urls anymore.

###

**Q2**: Is it normal that a subset of videos cannot be retrieved from the provided URLs?

**A2**: ~~Yes. See Q1.~~ As of 23 Feb 2024, we cannot even provide the urls anymore.

###

**Q3**: I noticed there are watermarks on the videos, how will this affect training?

**A3**: We found we were still able to achieve top performance (with the watermarks) on downstream text-to-video retrieval, both for finetuning and zero-shot settings. We expect similar results on other video language tasks but didn't test these in the paper. If you do use this dataset for other video-language tasks, we'd be interested to hear how it goes.

## Contact Us

If you have a question not provided in the FAQs above, please create an issue in this repository. 

If you would like to share feedback or report concerns, please email me at maxbain@robots.ox.ac.uk
