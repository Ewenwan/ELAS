# ELAS
http://www.cvlibs.net/software/libelas/

# 《LS-ELAS: Line Segment based Efficient Large Scale Stereo Matching》：
    作者改进的ELAS（efficient large-scale stereo matching），
    ELAS说的是通过取支持点（support point）并进行三角剖分再对视差进行插值计算从而避开了其他一些算法需要做全局优化，
    而LS-ELAS通过好的线段（尤其是竖直的，水平的相对质量差，因为在epipolar line上不好找）来更好的选择支持点。
    作者号称比ELAS又好又快，现场有人质疑LS-ELAS额外有边缘检测而ELAS是3x3或5x5采样所以肯定更快，
    作者的解释是虽然边缘检测耗时间，但结果是选择出来的支持点质量要好很多，而且很多选了也不行的根本就没选，
    这样支持点其实比ELAS少很多所以计算时间省了回来，笔者觉得是非常有道理的。
    在Intel Core i7的台式机上处理大概VGA分辨率LS-ELAS能达到60fps，越大分辨率LS-ELAS相比ELAS的速度优势越明显。
    
[LS-ELAS论文 ](http://www.cogsys.cs.uni-tuebingen.de/publikationen/2017/JellalICRA17.pdf)
