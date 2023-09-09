
# 研究背景
在过去几十年中，线性正则变换（Linear Canonical Transform, LCT）因其在光学传播、时频分析和信号处理等领域中的重要性而备受关注。LCT是一种广义的积分变换，包括傅立叶变换、分数阶傅立叶变换、菲涅尔变换和洛伦兹变换等作为其特例。

Wigner分布（Wigner Distribution, WD）最初是在量子统计力学中定义的，后来在信号处理中发现了其广泛应用。WD是一种有效的时频分析工具，但在处理多分量信号时容易受到交叉项的干扰。它无法从强噪声背景中提取目标回波信号的主要特征，尤其在弱信号检测问题中表现不佳。

为了克服传统WD的限制，引入LCT的参数可以提高信号表示的灵活性。已经提出了多种参数嵌入技术，包括线性正则域自相关函数替换、线性正则域核替换、线性正则域卷积替换和线性正则域瞬时互相关函数替换等。这些技术将WD转化为具有更多自由度的变体，使其在信号表示和分析方面更加灵活。

过去的研究主要集中在基于闭型瞬时互相关函数型Wigner分布（CICFWD）的弱信号检测上，但是，CICFWD的参数选择不唯一，导致检测精度不稳定，并且计算复杂度高，不适合实时应用。因此，研究人员需要探索的参数较少的方法，比如，瞬时互相关函数型Wigner分布（ICFWD）。这正是本文主题所在，即建立数学模型限制ICFWD参数的选择，并通过数值仿真在检测精度和算法时间两个方面对比ICFWD与其他方法。

# 研究内容
本文的主要内容是研究弱信号检测问题，通过建立和求解基于瞬时互相关函数型Wigner分布（ICFWD）的输出信噪比不等式模型。具体而言，研究内容包括以下几个方面。

首先，本文定义了含有零均值加性高斯白噪声的显性信号在ICFWD下的基于期望的输出信噪比。这个定义为后续的研究提供了基础。

其次，本文建立了含噪信号的ICFWD与传统Wigner分布的输出信噪比期望不等式模型。通过比较不同方法的信噪比，我们可以评估ICFWD在弱信号检测中的性能优势。

然后，本文针对零期望平稳噪声背景下的单分量和双分量线性调频信号（LFM）分别推导了不等式模型的解。求解该不等式模型可以得到对应的信号检测结果，验证ICFWD在提取信号特征方面的效果。

最后，本文对比了ICFWD与其他变体Wigner分布方法（如CICFWD、ACWD、KFWD和CRWD）以及传统Wigner分布的检测精度和计算速度。这样的对比分析可以帮助我们了解不同方法之间的优缺点，为选择适用于实际应用的方法提供参考。

以上研究内容旨在揭示ICFWD在弱信号检测中的优势，并为实际应用中的信号处理和分析提供有益的研究结果。

# 有何实验
本研究进行了一系列数值实验来验证研究方法的有效性和性能优势。以下是实验的主要内容和目标：
1.  实验一：验证基于期望的不等式模型解  针对零期望平稳噪声背景下的单分量和双分量线性调频信号（LFM），我们推导了相应的不等式模型的解。在这个实验中，我们通过计算模型ICFWD的解并与传统WD的进行比较，来验证不等式模型的有效性和准确性。
2.  实验二：比较不同方法的检测精度  在这个实验中，本文对比了瞬时互相关函数型Wigner分布（ICFWD）与其他变体Wigner分布方法（如CICFWD、ACWD、KFWD和CRWD）以及传统Wigner分布（WD）的检测精度。本文使用了一组包含弱信号的信号样本，并通过计算它们在不同方法下的信噪比来评估每种方法的性能。实验的目标是验证ICFWD在弱信号检测中的优势。
3.  实验三：比较不同方法的计算速度  在这个实验中，我们比较了ICFWD、CICFWD、ACWD、KFWD和CRWD的计算速度。本文使用相同的信号样本，并测量每种方法的计算时间。对比不同方法的计算速度可以评估它们的实时应用性能。

通过这些实验，本文可以验证ICFWD在保持或提高检测精度的同时节省计算时间的优势，并验证不等式模型在解决弱信号检测问题上的适用性。这些实验结果将为研究方法的应用和进一步改进提供实证支持。

# 结果
- 检测精度：ICFWD $\approx$ CICFWD > ACWD $\approx$ KFWD $\approx$ CRWD > WD；
- 计算效率：KFWD > ICFWD $\approx$ ACWD > CICFWD $\approx$ CRWD.

在所有线性正则域WD中，ICFWD具有权衡检测精度和计算复杂度的显著优势。因此，本文研究了ICFWD在检测多分量弱LFM信号中的应用，建模和求解了ICFWD和WD之间基于期望的输出信噪比不等式，推导出了单分量和双分量情形下ICFWD的LCT自由参数选择方法，并且通过大量的数值实验证明了理论结果的正确性。结果表明，ICFWD的检测精度与CICFWD相近，优于ACWD、KFWD、CRWD和常规WD的检测精度。此外，ICFWD的计算效率与ACWD相当，在高计算效率上优于CICFWD和CRWD，但不如KFWD。

ICFWD可以被应用于多个领域，具有广泛的应用前景。在LFM信号处理领域中，ICFWD期望不等式模型是一种重要的技术手段，它可以被应用于海洋勘探、海洋监测、水声通信等领域；使用该模型可以提高信号的抗干扰和检测性能，从而实现在真实有噪声环境中目标的精确探测和定位。此外，在无线通信领域中，ICFWD期望不等式模型可以为无线通信系统的设计和优化提供一种新的思路和工具。ICFWD期望不等式模型可以帮助提高信道估计和均衡算法性能，总而实现更好的信号传输质量和数据传输速率。

# 参考文献
[1]      A. Yelashetty, N. Gupta, D. Dhirhe, and U. Gopinathan, “Linear canonical transform as a tool to analyze coherence properties of electromagnetic beams propagating in a quadratic phase system,” _J. Opt. Soc. Am. A_, vol. 37, no. 8, pp. 1350--1360, Aug. 2020.

[2]      S. C. Pei and J. J. Ding, “Relations between fractional operations and time-frequency distributions and their applications,” _IEEE Trans. Signal Process._, vol. 49, no. 8, pp. 1638--1655, Aug. 2001.

[3]      A. Stern, “Sampling of linear canonical transformed signals,” _Signal Process._, vol. 86, no. 7, pp. 1421--1425, Jul. 2006.

[4]      R. N. Bracewell, _The Fourier Transform and Its Applications._Boston, MA, USA: McGraw-Hill, 2000.

[5]      H. M. Ozaktas, M. A. Kutay, and Z. Zalevsky, _The Fractional Fourier Transform With Applications in Optics and Signal Processing._ New York, NY, USA: Wiley, 2001.

[6]      R. Tao, B. Deng, and Y. Wang, _Fractional Fourier Transform and Its Applications._ Beijing, China: Tisinghua Univ. Press, 2009.

[7]      J. Shi, Y. N. Zhao, W. Xiang, V. Monga, X. P. Liu, and R. Tao, “Deep scattering network with fractional wavelet transform,” _IEEE Trans. Signal Process._, vol. 69, pp. 4740--4757, Jul. 2021.

[8]      C. Gao, R. Tao, and X. J. Kang, “Weak target detection in the presence of sea clutter using Radon-fractional Fourier transform canceller,” _IEEE J. Sel. Topics Appl. Earth Observ. Remote Sens._, vol. 14, pp. 5818--5830, May 2021.

[9]      Y. Liu, F. Zhang, H. X. Miao, and R. Tao, “The hopping discrete fractional Fourier transform,” _Signal Process._, vol. 178, Article No. 107763, Jan. 2021.

[10]    H. Oberst, D. Kouznetsov, K. Shimizu, J.-I. Fujita, and F. Shimizu, “Fresnel diffraction mirror for an atomic wave,” _Phys. Rev. Lett._, vol. 94, Article No. 013203, Jan. 2005.

---

# 协作与分工
1.  强盛周：
    -   进行Wigner分布的研究，包括Wigner分布的定义和数学表达式。
    -   研究基于Wigner分布的信号表示理论，包括广义Wigner分布和线性正则域Wigner分布的相关理论，建立基于期望的不等式模型。
    -   参与数值仿真中的算法设计，编写并实现MATLAB程序代码，并根据反馈维护修改程序。
    -   协助撰写论文和报告，整理研究结果和分析。
3.  蒋贤：
    -   参与非平稳信号检测领域的文献综述和前沿技术调研。
    -   研究线性正则变换的基本原理和方法，了解其在信号处理中的应用。
    -   协助构建研究框架，包括闭形式瞬时互相关函数型Wigner分布和线性正则变换自由参数的引入方法，建立基于方差的不等式模型。
    -  参与研究中的数值仿真分析，评估线性正则变换自由参数与检测性能之间的因果关系。
    -   参与研究结果的讨论和总结，并参与撰写相关部分的论文和报告。
1.  陈正龙：
    -   参与线性正则变换与Wigner分布的理论研究。
    -   分析线性正则变换自由参数引入方法建立的线性正则域Wigner分布之间的包含关系，进一步提出KF-$\tau$-WD方法
    -   协助构建相关理论，并在此基础上针对含噪非平稳信号进行研究。
    -   参与研究结果的分析和讨论，并撰写相关部分的论文和报告。