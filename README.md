# `sandbox-doc2vec`

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

### Output (doc2vec Model)

```
it’s a model
```
