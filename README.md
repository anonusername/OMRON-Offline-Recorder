# OMRON-Offline-Recorder
Using 'omblepy' and 'open-BPM' to create a standalone recorder for Linux/Win/MacOSx service

## Submodules

This project depends on two external projects included as git submodules:

| Directory | Repository | Purpose |
|-----------|-----------|---------|
| `omblepy/` | [userx14/omblepy](https://github.com/userx14/omblepy) | Pair and connect with the OMRON blood-pressure machine over Bluetooth |
| `open-BPM/` | [evnleong/open-BPM](https://github.com/evnleong/open-BPM) | Read and record measurement data from the machine |

### Cloning with submodules

```bash
git clone --recurse-submodules https://github.com/anonusername/OMRON-Offline-Recorder.git
```

If you already cloned without `--recurse-submodules`, initialise them afterwards:

```bash
git submodule update --init --recursive
```

### Updating a submodule to a newer upstream commit

To pull the latest commit from an upstream submodule and open a pull request for the change:

```bash
# Update one submodule
cd omblepy          # or open-BPM
git fetch origin
git checkout main   # or whichever branch you want to track
git pull
cd ..

# Stage the new submodule pointer and open a PR
git add omblepy     # or open-BPM
git commit -m "chore: update omblepy submodule to latest"
git push origin <your-branch>
```

Then open a pull request against the `main` branch of this repository.  
The PR will show the updated submodule commit SHA, and reviewers can verify the change before merging.
