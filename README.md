# CS7180
Project for CS7180: Advanced Computer Vision. 'Siamese Networks for Domain Adaptation'

The project contains two train files: train.py and train_duets.py. train.py can be used to run the code with tirplet and quadruplet loss. train_duets.py can be used to run the code with duet, kl-div and NT-Xent loss.

Triplet/Quadruplet Loss:

python train.py --task [TASK_NAME] --source_domain [SOURCE_DOMAIN] --target_domain [TARGET_DOMAIN] --loss [LOSS] --samples_per_class [SAMPLES_PER_CLASS]

Duet/ kl-div / NT-Xent Loss:

python train_duets.py --task [TASK_NAME] --source_domain [SOURCE_DOMAIN] --target_domain [TARGET_DOMAIN] --loss [LOSS] --samples_per_class [SAMPLES_PER_CLASS]

TASK_NAME: 'digit' or 'office'

SOURCE_DOMAIN: if task is digit: 'MNIST' or 'USPS'; if task is office: 'amazon', 'dslr' or 'webcam'

TARGET_DOMAIN: if task is digit: 'MNIST' or 'USPS'; if task is office: 'amazon', 'dslr' or 'webcam'

LOSS: for train.py - 'triplet' or 'quadruplet'; for train_duets.py - 'duet', 'kld' or 'ntxent'

SAMPLES_PER_CLASS: number of samples to use from target domain per class

The experiments for 'digit' were done using samples_per_class = 1,2,4 or 6 and for 'office' samples_per_class = 4.

Have Fun!!
