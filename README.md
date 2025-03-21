# GEE Sentinel-2 Wildfire Monitoring

**University of California, Davis - Digital Agriculture Laboratory**  
**Authors:** Quynh Tran, Mohammadreza Narimani, Ali Moghimi, Alireza Pourreza

## Description

The **GEE Sentinel-2 Wildfire Monitoring** repository showcases a workflow for detecting and monitoring wildfires using Sentinel-2 imagery and Google Earth Engine (GEE). This project focuses on leveraging Sentinel-2’s spectral bands, particularly the Short-Wave Infrared (SWIR) range, to effectively identify and analyze active fire zones. By combining GEE’s extensive satellite archives with Python-based preprocessing and annotation techniques, this toolkit facilitates rapid data collection, cloud filtering, region-of-interest clipping, and creation of a robust dataset for wildfire segmentation models.

### Key Functionalities Include:
1. **ROI Selection & Cloud Filtering:** Dynamically define regions of interest and filter scenes by cloud coverage to ensure high-quality imagery.  
2. **False Color Composites (SWIR Visualization):** Highlight fire-affected areas by combining SWIR2, SWIR1, and Red bands for enhanced visibility of active fires.  
3. **Image Clipping & Export:** Clip and export selected images to Google Drive for offline analysis or deep learning model development.  
4. **Data Annotation Workflow:** Create annotated datasets (e.g., via Label Studio) for training wildfire segmentation algorithms.  
5. **Deep Learning Readiness:** Provide preprocessed, labeled images suitable for U-Net or other segmentation architectures to further research in automated wildfire detection.

This toolkit addresses the urgent need for efficient wildfire surveillance, particularly in fire-prone regions like California. By harnessing Sentinel-2’s five-day revisit frequency and its SWIR bands, researchers and practitioners can quickly monitor fire progression, assess damage, and support decision-making in disaster management.

## Explore the Code

To view the core Google Earth Engine script, check out the JavaScript file in this repository:

- [**Sentinel2_ROI_Download_B12_B11_B4.js**](Sentinel2_ROI_Download_B12_B11_B4.js)

This script demonstrates:
- Filtering Sentinel-2 images by date and location (ROI).  
- Sorting images by cloud coverage.  
- Visualizing SWIR-based false color composites.  
- Clipping and exporting selected images to Google Drive.

You can copy this script into the [Google Earth Engine Code Editor](https://code.earthengine.google.com/) to run it. Simply update the date range and region of interest as needed.

## Usage

1. **Clone or Download** this repository.  
2. **Open** the `Sentinel2_ROI_Download_B12_B11_B4.js` file in the [Google Earth Engine Code Editor](https://code.earthengine.google.com/).  
3. **Set** your desired date range, region of interest (ROI), and cloud coverage threshold.  
4. **Run** the script to visualize the false color composite.  
5. **Export** the clipped images to your Google Drive folder for further analysis or annotation.

## Conference Poster

Check out the poster of this work that was presented at the ESEARCH program of UC Davis in the spring of 2024. Click on the image below to view the full PDF:

[![ESEARCH Spring 2024 Poster Preview](UCDavis_ESEARCH_Spring_2024_Poster.png)](UCDavis_ESEARCH_Spring_2024_Poster.pdf)

## Future Work

- **Deep Learning Integration:** Implement and refine U-Net or similar segmentation architectures to detect fire pixels automatically.  
- **Hyperparameter Tuning:** Tailor model parameters for Sentinel-2 data, optimizing wildfire segmentation performance.  
- **Multi-Temporal Analysis:** Expand beyond single-event monitoring to track fire progression, burn severity, and post-fire recovery over time.  
- **Cross-Platform Comparison:** Compare Sentinel-2 results with data from other satellites (e.g., Landsat 8, MODIS) to enhance model robustness.

## Contact

For further information, collaborations, or questions, please contact:
- **Quynh Tran**: [pqtran@ucdavis.edu](mailto:pqtran@ucdavis.edu)  
- **Mohammadreza Narimani**: [mnarimani@ucdavis.edu](mailto:mnarimani@ucdavis.edu)  

For more information about our lab and other projects, please visit the [Digital Agriculture Lab](https://digitalag.ucdavis.edu/).

## References

1. OpenGeoEdu. (n.d.). **Sentinel-2 Teil 1**.  
   [https://learn.opengeoedu.de/en/fernerkundung/vorlesung/copernicus/Sentinel-2-Teil-1](https://learn.opengeoedu.de/en/fernerkundung/vorlesung/copernicus/Sentinel-2-Teil-1)

2. UP42. (n.d.). **Enhancing Sentinel-2 Images to Superresolution**.  
   [https://up42.com/blog/sentinel-2-superresolution](https://up42.com/blog/sentinel-2-superresolution)

3. de Almeida Pereira, G. H., Fusioka, A. M., Nassu, B. T., & Minetto, R. (2021). **Active fire detection in Landsat-8 imagery: A large-scale dataset and a deep-learning study**. *ISPRS Journal of Photogrammetry and Remote Sensing, 178*, 171-186.
