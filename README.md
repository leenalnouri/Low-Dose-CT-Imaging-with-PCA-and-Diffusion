This repositry contains code from my MSc thesis project, "Opportunities And Challenges In Low Dose CT Imaging: A PCA Based Latent Diffusion Approach".

<b> Abstract </b>

<p align="justify">
  Computed Tomography (CT) imaging is widely used in the clinic for numerous
  applications like disease screening scans for cancer, lung nodules or internal bleedings,
  routine exams of bone or head injuries, and radiotherapy planning. However, radiation
  exposure of patients during CT examinations is a major concern; it poses the potential
  risk of causing cancer with repeated scan sessions. Current state-of-the-art denoising
  methods are based on diffusion models, which require extensive training time. To
  address this limitation, this study proposes the integration of Principal Component
  Analysis (PCA)-based latent space representations into a diffusion model for low-dose
  CT denoising, aiming to reduce data dimensionality, computational cost and model
  complexity.
</p>
<p align="justify">
  Block-wise PCA transformation was applied during preprocessing using an 8×8
  block size, fitted on high-dose training data. All image data was then transformed using
  this same PCA model. The compressed low-dose images were fed as input to a
  framework based on the CoreDiff model to perform denoising in the transformed space.
  The proposed diffusion model employed Mean-squared Error (MSE) loss and utilized a
  lightweight 2-layer U-Net, and the output predictions were reconstructed back to the
  pixel domain using reverse PCA. Post-processing filters were explored to mitigate edge
  artifacts introduced by the PCA reshaping process. Additionally, the method was tested
  on the Residual Encoder-Decoder Convolutional Neural Network (RED-CNN) model,
  where it significantly reduced training time. The approach was evaluated on two publicly
  available datasets, demonstrating generalizable denoising performance with reduced
  computational cost. Results indicate that PCA is a viable option for accelerating low-
  dose CT denoising using diffusion model frameworks, without notably sacrificing
  performance.
</p>
<p align="center">
  <img width="712" height="412" alt="image" src="https://github.com/user-attachments/assets/bb305d62-552b-4be1-b67a-4de9698a2118" />
  <img width="546" height="263" alt="image" src="https://github.com/user-attachments/assets/7c2f9dcb-eea2-46f8-9934-8658d4803225" />
  <img width="712" height="438" alt="image" src="https://github.com/user-attachments/assets/073ed4ba-17e4-45d3-992b-0cf6442c3483" />
  <img width="556" height="345" alt="image" src="https://github.com/user-attachments/assets/a783432b-bb3a-4bd2-893e-5e9520506fbf" />
</p>
