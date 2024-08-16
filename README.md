<div align="center">
<h1>An Element is Worth a Thousand Words: Enhancing Legal Case Retrieval by Incorporating Legal Elements[<a href="https://aclanthology.org/2024.findings-acl.139/">Paper</a>]</h1>
</div>

## Released Resources
The LeCaRD-Elem dataset can be downloaded via:
```shell
# Download dataset from huggingface link
wget https://huggingface.co/datasets/ChenlongDeng/LeCaRD-Elem/resolve/main/LeCaRD-Elem.zip?download=true

# unzip the zip file
unzip LeCaRD-Elem.zip
```

## Data Structure
The data structure in the above link is presented as:
```
LeCaRD-Elem
├── candidates.json     # the annotated candidate cases
├── label_system.xlsx   # the element label taxonomy of our LeCaRD-Elem
└── querys.json         # the annotated query cases
```
`querys.json` contains 107 query cases, while `candidates.json` contains 9088 candidate cases. You can load them in Python using `json.load()` function.

## Usage

### querys.json
`querys.json` contains the follwing fields:
<pre style="white-space: pre-wrap;"><code class="language-python">
{
    "path": "the path field copied from the original LeCaRD dataset",
    "ridx": "the query id for each case",
    "q": "the detailed case decription whose content is split into sentences. the key-value pair of this field denotes sentence index and its corresponding content, respectively",
    "crime": "the crime list provided in the original LeCaRD dataset",
    "element": "the annotated elements for this case. `ajjbqk_reference` field under each element denotes the sentence indexes to support this element"
}
</code></pre>


### candidates.json

### label_system.xlsx

## Citation
```
@inproceedings{deng-etal-2024-element,
    title = "An Element is Worth a Thousand Words: Enhancing Legal Case Retrieval by Incorporating Legal Elements",
    author = "Deng, Chenlong  and
      Dou, Zhicheng  and
      Zhou, Yujia  and
      Zhang, Peitian  and
      Mao, Kelong",
    editor = "Ku, Lun-Wei  and
      Martins, Andre  and
      Srikumar, Vivek",
    booktitle = "Findings of the Association for Computational Linguistics ACL 2024",
    month = aug,
    year = "2024",
    address = "Bangkok, Thailand and virtual meeting",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2024.findings-acl.139",
    pages = "2354--2365",
    abstract = "Legal case retrieval plays an important role in promoting judicial justice and fairness. One of its greatest challenges is that the definition of relevance goes far beyond the common semantic relevance as in ad-hoc retrieval. In this paper, we reveal that the legal elements, which typically comprise key facts in a specialized legal context, can largely improve the relevance matching of legal case retrieval. To facilitate the use of legal elements, we construct a Chinese legal element dataset called LeCaRD-Elem based on the widely-used LeCaRD dataset, through a two-stage semi-automatic method with a minimized reliance on human labor. Meanwhile, we introduce two new models to enhance legal search using legal elements. The first, Elem4LCR-E, is a two-stage model that explicitly predicts legal elements from texts and then leverages them for improved ranking. Recognizing the potential benefits of more seamless integration, we further propose an end-to-end model called Elem4LCR-I, which internalizes the legal element knowledge into its model parameters using a tailored teacher-student training framework. Extensive experiments underscore the significant value of legal elements and demonstrate the superiority of our two proposed models in enhancing legal search over existing methods.",
}
```

