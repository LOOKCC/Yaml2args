# Yaml to args
A Sample code for you to update your yaml config to args.
## Usage
You can use pip
```
pip install yaml2args==0.0.2
```
or just git clone this repository, even copy the code in ./yaml2args/tools.py to your code.
```
from yaml2args import yaml2args
import argparse

parser = argparse.ArgumentParser(description='PyTorch ImageNet Training')
parser.add_argument('-c', '--config', default='config.yaml', type=str, help='path to config file.')
parser.add_argument('--resume', default='', type=str, metavar='PATH',
                    help='path to latest checkpoint (default: none)')
parser.add_argument('-e', '--evaluate', dest='evaluate', action='store_true',
                    help='evaluate model on validation set')

args = parser.parse_args()
args = yaml2args(args.config, args)
print(args.xxx)
```
code in config.yaml:
```
xxx: "just for test"
```
You can also see example.py

