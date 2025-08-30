# Masked Feature Residual Coding for Neural Video Compression
In neural video compression, an approximation of the target frame is predicted, and a mask is subsequently applied to it. Then, the masked predicted frame is subtracted from the target frame and fed into the encoder along with the conditional information. However, this structure has two limitations. First, in the pixel domain, even if the mask is perfectly predicted, the residuals cannot be significantly reduced. Second, reconstructed features with abundant temporal context information cannot be used as references for compressing the next frame. To address these problems, we propose Conditional Masked Feature Residual (CMFR) Coding. We extract features from the target frame and the predicted features using neural networks. Then, we predict the mask and subtract the masked predicted features from the target features. Thereafter, the difference is fed into the encoder with the conditional information. Moreover, to more effectively remove conditional information from the target frame, we introduce a Scaled Feature Fusion (SFF) module. In addition, we introduce a Motion Refiner to enhance the quality of the decoded optical flow. Experimental results show that our model achieves an 11.76% bit saving over the model without the proposed methods, averaged over all HEVC test sequences, demonstrating the effectiveness of the proposed methods.



## MS-SSIM metric results correction
![ms_ssim_correction](MSSSIM_values.png)


We found an error in our MS-SSIM measurement process and confirmed that incorrect values were reported in the original paper. The table above presents the corrected performance results after re-evaluating the MS-SSIM scores accurately.
As shown in the table of the updated results, our model achieves still outperforms DCVC-DC model. Furthermore, our model demonstrates higher performance on the MCL-JCV dataset, indicating better results across a various test datasets than initially reported in the paper.
