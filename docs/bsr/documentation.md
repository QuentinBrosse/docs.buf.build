---
id: documentation
title: Generated Documentation
---

import useBaseUrl from '@docusaurus/useBaseUrl';

The BSR comes with complete documentation for your Protobuf files through a browsable UI with syntax highlighting, one click navigation between definitions and references. Navigate to a repository within the BSR and click the **Docs** tab. 

<div align="center">
  <img alt="BSR module" src={useBaseUrl('/img/bsr/gen_docs-3.png')}/>
</div>

For an example see the `demolab/theweather` module by visiting [https://buf.build/demolab/theweather/docs](https://buf.build/demolab/theweather/docs).

## Module documentation

The majority of documentation will come directly from comments associated with your Protobuf definitions. But, there also needs to be a simple way for authors to *describe their module* for others to understand its functionality.

To accomplish this, you add a `buf.md` file to the same directory as your module's `buf.yaml` file and push it to the BSR like normal. Since documentation is part of your module, any updates to your `buf.md` will result in new commits in the BSR.

The `buf.md` file is analogous to a GitHub repository's `README.md` and currently supports all of the
[CommonMark](https://commonmark.org) syntax.

<div align="center">
  <img alt="BSR module" src={useBaseUrl('/img/bsr/gen_docs-2.png')}/>
</div>

## Package documentation

The package level documentation provides Protobuf type definitions and comments for all package files. Clicking through the type definitions will take you to the referenced item.

You can quickly navigate from the docs to the Protobuf file by clicking the filename on the right-hand side.

Each type definition will have a unique placeholder within the page, an anchor tag, making it easy to share links referencing the exact item.

### Package description

When sharing packages it is often useful to provide an overview of the package. You can do so by adding comments above the `package` directive in your .proto file.

Comments on the package directive are not merged across files. Files are parsed alphabetically, and only the first file with a non-empty comment will be displayed in the generated documentation.

<div align="center">
  <img alt="BSR module" src={useBaseUrl('/img/bsr/gen_docs-1_v2.png')}/>
</div>