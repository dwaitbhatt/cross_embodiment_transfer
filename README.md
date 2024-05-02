# cross_embodiment_transfer

1. Install packpages
```bash
pip install -r requirements.txt
```
2. Install robosuite fork 
```bash
git clone https://github.com/tianyudwang/robosuite
cd robosuite
pip install -e .
```

3. Data generation
```bash
python3 generate_demos.py --robot Panda
python3 generate_demos.py --robot Sawyer
```

4. Train source policy
```bash
python3 train_bc.py --config configs/Reach/BC_JV.yml
```

5. Alignment
```bash
python3 train_align --config configs/Reach/align.JV.yml
```