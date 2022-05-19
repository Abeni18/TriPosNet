# TriPosNet
Repository for the paper "TriPosNet"
## Abstract
Most object detection research focuses on identifying a large object covering a substantial part of the image, while small object detection is often overlooked. Small objects are difficult to detect since they contain few pixels and cover a small portion of the picture. We propose TriPoslNet, a key-point based object detection framework that employs a novel key-point encoder and attention mechanism to enhance the small object detection performance. The key-point encoder addresses the representational imbalance between small and big objects by effectively encoding object information in a heatmap representation. The attention mechanism enables the detector to adaptively change the receptive field in order to capture and emphasize small object features on low-resolution representation of the extracted features. To further improve the performance, we developed a fusion module to combine predictions from several output levels of the backbone architecture. Using our suggested method, we achieve state-of-the-art performance on both the UDETRAC and the UAVDT benchmark dataset, which consists primarily of small objects. For further information, visit.

## Model


# Results

\begin{table*}[h] 
% \scriptsize
\small
\centering
\unboldmath
\captionsetup{font=small}
% \textup{Sample Text 0123}
\caption{Comparison with various models on UA-Detrac datasets. Results for TriPosNet and other state-of-the-art detectors are generated using the official toolkit from the UA-DETRAC website. Boldface
indicates the our approach result.}
\setlength{\tabcolsep}{10pt} % Default value: 6pt
\renewcommand{\arraystretch}{1.2} % Default value: 1
\begin{tabular}{p{2.95cm} p{1.15cm}p{1.15cm}p{1.15cm}p{1.15cm}p{1.15cm}p{1.15cm}p{1.15cm}p{1.15cm}}
\Xhline{.2pt}
Model & Overall & Easy & Medium & Hard & Cloudy & Night & Rainy & Sunny   \\ 
 \hline \hline
     \textbf{TriPosNet} & \textbf{88.43\%} &	\textbf{97.83}\% &	\textbf{93.12\%} &	\textbf{79.81\%} &	\textbf{91.37\%} &	\textbf{90.29\%} &	\textbf{83.24\%} &	\textbf{91.32\%} \\ 
    \hline
    % \textbf{TriPosNet (ours)} & \textbf{88.09\%} &	\textbf{97.88}\% &	\textbf{92.55\%} &	\textbf{79.63\%} &	\textbf{91.33\%} &	\textbf{89.64\%} &	\textbf{82.58\%} &	\textbf{91.78\%} \\ 
    % \hline
    
%     \textbf{TriPosNet\scriptsize{-max }} & \textbf{87.75\%} &	\textbf{97.75}\% &	\textbf{92.17\%} &	\textbf{79.20\%} &	\textbf{91.37\%} &	\textbf{89.09\%} &	\textbf{81.90\%} &	\textbf{91.69\%} \\ 
% \hline
%     \textbf{TriPosNet \scriptsize{}} & \textbf{87.28\%} &	\textbf{97.80}\% &	\textbf{92.50\%} &	\textbf{77.66\%} &	\textbf{90.69\%} &	\textbf{89.34\%} &	\textbf{81.15\%} &	\textbf{91.37\%} \\ 
%     \hline
    \hline
    SpotNet \cite{perreault2020spotnet} & 86.80\% &	97.58\% &	92.57\% &	76.58\% &	89.38\% &	89.53\% &	80.93\% &	91.42\% \\ 
    \hline
    SSD-VDIG \cite{} & 82.68\% &	94.60\% &	89.71\% &	70.65\% &	89.81\% &	83.02\% &	73.35\% &	88.11\%  \\ 
    \hline
    ME-Net \cite{} & 80.76\% &	94.56\% &	85.90\% &	69.72\% &	87.19\% &	80.68\% &	71.06\% &	89.74\%  \\
    \hline
    HAVD \cite{} & 80.51\% &	94.48\% &	86.13\% &	69.02\% &	87.28\% &	82.30\% &	69.37\% &	89.71\%  \\ 
    \hline
        FG-BR Net \cite{fu2019foreground} & 79.96\% & 93.49\% & 83.60\% & 70.78\% & 87.36\% & 78.42\% & 70.50\% & 89.8\% \\
        \hline
            HAT  \cite{wu2019hierarchical}&  78.64\% & 93.44\% & 83.09\% & 68.04\% & 86.27\% & 78.00\% & 67.97\% & 88.78\%  \\ 
            \hline 
    GP-FRCNNm  \cite{amin2017geometric}& 77.96\% & 92.74\% & 82.39\% & 67.22\% & 83.23\% & 77.75\% & 70.17\% & 86.56\% \\
    \hline
    R-FCN  \cite{dai2016r} &  69.87\% & 93.32\% & 75.67\% & 54.31\% & 74.38\% & 75.09\% & 56.21\% & 84.08\%  \\  
    \hline
    EB  \cite{wang2017evolving} &  67.96\% & 89.65\% & 73.12\% & 53.64\% & 72.42\% & 73.93\% & 53.40\% & 83.73\% \\
    \hline
    Faster R-CNN  \cite{ren2015faster} &  58.45\% & 82.75\% & 63.05\% & 44.25\% & 66.29\% & 69.85\% & 45.16\% & 62.34\%  \\
    \hline
    YOLOv2  \cite{redmon2017yolo9000} &  57.72\% & 83.28\% & 62.25\% & 42.44\% & 57.97\% & 64.53\% & 47.84\% & 69.75\%  \\ 
    \hline 
    RN-D  \cite{perreault2019road}&  54.69\% & 80.98\% & 59.13\% & 39.23\% & 59.88\% & 54.62\% & 41.11\% & 77.53\%  \\ 
    \hline
    3D-DETnet  \cite{li20183d} & 53.30\% & 66.66\% & 59.26\% & 43.22\% & 63.30\% & 52.90\% & 44.27\% & 71.26\%  \\  
    \hline
    CompACT \cite{cai2015learning} &	53.23\% &	64.84\% &	58.70\% &	43.16\% &	63.23\% &	46.37\% &	44.21\% &	71.16\%   \\  
    \hline
    R-CNN \cite{girshick2014rich}&	48.95\% &	59.31\% &	54.06\% &	39.47\% &	59.73\% &	39.32\% &	39.06\% &	67.52\%  \\  
    \hline
    ACF \cite{dollar2014fast}&	46.35\% &	54.27\% &	51.52\% &	38.07\% &	58.30\% &	35.29\% &	37.09\% &	66.58\%  \\  
    \hline
    SA-FRCNN \cite{Lu_Zonglei2021sa} &	45.83\% &	73.93\% &	49.00\% &	30.76\% &	49.97\% &	52.30\% &	33.39\% &	55.04\%  \\  
    \hline
    DPM \cite{felzenszwalb2009object}	& 25.70\% &	34.42\% &	30.29\% &	17.62\% &	24.78\% &	30.91\% &	25.55\% & 31.77 \% \\  
    \hline
    
 %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
             \Xhline{.2pt}
        % \Xhline{2pt}
%  ####################################################################################
      \end{tabular}
\label{tab:classification_Cifar_100}
\end{table*}
