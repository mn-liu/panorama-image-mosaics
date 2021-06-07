# panorama-image-mosaics
对20张图片的全景拼接
首先采用宋然老师的《Auto-sorting scheme for image ordering applications in image mosaicing》论文中的方法进行排序。
  1.对前一次生成的全景图取大小生成同样大小的黑色背景，将待排序的图片放到背景中 
  2.对所有图像进行傅里叶-梅林变换后，对峰值排序，将最大值的图像作为下次要拼接的图像
然后采用SURF算法提取特征点，先两两进行拼接，拼接后将新的图作为下次待拼接的图片之一
最后可以完成20张图片的拼接
