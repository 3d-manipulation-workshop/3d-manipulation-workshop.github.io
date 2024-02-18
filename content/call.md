# Call for Papers

## Instructions for Submission

We invite participants to submit extended abstracts **3+n pages** (not anonymously), with n pages (no page-limit) for the bibliography, in the two-column IEEE conference style. The submissions will be reviewed by experts of the field. The accepted abstracts will be made available on the workshop website but will not appear in the official IEEE proceedings. Abstracts can be submitted through OpenReview at the link below.

LaTeX templates: http://ras.papercept.net/conferences/support/tex.php#latexclass

Submission link: https://openreview.net/group?id=IEEE.org/2024/ICRA/Workshop/3D_Manipulation

## Important Dates

| Date | Event |
|------|-------|
| April 5th, 2024 (11:59pm PST) | Paper submission deadline |
| April 16th, 2024 | Notification of acceptance |
| May 3rd, 2024 (11:59pm PST) | Camera-ready deadline |
| May 17th, 2024 | Workshop |

## Topics of Interest

We invite submissions of papers on the topic of 3D visual representations for robot manipulation. Topics of interest include, but are not limited to:

- **Acquiring 3D geometric information:** there are many ways to acquire raw 3D geometric information in a scene. Explicit acquisition methods include LiDaR scans, depth images, stereo matching, etc. Implicit acquisition methods include multi-view reconstruction (including NeRF [1]), structure from motion, etc. We would like to discuss which of these acquisition techniques will be best long-term for generalist manipulation.
- **Representing raw 3D geometry:** there are also many ways to represent 3D geometric information throughout a robotic system: point clouds, depth images, voxels, implicit functions (signed distance fields, NeRF, etc.), and meshes. Many systems also encode this information inside of entangled latent variables, or simply expect systems to extract partial information directly from RGB images. Further complicating choice of representations is dealing with a temporal dimension – how can these 3D representations be tracked and updated through the life of a system?
- **Learning on top of 3D geometric inputs:** there are several dimensions to modern deep learning systems, including architectures, datasets, and learning algorithms. Learning from 3D inputs is less well-studied than 2D images. The largest point cloud architectures commonly used have about 10 million parameters, while the smallest vision transformer has about 80 parameters, and tends to learn much better and more stably. Additionally, architectures may or may not include 3D geometric inductive biases (occlusion robustness, equivariance, symmetry). Finally, and perhaps most critically, there is a scarcity of 3D data with only several curated datasets, in contrast to the internet-scale 2D data that exists.
- **Building 3D representations which are useful for manipulation agents:** How can we construct 3D representations which can be used to infer physical properties and task-specific properties which are useful for manipulation? Physical properties include object segmentation, kinematic structure, and dynamic models, while task-specific properties include things such as goals, constraints, and 3D optical flow.
- **Connecting 3D visual representations to action spaces:** Robots can have very different action spaces; from low-level torque control to long-horizon position+velocity control. How should 3D visual pipelines be connected to these action spaces in a way that enables generalization to diverse scenarios? There are several key questions here:
    - **Black-box vs. inductive biases:** black-box architectures like [2] have maximum flexibility, but fail to generalize; modular approaches must be redesigned per-task; hybrid approaches which encode task-agnostic 3D inductive biases offer compromise [3, 4].
    - **Handling multimodality:** Many robotics problems are fundamentally multimodal - there are often many valid paths through an environment in motion planning, many real-world objects are symmetric, and multiple strategies may yield successful results. Paths in particular may also be variable-length. At the same time, multimodality and variable length paths are often very challenging for neural networks to represent.

In addition to the topics above, given the recent progress in foundational vision / language models, we will devote a portion of the workshop to debating the merits of using these representations explicitly in robot systems versus end-to-end.

[1] https://arxiv.org/abs/2003.08934  
[2] https://arxiv.org/abs/1504.00702  
[3] https://spatial-action-maps.cs.princeton.edu/  
[4] https://arxiv.org/abs/2010.14406  





