---
{"dg-publish":true,"permalink":"/instant-ngp/"}
---

#Installation
conda create -n ngp python=3.10
conda activate ngp
cd "D:\othsoft\Instant-NGP-for-RTX-3000-and-4000\Instant-NGP-for-RTX-3000-and-4000"
pip install -r requirements.txt
done
---
#From Video
```
conda activate ngp
cd D:\othsoft\Instant-NGP-for-RTX-3000-and-4000\Instant-NGP-for-RTX-3000-and-4000
cd currentproject
python ..\scripts\colmap2nerf.py --video_in video.mp4 --video_fps 2 --run_colmap --overwrite
python "D:\othsoft\Instant-NGP-for-RTX-3000-and-4000\Instant-NGP-for-RTX-3000-and-4000scripts\colmap2nerf.py" --colmap_matcher exhaustive --run_colmap --aabb_scale 16 --overwrite
cd ..
./instant-ngp.exe currentproject
done
```

---
#From Images
conda activate ngp
cd D:\othsoft\Instant-NGP-for-RTX-3000-and-4000\Instant-NGP-for-RTX-3000-and-4000
cd currentprojectim
python "D:\othsoft\Instant-NGP-for-RTX-3000-and-4000\Instant-NGP-for-RTX-3000-and-4000\scripts\colmap2nerf.py" --colmap_matcher exhaustive --run_colmap --aabb_scale 16 --overwrite
cd ..
./instant-ngp.exe currentprojectim
done