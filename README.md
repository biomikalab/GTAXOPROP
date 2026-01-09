# GTAXOPROP

![Python Version](https://img.shields.io/badge/python-3.10+-blue.svg)
![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)
![Version](https://img.shields.io/badge/version-1.0.0-green.svg)

**GTAXOPROP** (Genbinesia Taxonomy Propagator) is a utility to generate input files for taxonomy propagation and assignment in QIIME/QIIME2 from the NCBI database. It converts NCBI accession numbers to QIIME-compatible taxonomy files with API fallback.

# ⚠️ Derivative Work Notice

GTAXOPROP is a **derivative work** based on `entrez_qiime` v.2.0 by Christopher C. M. Baker.
This version includes substantial modifications and enhancements while maintaining GPL v3 compliance.

**Original work:** Baker, C. C. M. (2016). entrez_qiime. Version 2.0. https://github.com/bakerccm/entrez_qiime

# Major Enhancements from Original
- ✅ Complete Python 3 migration
- ✅ cogent3 integration (replaced PyCogent)
- ✅ Advanced caching with resume capability
- ✅ Batch API processing with rate limiting
- ✅ Improved error handling and logging
- ✅ Enhanced file encoding detection
- ✅ Better taxonomy rank handling

# Quick Start

## Usage
gtaxoprop -i your_sequences.fasta -o your_taxdumps.txt -g your_execution.log -n /path/to/your/NCBI/taxdump/ -a /path/to/your/NCBI/accession2taxid/wgs.accession2taxid -r domain,kingdom,phylum,class,order,family,genus,species -d --email your_mail@email.xxx

## Help
gtaxoprop -h

# Acknowledgments
Based on entrez_qiime Version 2.0 by Chris Baker (https://github.com/bakerccm/entrez_qiime)

# License
GNU General Public License v3.0 - See LICENSE
