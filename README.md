<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=300&text= AutoRClone_Sync &fontAlignY=35&desc=Backup%20your%20Beloved%20RClone%20Drives%20to%20Multiple%20Mirrors&animation=fadeIn&fontColor=0c1017" alt="RClone Mirror Manager"/>

</div>

# Description
Put simply, it regularly triggers GitHub Actions to execute a script that pair-wise iterates and runs `rclone sync` over defined drives. 

---

# Dependencies 🧰
- AutoRclone
- python3
- Potato brain

---

# Usage 👨‍💻
1. Create an `rclone.conf` file that complies with [RClone](https://rclone.org/).
2. Host it on some online paste bin. I personally use Secret Gists (yep, I’m obsessed with version control, how’d you guess?).
3. Fork/mirror this repo.
4. Create a GitHub Secret called `CONF_URL` and set it's value as the link to the rclone config (make sure you copy the link to the "RAW Text").
5. Edit the `from_drives` and `to_drives` in [`sync.py`](sync.py) as you wish.
6. The script is set to run every day at 6:30 AM UTC. Feel free to modify that under [`.github/workflows/sync.yaml`](.github/workflows/sync.yaml).
7. Profit 💯

---
