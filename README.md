# PubChem

PubChem is NCBI's open chemistry database containing information on more than 100 million chemical compounds. Operated by the National Center for Biotechnology Information (NCBI) at the U.S. National Institutes of Health (NIH), PubChem provides free programmatic access to chemical structures, molecular properties, bioactivity data, safety information, and drug information through REST and SOAP APIs.

## APIs

### PUG REST API
The Power User Gateway (PUG) REST API is the primary interface for programmatic access to PubChem data. It supports lookup of compounds by name, CID, SMILES, InChI, and structure search. Key operations include:

- Compound property retrieval (molecular formula, weight, logP, TPSA, etc.)
- Structure search (substructure, superstructure, similarity)
- Bioassay result summaries
- Cross-reference lookups (CAS, ChEMBL, ChEBI, etc.)
- 2D structure image generation

Base URL: `https://pubchem.ncbi.nlm.nih.gov/rest/pug`

Documentation: https://pubchem.ncbi.nlm.nih.gov/docs/pug-rest

### PUG View API
The PUG View API returns the full structured data pages for compounds and substances, organized hierarchically as displayed on the PubChem website. Covers names, identifiers, structures, physical and chemical properties, safety data, pharmacology, toxicology, biological activities, and literature.

Base URL: `https://pubchem.ncbi.nlm.nih.gov/rest/pug_view`

Documentation: https://pubchem.ncbi.nlm.nih.gov/docs/pug-view

### PUG SOAP API (Legacy)
Legacy SOAP/XML interface supporting structure search, identity search, and chemical standardization. New integrations should use the REST API.

WSDL: https://pubchem.ncbi.nlm.nih.gov/pug/pugsoap.cgi?wsdl

### Structure Image Service
Generates 2D structure images in PNG format for compounds identified by CID, name, or SMILES.

### Identifier Exchange Service
Bulk identifier conversion between PubChem CIDs, SIDs, and external identifiers including CAS Registry Numbers, ChEMBL, and ChEBI.

Service URL: https://pubchem.ncbi.nlm.nih.gov/idexchange/idexchange.cgi

## Authentication

PubChem APIs are free and publicly accessible without authentication. For higher rate limits, register a free NCBI API key at https://www.ncbi.nlm.nih.gov/account/ and pass it as the `api_key` query parameter.

## Rate Limits

| Access Type | Rate Limit |
|---|---|
| Anonymous | 5 requests/second per IP |
| NCBI API Key | 10 requests/second |

For bulk data needs exceeding these limits, use FTP downloads at https://ftp.ncbi.nlm.nih.gov/pubchem/

## Cost

PubChem is a free U.S. government service funded by NIH. There are no costs, subscription fees, or usage-based charges for any API or data service.

## Links

- Website: https://pubchem.ncbi.nlm.nih.gov/
- Documentation: https://pubchem.ncbi.nlm.nih.gov/docs/
- Blog: https://pubchemblog.wordpress.com/
- FTP Bulk Data: https://ftp.ncbi.nlm.nih.gov/pubchem/
- Support: https://support.nlm.nih.gov/
- NCBI Account (API Key): https://www.ncbi.nlm.nih.gov/account/
