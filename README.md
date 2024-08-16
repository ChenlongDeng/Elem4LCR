# An Element is Worth a Thousand Words: Enhancing Legal Case Retrieval by Incorporating Legal Elements[<a herf="https://aclanthology.org/2024.findings-acl.139/">Paper</a>]


## Released Resources
The LeCaRD-Elem dataset can be downloaded via:
```shell
# Download dataset from huggingface link
wget https://huggingface.co/datasets/ChenlongDeng/LeCaRD-Elem/resolve/main/LeCaRD-Elem.zip?download=true

# unzip the zip file
unzip LeCaRD-Elem.zip
```

## Data Structure

## Usage

### querys.json

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

