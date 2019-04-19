自动对焦
============
本报告提出了一种基于块反差的对焦值计算方法，并且表现出了较高的鲁棒性，特别是对于纹理不是很丰富，且噪声较严重的场景下也有不错的表现。相对于传统算法计算纹理，
对于有噪声的场景需要先进行滤波，在高 ISO 条件下为了减少噪声，一些滤波算法可能导致边缘被抹掉，导致边缘不是很明显，使用联合双边滤波或导向滤波等虽然能保证边缘，但是
大大增加了计算量，而频域的计算方式需要 FFT，计算代价也不低，本报告提出的方法，相对而言有较低的计算复杂度 O(n)，根据数据分析效果也可以接受，适合在嵌入式设备上运
行。至于爬山算法的应用则依赖于设备具体参数，需要根据设备进行优化。 