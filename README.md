# Pediatric Cardiac MRI of Patients with Complex Congenital Heart Diseases

## Dataset
Our dataset includes 64 CMR studies from pediatric patients with an age range of 2 to 18 scanned at the Children’s Hospital Los Angeles (CHLA). The CMR dataset–as provided–consists of Tetralogy of Fallot (TOF; n = 20), Double Outlet Right Ventricle (DORV; n = 9), Transposition of the Great Arteries (TGA; n = 9), Cardiomyopathy (n = 8), Coronary Artery Anomaly (CAA; n = 9), Pulmonary Stenosis or Atresia (n = 4), Truncus Arteriosus (n = 3), and Aortic Arch Anomaly (n = 2). The study was reviewed by the Children’s Hospital Los Angeles Institutional Review Board and was granted an exemption per 45 CFR 46.104[d][4][iii] and a waiver of HIPAA authorization per the Privacy Rule (45 CFR Part 160 and Subparts A and E of Part 164).

## CMR Studies

Imaging studies were performed on either a 1.5 Tesla Philips Achieva or a 3.0 Tesla Philips Ingenia scanner (Philips Healthcare, Best, Netherlands). CMR images for ventricular volume and function analysis were obtained using a standard balanced steady state free precession (SSFP) sequence without the use of a contrast agent. Each dataset includes 12 − 15 short-axis slices encompassing both right and left ventricles from base to apex with 20 − 30 frames per cardiac cycle. Typical scan parameters were: slice thickness of 6 − 10mm, in-plane spatial resolution of 1.5 − 2mm^2 , repetition time of 3 − 4ms, echo time of 1.5 − 2ms, and flip angle of 60 degrees. Manual image segmentation was performed by a pediatric cardiologist with expertise in cardiac MRI. Endocardial contours were drawn on end-diastolic and end-systolic images. 


## Post-Processing of CMR Data

Each image’s original size and its corresponding segmentation was 512 × 512 pixels. The original dataset was first preprocessed by center cropping each image to the size 445 × 445, after removing patients’ information and anonymizing the data. To reduce the dimensionality, each cropped image was subsequently resized to 128 × 128 using the imresize function in the open-source Python library SciPy. The entire process was performed using two different down-sampling methods: (1) nearest-neighbor down-sampling and (2) bi-cubical down-sampling. For training data, twenty-six patients (10 TOFs, 4 DORVs, 4 TGAs, 4 CAAs and 4 patients with cardiomyopathy) were selected whereas the remaining 38 patients were used as test data.

## Training and Test Subjects

The index of training and test subjects are provided below:

| Dataset | Subject Index |
| --- | --- |
| `Training` | 1, 3, 4, 5, 6, 7, 8, 9, 10, 12, 14, 15, 16, 24, 25, 28, 29, 31, 34, 39, 52, 53, 57, 58, 62, 63 |
| `Test` | 2, 11, 13, 17, 18, 19, 20, 21, 22, 23, 26, 27, 30, 32, 33, 35, 36, 37, 38, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 54, 55, 56, 59, 60, 61, 64 |


## Acknowledgments

The authors wish to thank all participants and staff in this study that was carried out in part at the Children’s Hospital Los Angeles.
