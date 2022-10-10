## clam_av(fp[, options])

Scan a File pointer (fp) with ClamAV.

**Params**

- fp `File` - the mail file
- options `array` - options array

The following options are available in the **options** array.

- timeout `number` - Timeout in seconds. The default is 5 seconds.
- path `string` - Path to a the clamd unix socket. The default is `/var/run/clamav/clamd.ctl` 
- address `string` - Host of the clamd server.
- port `number` - Port of the clamd server.

**Returns**: An associative array, with a `virus` property containing a list of viruses found (array of strings), however note that clamd may currently only return one virus. If an error occures an `error` property (string) is set contaning the error message.

```
import { clamav } from "extras://clamav";

$clamav = clamav($mail->toFile());
if ($clamav["virus"])
  Reject("Virus found");
```
