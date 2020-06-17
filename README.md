Unsupervised Translator Using UNdreaMT
==============

This is an implementation of an unsupervised neural machine translator using the aproach originally proposed by Artetxe et al. (2018). 
The original paper can be found in

Mikel Artetxe, Gorka Labaka, Eneko Agirre, and Kyunghyun Cho. 2018. **[Unsupervised Neural Machine Translation](https://arxiv.org/pdf/1710.11041.pdf)**. In *Proceedings of the Sixth International Conference on Learning Representations (ICLR 2018)*.

and their project is available in their Github **[UNdreaMT: Unsupervised Neural Machine Translation](https://github.com/artetxem/undreamt)**


The implementation here presented was tested using a corpus composed of texts in brazilian portuguese in the e-commerce domain. The full paper, in .pdf and in portuguese, is present in the project by the name **Tradução Automática Neural inglês-português no domínio do E-Commerce**


Requirements
--------
- Python 3
- PyTorch (tested with v0.3)


Usage
--------
As this project uses UNdreaMT, the usage is essentially the same. The resulting models created by UNdreaMT are in the folder named *Models*, and UNdreaMT itself is in the folder named *undreamt-master*.

The following command uses the model trained to translate from english to portuguese in the input given:

```
python3 undreamt-master/translate.py Models/MODEL_PARALELO_100k_iter.final.trg2src.pth < INPUT.txt > OUTPUT.txt

```
**NOTE** The Models were trained using CUDA. Due to this fact, it seems that the *translate.py* script uses it as well. It is suggested that you use the same PyTorch version used by UNdreaMT


For more details and additional options, refer to the original paper or github. Or run the above script with the `--help` flag.
