
This is the artifact for the FSE'18 paper **Detection of Energy Inefficiencies
in Android Wear Watch Faces** by *Hailong Zhang*, *Haowei Wu* and *Atanas Rountev*.
It contains the static analysis, testing framework, experimental
subjects, materials for app market study, logs generated by the static analysis,
and the result of testing. Details on the instructions and usage are in the 
readme files in each sub-folder.

# Installation

Below are two ways to download the artifact including all the benchmarks.
After downloading all the necessary files, follow the instructions in [INSTALL.md](INSTALL.md)
to reproduce the results in the paper.

## Recommended way

We recommend downloading the artifact from [APTWear](http://web.cse.ohio-state.edu/presto/software/aptwear)
as we will post future fixes and improvements there.

There are two files required:

1. fse18.tar.xz (implementation and watch faces with leaks, 1.3GB);
2. fse18-benchmark.tar (all 1490 benchmarks described in the paper, 16GB).

```bash
wget http://web.cse.ohio-state.edu/presto/software/aptwear/downloads/fse18.tar.xz
tar xvfJ fse18.tar.xz
wget http://web.cse.ohio-state.edu/presto/software/aptwear/downloads/fse18-benchmark.tar
tar xvf fse18-benchmark.tar --directory hailongzhang-aptwear-fse18-paper-163/
```

## GitHub way

Due to GitHub's limitation on file sizes, all benchmarks have to be downloaded separately.

```bash
git clone https://github.com/presto-osu/fse18.git
wget http://web.cse.ohio-state.edu/presto/software/aptwear/downloads/fse18-benchmark.tar
tar xvf fse18-benchmark.tar --directory fse18/
```

# Structure

- `analysis` includes the code for static analysis;
- `analysis-logs` contains the log files by running the static analysis against
the 1490 experimental subjects;
- `apks` (download separately) includes all the experimental subjects,
i.e., the APK files for 1490 watch faces, as well as the tool to download them;
- `app-market-study` contains the crawler for app markets and the scripts to
generate statistics in the paper;
- `INSTALL.md` includes the instructions to reproduce the experimental results in 
the paper;
- `LICENSE` includes the copyright information;
- `README.md` is this file;
- `testing` contains the testing framework and the results.

Others may use the static analysis to detect inefficiencies for any new watch
face, use the testing framework to validate the reports by static analysis, as
well as utilizing the benchmarks located at `apks` for further studies.

Please refer to the readme files in each sub-directory for more details.

# Questions

If you have any question, please contact the authors of the paper.

