# PDFMerger for PHP (PHP 5 and above up to PHP 8.1 Compatible)

PDFMerger created by Jarrod Nettles December 2009 jarrod@squarecrow.com

Updated by Vasiliy Zaytsev February 2016 vasiliy.zaytsev@ffwagency.com

- Uses tcpdf 6.6.5 by Nicola Asuni
- Uses patched tcpdi_parser 0.4 by Vitor Mattos with own TCPdiParserException
- Uses TCPDI 1.3.4 by Pavel Kulbakin with FPDF_TPL extension 1.2.3 by Setasign

## PHP 5,6,7 and 8 Compatible

I have made some changes in original codes to make PHPMerger compatible for PHP 5. 

- Update

Successfully tested with PHP 8.1.

## Support of PDF 1.5 and PDF 1.6

FPDF and FPDI libraries replaced by TCPDF with TCPDI extension and parser.

### Using Namespace

```php
use InergyTechCorp\PDFMerger\PDFMerger;

$pdf = new PDFMerger;

$pdf->addPDF('a.pdf');
$pdf->addPDF('b.pdf');

$pdf->merge('download','merged.pdf');
```

### Example Usage
```php
include 'PDFMerger.php';

$pdf = new PDFMerger; // or use $pdf = new \PDFMerger; for Laravel

$pdf->addPDF('samplepdfs/one.pdf', '1, 3, 4');
$pdf->addPDF('samplepdfs/two.pdf', '1-2');
$pdf->addPDF('samplepdfs/three.pdf', 'all');


$pdf->merge('file', 'samplepdfs/TEST2.pdf'); // generate the file

$pdf->merge('download', 'samplepdfs/test.pdf'); // force download

// REPLACE 'file' WITH 'browser', 'download', 'string', or 'file' for output options
```
