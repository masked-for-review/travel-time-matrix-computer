# Compute travel time matrices

This is a Python package to handle the high-level logic of computing travel time
matrices for multiple travel modes using [`r5py`](https://r5py.readthedocs.io/).

This package is used, for instance, for [calculating travel time matrices of the
Helsinki metropolitan
area](https://github.com/masked-for-review/helsinki-ttm-sdata-2024) (in
a Docker container), but can be used by itself, as well.


## Installation

```
pip install git+https://github.com/masked-for-review/travel-time-matrix-computer.git
```


## Use

Create a `data` directory, within that a config file according to the template
provided in `travel_time_matrix_computer.yml.example`, and pass it to `python
-m travel_time_matrix_computer`


## Dependencies

This package depends on [r5py](https://r5py.readthedocs.io/),
[car_speed_annotator](https://github.com/masked-for-review/car-speed-annotator),
[cycling_speed_annotator](https://github.com/masked-for-review/cycling-speed-annotator),
and
[parking_times_calculator](https://github.com/masked-for-review/parking-times-calculator),
as well as all dependencies listed there (i.e., a Java JRE and
[`osmium`](https://docs.osmcode.org/pyosmium/latest/ref_osmium.html), which is
available as a package for most Linux distributions: e.g., `osmium-tool` on
Ubuntu and Arch). 

Output data aggregation and packing can be sped up by installing the optional
dependency `7za` (available as `p7zip` on Ubuntu, Arch, and most likely most
Linux distributions)
