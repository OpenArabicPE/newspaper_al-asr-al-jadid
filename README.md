---
title: "newspaper_al-asr-al-jadid: read me"
author: Till Grallert
date: 2019-03-01
---

This repository contains bibliographic metadata for the privately published newspaper in Damascus, *al-ʿAṣr al-Jadīd*, which was published from 1 October 1908 onwards by Nāṣīḏ Abū Zayd.

# some technical details

This repository contains the following files:

1. a [TEI XML](metadata/al-asr-al-jadid.TEIP5.xml) file containing one `<biblStruct>` for each issue of *al-ʿAṣr al-Jadīd* between #53 and #249 for which there are digital facsimiles available from the Internet Archive ([1909](https://archive.org/details/AlAsrAljadid1909OttomanEmpireArabic), [1910](https://archive.org/details/AlAsrAljadid1910OttomanEmpireArabic)). This file is produced through automatic iteration making use of [this code developed for OpenArabicPE](https://github.com/OpenArabicPE/generate_metadata-through-iteration/tree/al-asr-al-jadid) and manual validation against the digital facsimiles.
2. individual TEI files for every issue of *al-ʿAṣr al-Jadīd*. These are generated from the output of step 1 using the XSLT stylesheet [`generate_tei-from-biblstruct.xsl`](https://github.com/OpenArabicPE/generate_metadata-through-iteration/blob/al-asr-al-jadid/xslt/generate_tei-from-biblstruct.xsl) from the same repository. TEI files contain links to the locally available facsimiles.
3. all bibliographic data is then [automatically converted](https://www.github.com/OpenArabicPE/convert_tei-to-mods) from TEI XML to MODS XML for integration into reference management software etc (such as Zotero).
4. The TEI files for individual issues were [converted to TSS XML](https://github.com/OpenArabicPE/convert_tei-to-sente/) for use with the now discontinued reference manager Sente. Before import into Sente, one needs to generate one PDF per issue from the attached facsimiles using [this code](https://github.com/OpenArabicPE/generate_pdf-from-attached-facsimiles) and make sure that these files are available (the relative links in TSS XML must be turned into absolute ones).