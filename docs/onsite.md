# Genomics Hub On-Site Data Processing
## Data Ingestion From On-Site

### Data Transfer: Sequencer BCL data automatically transfer
 * The sequencer will automatically transfer the generated raw BCL data into the `seqout` folder in Pure Storage:
    
    Example:
    <pre><code> /purexxxx/hubs/genomics/seqout/{site_name}{instrument_manufacturer}{serial_number} </code></pre> 
 
 * Data stored in pure storage is `read only` by everyone, `writable only` by instrument.

    Data stored in this path of pure storage will be automatically synchronized into an AWS S3 bucket under the name altos-lab-genomics-seqout:
    <pre><code> s3://altos-lab-genomics-seqout/{site_name}_{instrument_manufacturer}_{serial_number]} </code></pre>



### Demultiplexing
* Demultiplexing on Nextflow Tower Manually (Not Recommend):
    * BCL data can be demultiplexed through the demultiplexing pipeline of the Nextflow Tower

* Demultiplexing on Nextflow Tower Automatically (Recommend)
    * [Altos Labs - Genomics Data Hub - Site User Guide v3](https://docs.google.com/presentation/d/1wc8YL9THBm5JfrHw4Y_Su7b9F7NkeR9RHj-apLC0ChY/edit#slide=id.g1a6804f61de_0_167)

        


