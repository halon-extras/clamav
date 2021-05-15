## clam_av(fp[, options])

Scan a File pointer (fp) with ClamAV.

**Params**

- fp `File` - the mail file
- options `array` - options array

**Returns**: A `array` of viruses found, the array is empty if the message was clean or `none` on error.

The following options are available in the **options** array.

- timeout `number` - Timeout in seconds. The default is 5 seconds.
- path `string` - Path to a the clamd unix socket. The default is `/var/run/clamd.sock` 
