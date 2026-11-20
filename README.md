# OWL Dataset

**An outdoor RGB-thermal dataset for low-light image enhancement.**

OWL is introduced in **TGSE-Net: Thermal-Guided Structure-aware Network for Low-Light Image Enhancement**. It contains 428 geometrically registered image triplets, each consisting of a low-light RGB image, a normal-exposure RGB reference image, and a corresponding thermal infrared image.

This page provides an overview of the dataset, representative samples, and information on data availability.

## Dataset Overview

| Property | Description |
| --- | --- |
| Task | RGB-thermal low-light image enhancement |
| Total samples | 428 image triplets |
| Images per triplet | Low-light RGB, normal-exposure RGB reference, and thermal infrared |
| Processed resolution | 640 × 480 pixels |
| Acquisition periods | 304 daytime, 29 dusk, and 95 nighttime triplets |
| Scene coverage | Primarily outdoor campus environments, with some additional off-campus scenes |

The dataset includes buildings, roads, vehicles, trees, and open outdoor areas. The acquisition-period categories describe when the images were captured; low-light RGB inputs were obtained through camera exposure control across these periods.

## Representative Samples

![Four representative OWL triplets, with reference RGB images in the top row, low-light RGB images in the middle row, and thermal images in the bottom row.](assets/owl_samples.png)

Each column shows one image triplet. The rows labeled **Target**, **Low**, and **Thermal** correspond to normal-exposure RGB reference images, low-light RGB inputs, and paired thermal images, respectively.

## Image Acquisition and Registration

OWL was collected using an RGB camera and a PLUG617R thermal imager. A reference RGB image and its corresponding thermal image were acquired first, followed by a low-light RGB image captured by adjusting the RGB camera's exposure time and sensor gain while keeping the cameras fixed. Triplets were acquired individually rather than extracted from continuous video.

The processing pipeline includes camera calibration, distortion correction, cropping, resampling, and geometric registration. Thermal images were mapped to the reference RGB coordinate system using XoFTR feature matching and a homography transformation. All processed images have a resolution of 640 × 480 pixels. Residual cross-modal misalignment may remain after registration.

## Dataset Scope and Limitations

OWL has limited scene and device coverage, with most samples collected in outdoor campus environments and during daytime. Its coverage should not be taken to represent the full range of real-world nighttime conditions. The reference RGB images retain the camera's normal-exposure output characteristics and are not absolute color ground truth established through colorimetric calibration.

## Data Availability

The complete OWL dataset is not yet publicly available. As it contains images of campus buildings and related scenes, we are currently seeking authorization from the relevant university offices for its public release. Once authorization is granted, we will provide a download link on this page.

## Contact

For inquiries about OWL, please contact **Nan Duan** at [duannanyoujian@163.com](mailto:duannanyoujian@163.com).
