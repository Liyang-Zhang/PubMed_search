# PubMed_search

This Python script searches PubMed articles for genes associated with female infertility. It first retrieves all known human genes that have annotated, Ensembl, and RefSeq matched genes' names. Then, it retrieves PubMed articles based on a search query and tries to find genes mentioned in those articles' abstracts. The script creates a dictionary that maps matched genes to their corresponding article IDs, and eventually saves the resulting gene-article pairs into an Excel file.

Here is a summary of the code:

1. Import necessary libraries and set Entrez email for NCBI contact.
2. Retrieve all known human genes from NCBI database.
3. Read the gene_info.gz file and create a dictionary to store Entrez IDs and their corresponding gene symbols.
4. Define a search query for PubMed articles.
5. Use Entrez.esearch to retrieve PubMed articles based on the search query.
6. For each article, fetch its abstract and search for gene symbols in the abstract text.
7. Create a dictionary that maps matched genes to their corresponding article IDs.
8. Convert the dictionary into a DataFrame and save it to an Excel file.
9. Read a redundant gene list from an Excel file.
10. Filter out redundant genes from the search results and save the unmatched gene list to a new Excel file.
