# Quick Tips for Downloading Data from NCBI's Sequence Read Archive (SRA)
Here is one way of downloading data from SRA. Alternatively, see the [SRA Toolkit Documentation](https://trace.ncbi.nlm.nih.gov/Traces/sra/sra.cgi?view=toolkit_doc).

1. Get SRA Toolkit, if not already present on your system
   - Download appropriate compiled binary for your system from https://github.com/ncbi/sra-tools/wiki/Downloads
   
2. Download SRA data for the run accession of your choice
   - Use `prefetch` tool from SRA toolkit, e.g. for the run accession SRR111111 : 
   ```
   /Users/uname/Downloads/sratoolkit.2.9.2-mac64/bin/prefetch SRR111111
   ```
   - After downloading, you may need to move file from designated cache area to your preferred working directory, e.g. :
   ```
   mv /Users/uname/ncbi/public/sra/SRR111111.sra /path/to/preferred/directory/
   ```
3. Convert *.sra file to preferred file type
   - Use tool from the SRA Toolkit bin directory (same directory wherein you found the `prefetch` tool) such as `fastq-dump`, `sam-dump`, `sff-dump`
   - For more information, see: [Using the SRA Toolkit to convert .sra files into other formats
](https://www.ncbi.nlm.nih.gov/books/NBK158900/)
