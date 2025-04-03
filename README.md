# Learning-Parameters-in-Gabor-Convolutional-Networks
Master Thesis at UZH

Before the deep learning era, image processing was often performed with Gabor wavelets [Lee, 1996], mostly
in terms of face recognition [Wiskott et al., 1997, Zhang et al., 2005, Gunther et al., 2012, Serrano et al., 2010],
because they are related with the functioning of the human brain. While much research was only treating Gabor
wavelets as pre-processing for follow-up tasks [Zhang et al., 2005], we also have learned important understanding
on how to make use of local texture features [Wiskott et al., 1997, Gunther, 2012].
Most of the previous knowledge came out of favor when deep learning and convolutional neural net
works revolutionized image processing. Instead of using a xed set of kernels, as represented by Gabor
wavelets, convolutional kernels are nowadays learned end-to-end [Krizhevsky et al., 2012] by adapting to the
input data. Interestingly, it was shown that these lters automatically learn structures that represent Ga
bor lters [Krizhevsky et al., 2012], at least partially. Since Gabor lters are typically large (more than
100 100 pixels), for a long time, Gabor lters were not considered in image processing tasks. Only a few
and very limited approaches have been made to replace or augment rst convolutional lters with Gabor l
ters [Luan et al., 2018, Alekseev and Bobe, 2019, Rai and Rivas, 2020], but these approaches have not used the
complete representational power of Gabor wavelets.
Interestingly, when applying the Gabor lters in frequency domain [Gunther, 2012], processing time can be
greatly reduced. Recently, a Master project [Duan and Wu, 2024] implemented Gabor wavelet processing in
frequency domain using PyTorch [Paszke et al., 2019], which allows including Gabor lters just as a regular
network layer including backpropagation capabilities. First experiments with this toolbox have been done
[Kung, 2024], from which we have learned a few lessons.
The goal of this Master thesis is to utilize this implementation to exploit Gabor wavelet processing for
image processing tasks, such as ImageNet classi cation [Russakovsky et al., 2015]. Later, the toolbox should
be extended to make the parameters of the Gabor wavelets learnable, and to include color information in a
structured way. It should be tested whether the learned parameters re ect what has been found in mammals
[Jones and Palmer, 1987], and how this di ers between di erent training datasets such as ImageNet, Fruits and
Vegetables, or alike. Possibly, non-linearity that mimics brain processing can be applied [Gunther, 2012], so
that magnitudes and Gabor phases [Gunther et al., 2012] can be exploited. Also, the use of attention blocks
specialized to the inner workings of Gabor wavelets can be explored.
