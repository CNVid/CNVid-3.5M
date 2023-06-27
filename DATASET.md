## DATASET
The CNVid-3.5M dataset is a large-scale video-text Chinese dataset.

## Download
Download link is now available：[https://drive.google.com/drive/folders/1ACVN2Zb_XoY5IpMrkfbKqEIJfhleMSDO?usp=share_link](https://drive.google.com/drive/folders/1ACVN2Zb_XoY5IpMrkfbKqEIJfhleMSDO?usp=share_link)
We provide the following files:
####CSVs:

----HowTo100M_v1.csv----: 
This CSV contains all of the HowTo100M YouTube video urls.
Column description: 
    --video_id: YouTube video id
    --task_id: task id (see task_ids.csv for more details)
    --rank: YouTube search result rank of the video when querying the task
    --category_1: Highest level task category from WikiHow
    --category_2: Second Highest level task category from WikiHow

----task_ids.csv----:
This CSV contains the mapping between the task_id and the task description / name
we have scrapped from WikiHow.

####JSON:

----caption.json----:
This json file contains the captions for all the HowTo100M videos.
It is stored as a dictionary where each key is a video_id.
Each value of the dictionary is another dictionary with the keys ['text', 'start', 'end']
where the value of 'text' is a list of all the captions from the given video_id,
and 'start' and 'end' are arrays correspondings to the start and end time timestamp of the captions
(in second).

Note that the narrated captions have been processed.
In fact, we have removed a significant number of stop words
which are not relevant for the learning of the text-video joint embedding.
The list of stop words can be found here: https://github.com/antoine77340/howto100m/blob/master/stop_words.py

You can find the unprocessed caption file (i.e. with stop words) here: https://www.rocq.inria.fr/cluster-willow/amiech/howto100m/raw_caption.zip


## Statistics
* The CNVid-3.5M dataset contains **3.5 Million** <video, text> pairs.
* **Topics:**  CNVid-3.5M contains a total of 5.7 Million topics,
and each video has 1.63 topics on average.
* **Keywords:**  CNVid-3.5M contains a total of 21.5 Million keywords, and each video has 6.15 keywords on average.
* **Video Durations:** The maximum, minimum, and average video duration of CNVid-3.5M is 1,974s, 4s, and 36.34s, respectively.
* **PoS Tags of the ASR Text:** CNVid-3.5M contains a total of 17.0 Million verbs, 9.1 Million nouns, and 3.2Million adjectives, respectively.
