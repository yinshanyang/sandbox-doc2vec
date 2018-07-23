# `sandbox-doc2vec`

## Setup

```bash
# install dependencies
conda env create --file environment.yml
source activate doc2vec

# train some models
./train INPUT OUTPUT_MODEL OUTPUT_VECTORS
```

## `train`

```
usage: train [-h] [-e EPOCHS] [-d DIMENSIONS] [-a ALPHA] [--decay DECAY]
             INPUT OUTPUT

doc2vec model trainer

positional arguments:
  INPUT                 source file, list of newline-delimited sentences or
                        phrases, e.g. sentences.csv
  OUTPUT                output path, e.g. model.d2v

optional arguments:
  -h, --help            show this help message and exit
  -e EPOCHS, --epochs EPOCHS
                        number of epochs to train the model (default: 100)
  -d DIMENSIONS, --output_dimensions DIMENSIONS
                        number of output dimensions to embed (default: 300)
  -a ALPHA, --alpha ALPHA
                        learning rate (default: 0.025)
  --decay DECAY         decay to the learning rate (default: 0.0002)
```

### Input (Sentences or Phrases)

> note: a simple newline-delimited list of sentences or phrases to train with, there’s no need for quoting

```
Camera is not upto mark
Finger print sensor is pathetic
always hang
...
Over heating problem
Amazon service is best but xiaomi not
Many required features are not available which are commonly found in other competitive phone like Coolpad
```

### Output Model (doc2vec Model)

```
it’s a model
```

### Output Vectors (doc2vec Embeddings)

```
*dt_0 -0.0032 -0.0722  0.0054 ... -0.0151 -0.0035 -0.0059
*dt_1  0.0089 -0.0051  0.0078 ... -0.0107 -0.0224 -0.0012
*dt_2  0.005  -0.0114  0.015  ... -0.0015 -0.0138 -0.016
 ...
*dt_7 -0.0008 -0.0075 -0.0023 ... -0.0054 -0.0123 -0.0103
*dt_8  0.0015 -0.008  -0.008  ...  0.0072 -0.0123  0.0033
*dt_9  0.0007 -0.0098  0.0038 ...  0.008  -0.011  -0.0024
```
