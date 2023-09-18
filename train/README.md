

### File Structure

```bash
├── data                                
|    ├── WTS                            # site name
|        ├── beacons.csv                # beacon coordinates in meters
|        ├── point_1.csv                # collected data with rssi and beacon id (column 'anchor')
|        ├── point_1_gt.txt             # the coordinate where the data is collected
|        ├── point_2.csv              
|        ├── point_2_gt.txt           
├── src
|    ├── train.ipynb                    # training code
```

*** data structure *** 
```
beacons.csv: pandas.DataFrame
    column 'anchor': beacon id
    columns [0, 1]: coordinates in meters
    each row represents a beacon
point_<n>.csv: pandas.DataFrame with columns
    column 'anchor': beacon id, 
    column 'rssi': received signal strength indicator
    each row represents a signal
point_<n>_gt.txt: 2-D tuple
    coordinate (<x>,<y>) where the data point_<n> was collected
```

### Package Version
| Package | Version |
| :----- | :------ |
| Python | 3.11.0  |
| Numpy  | 1.23.5 |
| Pandas | 1.5.2  |
| Matplotlib | 3.6.2 |


### Entry
```src/train.ipynb```
