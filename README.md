UclCli
=============================================================================

C++/CLI .NET wrapper around the UCL compression library. Provides a static
class that exposes all of the libraries compression and decompression
functions, but with .NET types.

Usage
-----------------------------------------------------------------------------

```csharp
// Compress string
var uncompressed = Encoding.UTF8.GetBytes("Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque sagittis nunc eget sem elementum, id convallis mauris placerat. Pellentesque venenatis est a mauris interdum, vitae vestibulum nunc viverra. Sed volutpat odio vitae turpis facilisis, quis dignissim nisi tincidunt. Maecenas egestas molestie diam vel posuere. Praesent cursus est eu enim tincidunt facilisis. Proin gravida pharetra purus, porttitor egestas justo pellentesque sit amet. Cras nec iaculis arcu, at egestas enim. Aliquam aliquet mollis massa a iaculis. Sed vel eleifend justo, sit amet dictum massa.");
var compressed = Ucl.NRV2E_99_Compress(uncompressed, 10);

// Decompress compressed string and print it
var decompressed = Ucl.NRV2E_Decompress_8(compressed, uncompressed.Length);
Console.WriteLine(Encoding.UTF8.GetString(decompressed));
```

Links
-----------------------------------------------------------------------------

- GitHub: https://github.com/exectails/UclCli
- UCL Website: http://www.oberhumer.com/opensource/ucl/
