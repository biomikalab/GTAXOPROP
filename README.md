# GTAXOPROP (Genbinesia Taxonomy Propagator)

![Python Version](https://img.shields.io/badge/python-3.10+-blue.svg)
![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)
![Version](https://img.shields.io/badge/version-1.0.0-green.svg)
[![Github All Releases](https://img.shields.io/github/downloads/biomikalab/GTAXOPROP/total.svg)]()

**GTAXOPROP** is a utility to generate input files for taxonomy propagation and assignment in QIIME/QIIME2 from the NCBI database. It converts NCBI accession numbers to QIIME-compatible taxonomy files with API fallback.

# ⚠️ Derivative Work Notice

GTAXOPROP is a **derivative work** based on `entrez_qiime` v.2.0 by Christopher C. M. Baker.
This version includes substantial modifications and enhancements while maintaining GPL v3 compliance.

**Original work:** Baker, C. C. M. (2016). entrez_qiime. Version 2.0. https://github.com/bakerccm/entrez_qiime

# Major Enhancements from Original
- ✅ Complete Python 3 migration
- ✅ cogent3 integration (replaced PyCogent)
- ✅ Better NCBI Entrez communication using Biopython 
- ✅ Advanced caching with resume capability
- ✅ Batch API processing with rate limiting
- ✅ Improved error handling and logging
- ✅ Enhanced file encoding detection
- ✅ Better taxonomy rank handling

# Authors
- Maulana Malik Nashrulloh (Division of Biomics Research, Department of Sciences, Generasi Biologi Indonesia Foundation)
- Sonia Az Zahra Defi (Department of Biology, Faculty of Mathematics and Natural Sciences, Brawijaya University)
- Brian Rahardi (Department of Bioinformatics, Faculty of Mathematics and Natural Sciences, Brawijaya University)
- Muhammad Badrut Tamam (Division of Biomics Research, Department of Sciences, Generasi Biologi Indonesia Foundation & Biology Program, Faculty of Science, Technology, and Education, Muhammadiyah University of Lamongan)
- Riki Ruhimat (Research Center for Applied Microbiology, Research Organization for Life Sciences, National Research and Innovation Agency)
- Hessy Novita (Research Center for Veterinary Science, Research Organization for Health, National Research and Innovation Agency)

# Quick Start

## Installation
Currently we only support installation thru `pip` command only.
```bash
pip install git+https://github.com/biomikalab/GTAXOPROP.git
```

We hope we may provide PyPI and conda packages too in the future. STAY TUNES!

## Usage
For propagating taxonomy of Archaea, Bacteria, and Eukaryota:
```bash
gtaxoprop -i your_sequences.fasta -o your_taxdumps.txt -g your_execution.log -n /path/to/your/NCBI/taxdump/ -a /path/to/your/NCBI/accession2taxid/wgs.accession2taxid -r domain,kingdom,phylum,class,order,family,genus,species -d --email your_mail@email.xxx
```

For propagating taxonomy of Virus:
```bash
gtaxoprop -i your_sequences.fasta -o your_taxdumps.txt -g your_execution.log -n /path/to/your/NCBI/taxdump/ -a /path/to/your/NCBI/accession2taxid/wgs.accession2taxid -r realm,kingdom,phylum,class,order,family,genus,species -d --email your_mail@email.xxx
```

## Help
To access the help, use:
```bash
gtaxoprop -h
```

# Acknowledgments
This program is based on entrez_qiime Version 2.0 by Chris Baker (https://github.com/bakerccm/entrez_qiime)

# License
GNU General Public License v3.0 - See LICENSE
