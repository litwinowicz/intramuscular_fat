## Usage

```bash
python fat_dixon.py \
  --fat <path_to_fat.nii> \
  --water <path_to_water.nii> \
  --segmentation <path_to_segmentation.nii> \
  --output <output_threshold.nii> \
  --fat-fraction <output_fat_fraction.nii> \
  --stats <output_stats.json> \
  --threshold 80
```

### Arguments

- `--fat`: Path to fat NIfTI file
- `--water`: Path to water NIfTI file
- `--segmentation`: Path to segmentation mask NIfTI file
- `--output`: Output path for thresholded image
- `--fat-fraction`: Output path for fat fraction image
- `--stats`: Output path for statistics JSON file
- `--threshold`: Threshold value for fat classification (default: 80)

## Output

The script generates three outputs:
1. Thresholded image (NIfTI) with values:
   - 0: Background/non-segmented
   - 1: Muscle (below threshold)
   - 2: Fat (above threshold)
2. Fat fraction image (NIfTI)
3. JSON file with statistics:
   - Mean fat fraction
   - Median fat fraction
   - Standard deviation of fat fraction
