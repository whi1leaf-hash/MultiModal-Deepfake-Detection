# Dataset setup

FakeAVCeleb is not redistributed in this repository. Obtain it from the dataset authors and follow its access and use terms. After placing it locally, set `FAKEAVCELEB_DIR` to the dataset directory before running notebooks that use it.

Windows PowerShell example (for the current terminal only):

```powershell
$env:FAKEAVCELEB_DIR = "D:\datasets\FakeAVCeleb"
```

Do not commit the dataset, audio/video samples, extracted features, labels derived from private data, or model checkpoints.
