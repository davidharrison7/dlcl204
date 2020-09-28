# Tips for scanning books

*The following tips are adapted from [Data-Sitters Club #2: Katia and the Phantom Corpus](https://datasittersclub.github.io/site/dsc2/).*

If you are going to OCR some texts, you should **actually scan your sources**. With a scanner. At minimum 300 dpi (dots per inch -- it's a measure of how much detail the image captures). More like 400-600 dpi if your books include a really small font, like for footnotes. Yes, the technology is improving, and sometimes you can get better-than-total-garbage with photos from your phone, as long as they're not skewed (taken at an angle), the lighting is good, etc., but still, most phone pictures are still only 72 dpi, and it's hard to position your phone directly above a book and not cast a shadow. Just use a scanner.

**Scan your sources in grayscale**, especially if you're going to be using ABBYY FineReader. While all the OCR algorithms actually use on binarized images (black & white -- where everything in the image is either black or white, according to some threshold you or the software defines), you can go from grayscale to B&W, but not the other way around. Even though the OCR algorithm itself involves a binarized image, the algorithms used for layout analysis (i.e. figuring out where the text is on the page, whether it's one column or two, whether there's tables or running headers or page numbers, etc.) are more nuanced. Also, both ABBYY FineReader and the open-source Tesseract software include pre-processing steps before they perform the OCR, including binarizing images using a sensible threshold that cuts down on the noise in the image. For instance, if you run a B&W scan of a two-page spread through Tesseract (i.e. an image where the binarization has happened at the time when you did the scanning), you'll end up with some gibberish from when the OCR algorithm tried to "read" the shadow caused by the binding.

The [ABBYY FineReader documentation](https://abbyy.technology/en:kb:images_resolution_size_ocr) recommends color scans, but in most cases, the improvement in final OCR quality from color images vs. grayscale is negligible, and the file sizes are much bigger for color images.

**Save your scans as .tif files**, which are uncompressed and don't lose any of the data in the image to make the file size smaller. A 300 dpi grayscale scan of a two-page spread of a Baby-Sitters Club book (like you'd get when scanning it, assuming you don't want to just cut the book's spine and run it through a sheet-feeder scanner -- which is viscerally disturbing, but a much more time-efficient option) is close to 7 MB, and there's around 80 such scanned images per book, which works out to around half a gigabyte per book for the page images. If all you want is good OCR, don't feel like you need to keep all these image files for the long-term: you're not responsible for library-quality preservation for the books. Once you're satisfied with the OCR quality, you can let them go and delete them.