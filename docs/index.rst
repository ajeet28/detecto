.. Detecto documentation master file, created by
   sphinx-quickstart on Thu Dec 26 16:43:20 2019.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to Detecto's documentation!
===================================

Detecto is a simple, easy-to-use object detection package for Python. You can
train your own object detection model and run your predictions on a video with
less than ten lines of code::

   from detecto.core import Model, Dataset, DataLoader
   from detecto.utils import xml_to_csv
   from detecto.visualize import detect_video

   xml_to_csv('xml_labels/', 'labels.csv')
   dataset = Dataset('labels.csv', 'images/')
   loader = DataLoader(dataset)

   model = Model(['dog', 'cat', 'rabbit'])
   model.fit(loader)

   detect_video(model, 'input_video.mp4', 'output_video.avi')

See the guides below to get started:

.. toctree::
   :maxdepth: 2

   usage/quickstart
   usage/further-usage


API Documentation
=================

.. toctree::
   :maxdepth: 2

   api


Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`