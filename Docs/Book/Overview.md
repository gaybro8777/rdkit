# An overview of the RDKit

## What is it?

### Open source toolkit for cheminformatics
-   Business-friendly BSD license
-   Core data structures and algorithms in C++
-   Python 3.x wrappers generated using Boost.Python
-   Java and C\# wrappers generated with SWIG
-   2D and 3D molecular operations
-   Descriptor generation for machine learning
-   Molecular database cartridge for PostgreSQL
-   Cheminformatics nodes for KNIME (distributed from the KNIME community site: https://www.knime.com/rdkit)

### Operational:
- http://www.rdkit.org
- Supports Mac/Windows/Linux
- Releases every 6 months
- Web presence:
    - Homepage: http://www.rdkit.org
      Documentation, links
    - Github (https://github.com/rdkit)
      Downloads, bug tracker, git repository
    - Sourceforge (http://sourceforge.net/projects/rdkit)
      Mailing lists
    - Blog (https://rdkit.blogspot.com)
      Tips, tricks, random stuff
    - Tutorials (https://github.com/rdkit/rdkit-tutorials)
      Jupyter-based tutorials for using the RDKit
    - KNIME integration (https://github.com/rdkit/knime-rdkit)
      RDKit nodes for KNIME
- Mailing lists at https://sourceforge.net/p/rdkit/mailman/, searchable archives available for [rdkit-discuss](http://www.mail-archive.com/rdkit-discuss@lists.sourceforge.net/) and [rdkit-devel](http://www.mail-archive.com/rdkit-devel@lists.sourceforge.net/)
- Social media:
    - Twitter: @RDKit_org
    - LinkedIn: https://www.linkedin.com/groups/8192558
    - Slack: https://rdkit.slack.com (invite required, contact Greg)

### History:
-   2000-2006: Developed and used at Rational Discovery for building predictive models for ADME, Tox, biological activity
-   June 2006: Open-source (BSD license) release of software, Rational Discovery shuts down
-   to present: Open-source development continues, use within Novartis, contributions from Novartis back to open-source version

## Citing the RDKit

There is still no official RDKit publication, our recommended citation is:
```
RDKit: Open-source cheminformatics. https://www.rdkit.org
```
We also recommend that you include the DOI for the version of the RDKit you used in the work. You can look these up here:
https://doi.org/10.5281/zenodo.591637


### Powered by RDKit
[![RDKit badge](https://img.shields.io/badge/Powered%20by-RDKit-3838ff.svg?logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQBAMAAADt3eJSAAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAAFVBMVEXc3NwUFP8UPP9kZP+MjP+0tP////9ZXZotAAAAAXRSTlMAQObYZgAAAAFiS0dEBmFmuH0AAAAHdElNRQfmAwsPGi+MyC9RAAAAQElEQVQI12NgQABGQUEBMENISUkRLKBsbGwEEhIyBgJFsICLC0iIUdnExcUZwnANQWfApKCK4doRBsKtQFgKAQC5Ww1JEHSEkAAAACV0RVh0ZGF0ZTpjcmVhdGUAMjAyMi0wMy0xMVQxNToyNjo0NyswMDowMDzr2J4AAAAldEVYdGRhdGU6bW9kaWZ5ADIwMjItMDMtMTFUMTU6MjY6NDcrMDA6MDBNtmAiAAAAAElFTkSuQmCC)](https://www.rdkit.org/)

If you use RDKit in one of your projects, you can show your support and help us track it by adding our badge.
Simply copy the code from one of the markup languages below and paste it in your README file:

<details>
  <summary>Markdown</summary>
  <div style="display: flex">
    <textarea rows="1" wrap="off" readonly style="display: inline-block; width: 100%; resize: none; overflow-y: hidden">[![Powered by RDKit](https://img.shields.io/badge/Powered%20by-RDKit-3838ff.svg?logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQBAMAAADt3eJSAAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAAFVBMVEXc3NwUFP8UPP9kZP+MjP+0tP////9ZXZotAAAAAXRSTlMAQObYZgAAAAFiS0dEBmFmuH0AAAAHdElNRQfmAwsPGi+MyC9RAAAAQElEQVQI12NgQABGQUEBMENISUkRLKBsbGwEEhIyBgJFsICLC0iIUdnExcUZwnANQWfApKCK4doRBsKtQFgKAQC5Ww1JEHSEkAAAACV0RVh0ZGF0ZTpjcmVhdGUAMjAyMi0wMy0xMVQxNToyNjo0NyswMDowMDzr2J4AAAAldEVYdGRhdGU6bW9kaWZ5ADIwMjItMDMtMTFUMTU6MjY6NDcrMDA6MDBNtmAiAAAAAElFTkSuQmCC)](https://www.rdkit.org/)
    </textarea>
    <button onclick="copyBadgeMarkdown(this)" style="display: inline-block; padding: 0 8px">Copy</button>
  </div>
</details>

<details>
  <summary>reStructuredText</summary>
  <div style="display: flex">
    <textarea rows="1" wrap="off" readonly style="display: inline-block; width: 100%; resize: none; overflow-y: hidden">.. image:: https://img.shields.io/badge/Powered%20by-RDKit-3838ff.svg?logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQBAMAAADt3eJSAAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAAFVBMVEXc3NwUFP8UPP9kZP+MjP+0tP////9ZXZotAAAAAXRSTlMAQObYZgAAAAFiS0dEBmFmuH0AAAAHdElNRQfmAwsPGi+MyC9RAAAAQElEQVQI12NgQABGQUEBMENISUkRLKBsbGwEEhIyBgJFsICLC0iIUdnExcUZwnANQWfApKCK4doRBsKtQFgKAQC5Ww1JEHSEkAAAACV0RVh0ZGF0ZTpjcmVhdGUAMjAyMi0wMy0xMVQxNToyNjo0NyswMDowMDzr2J4AAAAldEVYdGRhdGU6bW9kaWZ5ADIwMjItMDMtMTFUMTU6MjY6NDcrMDA6MDBNtmAiAAAAAElFTkSuQmCC
      :alt: Powered by RDKit
      :target: https://www.rdkit.org/
    </textarea>
    <button onclick="copyBadgeMarkdown(this)" style="display: inline-block; padding: 0 8px">Copy</button>
  </div>
</details>

<details>
  <summary>HTML</summary>
  <div style="display: flex">
    <textarea rows="1" wrap="off" readonly style="display: inline-block; width: 100%; resize: none; overflow-y: hidden"><a href="https://www.rdkit.org/"><img alt="Powered by RDKit" src="https://img.shields.io/badge/Powered%20by-RDKit-3838ff.svg?logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQBAMAAADt3eJSAAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAAFVBMVEXc3NwUFP8UPP9kZP+MjP+0tP////9ZXZotAAAAAXRSTlMAQObYZgAAAAFiS0dEBmFmuH0AAAAHdElNRQfmAwsPGi+MyC9RAAAAQElEQVQI12NgQABGQUEBMENISUkRLKBsbGwEEhIyBgJFsICLC0iIUdnExcUZwnANQWfApKCK4doRBsKtQFgKAQC5Ww1JEHSEkAAAACV0RVh0ZGF0ZTpjcmVhdGUAMjAyMi0wMy0xMVQxNToyNjo0NyswMDowMDzr2J4AAAAldEVYdGRhdGU6bW9kaWZ5ADIwMjItMDMtMTFUMTU6MjY6NDcrMDA6MDBNtmAiAAAAAElFTkSuQmCC"></a>
    </textarea>
    <button onclick="copyBadgeMarkdown(this)" style="display: inline-block; padding: 0 8px">Copy</button>
  </div>
</details>

<script>
  function copyBadgeMarkdown(btn) {
    if (navigator.clipboard) {
      var text = btn.previousElementSibling.textContent;
      navigator.clipboard.writeText(text);
    }
  }
</script>

## Integration with other open-source projects
- [KNIME](https://www.knime.com/rdkit): Workflow and analytics tool
- [PostgreSQL](https://github.com/rdkit/rdkit/blob/master/Docs/Book/Cartridge.rst): Extensible relational database
- [Django](http://django-rdkit.readthedocs.org/en/latest/): "The web framework for perfectionists with deadlines"
- [SQLite](https://github.com/rvianello/chemicalite): "The most used database engine in the world"
- [Lucene](https://github.com/rdkit/org.rdkit.lucene): Text-search engine [1](#footnote1)

## Usage by other open-source projects
This will, inevitably, be out of date. If you know of others, please let us know or submit a pull request!

- [Datamol](https://datamol.io/) ([docs](https://doc.datamol.io/stable/), [repo](https://github.com/datamol-org/datamol/)) - A Python library to intuitively manipulate molecules.
- [DockOnSurf](https://gitlab.com/lch_interfaces/dockonsurf) ([docs](https://dockonsurf.readthedocs.io), [paper](https://www.doi.org/10.26434/chemrxiv.14095699)) - A high-throughput python code to automatically find the most stable geometry for molecules adsorbed on surfaces.
- [Scopy](https://github.com/kotori-y/Scopy) ([docs](https://scopy.iamkotori.com/), [paper](https://doi.org/10.1093/bib/bbaa194)) - an integrated negative design Python library for desirable HTS/VS database design
- [Open Force Field Toolkit](https://github.com/openforcefield/openforcefield/) - A parametrization engine for force fields based on direct chemical perception.
- [stk](https://github.com/lukasturcani/stk) ([docs](https://lukasturcani.github.io/stk/docs/build/html/), [paper](https://onlinelibrary.wiley.com/doi/10.1002/jcc.25377)) -
a Python library for building, manipulating, analyzing and automatic design of molecules.
- [gpusimilarity](https://github.com/schrodinger/gpusimilarity) - A Cuda/Thrust implementation of fingerprint similarity searching
- [Samson Connect](https://www.samson-connect.net) - Software for adaptive modeling and simulation of nanosystems
- [mol_frame](https://github.com/apahl/mol_frame) - Chemical Structure Handling for Dask and Pandas DataFrames
- [RDKit.js](https://github.com/rdkit/rdkit-js) - The official JavaScript release of RDKit
- [DeepChem](https://deepchem.io) - python library for deep learning for chemistry
- [mmpdb](https://github.com/rdkit/mmpdb) - Matched molecular pair database generation and analysis
- [CheTo](https://github.com/rdkit/CheTo) ([paper](http://pubs.acs.org/doi/10.1021/acs.jcim.7b00249))- Chemical topic modeling
- [OCEAN](https://github.com/rdkit/OCEAN) ([paper](http://pubs.acs.org/doi/abs/10.1021/acs.jcim.6b00067))- Optimized cross reactivity estimation
- [ChEMBL Beaker](https://github.com/mnowotka/chembl_beaker) - standalone web server wrapper for RDKit and OSRA
- [myChEMBL](https://github.com/chembl/mychembl) ([blog post](http://chembl.blogspot.de/2013/10/chembl-virtual-machine-aka-mychembl.html), [paper](http://bioinformatics.oxfordjournals.org/content/early/2013/11/20/bioinformatics.btt666)) - A virtual machine implementation of open data and cheminformatics tools
- [ZINC](http://zinc15.docking.org) - Free database of commercially-available compounds for virtual screening
- [sdf_viewer.py](https://github.com/apahl/sdf_viewer) - an interactive SDF viewer
- [sdf2ppt](https://github.com/dkuhn/sdf2ppt) - Reads an SDFile and displays molecules as image grid in powerpoint/openoffice presentation.
- [MolGears](https://github.com/admed/molgears) - A cheminformatics tool for bioactive molecules
- [PYPL](http://www.biochemfusion.com/downloads/#OracleUtilities) - Simple cartridge that lets you call Python scripts from Oracle PL/SQL.
- [shape-it-rdkit](https://github.com/jandom/shape-it-rdkit) - Gaussian molecular overlap code shape-it (from silicos it) ported to RDKit backend
- [WONKA](http://wonka.sgc.ox.ac.uk/WONKA/) - Tool for analysis and interrogation of protein-ligand crystal structures
- [OOMMPPAA](http://oommppaa.sgc.ox.ac.uk/OOMMPPAA/) - Tool for directed synthesis and data analysis based on protein-ligand crystal structures
- [OCEAN](https://github.com/rdkit/OCEAN) - web-tool for target-prediction of chemical structures which uses ChEMBL as datasource
- [chemfp](http://chemfp.com) - very fast fingerprint searching
- [rdkit_ipynb_tools](https://github.com/apahl/rdkit_ipynb_tools) - RDKit Tools for the IPython Notebook
- [Vernalis KNIME nodes](https://www.knime.com/book/vernalis-nodes-for-knime-trusted-extension)
- [Erlwood KNIME nodes](https://www.knime.com/community/erlwood)
- [AZOrange](https://github.com/AZcompTox/AZOrange)

## The Contrib Directory

The Contrib directory, part of the standard RDKit distribution, includes code that has been contributed by members of the community.


## Footnotes

<a name="footnote1">1</a>: These implementations are functional but are not necessarily the best, fastest, or most complete.


## License

This document is copyright (C) 2013-2018 by Greg Landrum

This work is licensed under the Creative Commons Attribution-ShareAlike 4.0 License. To view a copy of this license, visit <http://creativecommons.org/licenses/by-sa/4.0/> or send a letter to Creative Commons, 543 Howard Street, 5th Floor, San Francisco, California, 94105, USA.

The intent of this license is similar to that of the RDKit itself. In simple words: “Do whatever you want with it, but please give us some credit.”
