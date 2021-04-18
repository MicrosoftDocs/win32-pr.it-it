---
description: Il codec originale JPEG XR è disponibile tramite Windows Imaging Component (WIC). Il formato JPEG XR, supportato dal codec, è progettato per la fotografia digitale di utenti e professionisti.
ms.assetid: CB8D1A5F-B544-462E-8927-F45512CED873
title: Panoramica del codec JPEG XR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f32ffa397667b325d4e49eadf4d8ce42d49e8a88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316383"
---
# <a name="jpeg-xr-codec-overview"></a><span data-ttu-id="0a807-104">Panoramica del codec JPEG XR</span><span class="sxs-lookup"><span data-stu-id="0a807-104">JPEG XR Codec Overview</span></span>

<span data-ttu-id="0a807-105">Il codec originale JPEG XR è disponibile tramite Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="0a807-105">The native JPEG XR codec is available through the Windows Imaging Component (WIC).</span></span> <span data-ttu-id="0a807-106">Il formato JPEG XR, supportato dal codec, è progettato per la fotografia digitale di utenti e professionisti.</span><span class="sxs-lookup"><span data-stu-id="0a807-106">The JPEG XR format, which the codec supports, is designed for consumer and professional digital photography.</span></span>

<span data-ttu-id="0a807-107">Il formato JPEG XR può ottenere fino al doppio dell'efficienza di compressione del formato JPEG originale, con elementi di compressione meno evidenti.</span><span class="sxs-lookup"><span data-stu-id="0a807-107">The JPEG XR format can achieve up to twice the compression efficiency of the original JPEG format, with less noticeable compression artifacts.</span></span> <span data-ttu-id="0a807-108">Le funzionalità di JPEG XR includono:</span><span class="sxs-lookup"><span data-stu-id="0a807-108">Features of JPEG XR include:</span></span>

-   <span data-ttu-id="0a807-109">Supporto per immagini monocromatiche, RGB, CMYK e n-Channel</span><span class="sxs-lookup"><span data-stu-id="0a807-109">Support for monochrome, RGB, CMYK, and n-channel images</span></span>
-   <span data-ttu-id="0a807-110">formati Integer a 8, 16 e 32 bit</span><span class="sxs-lookup"><span data-stu-id="0a807-110">8-, 16-, and 32-bit integer formats</span></span>
-   <span data-ttu-id="0a807-111">Intervallo dinamico elevato, formati a gamma ampia, con valori di colore a virgola mobile o punto fisso</span><span class="sxs-lookup"><span data-stu-id="0a807-111">High dynamic range, wide-gamut formats, using fixed point or floating point color values</span></span>
-   <span data-ttu-id="0a807-112">Decodifica progressiva</span><span class="sxs-lookup"><span data-stu-id="0a807-112">Progressive decoding</span></span>
-   <span data-ttu-id="0a807-113">Codifica con perdita di perdite o senza perdita di tempo con lo stesso algoritmo di compressione</span><span class="sxs-lookup"><span data-stu-id="0a807-113">Lossy or lossless encoding using the same compression algorithm</span></span>
-   <span data-ttu-id="0a807-114">Supporto per la decodifica delle aree di interesse per immagini di grandi dimensioni</span><span class="sxs-lookup"><span data-stu-id="0a807-114">Support for decoding of regions of interest in large images</span></span>

<span data-ttu-id="0a807-115">Il formato JPEG XR viene definito nei documenti standard seguenti:</span><span class="sxs-lookup"><span data-stu-id="0a807-115">The JPEG XR format is defined in the following standards documents:</span></span>

-   <span data-ttu-id="0a807-116">ITU-T T. 832: *Information Technology-JPEG XR Image Coding System-specifica di codifica immagini*</span><span class="sxs-lookup"><span data-stu-id="0a807-116">ITU-T T.832: *Information technology – JPEG XR image coding system – Image coding specification*</span></span>
-   <span data-ttu-id="0a807-117">ISO/IEC 29199-2:2010: *Information Technology-JPEG XR Image Coding System-parte 2: specifica di codifica delle immagini*</span><span class="sxs-lookup"><span data-stu-id="0a807-117">ISO/IEC 29199-2:2010: *Information technology — JPEG XR image coding system — Part 2: Image coding specification*</span></span>

<span data-ttu-id="0a807-118">Lo standard JPEG XR è in gran parte basato sul formato [foto HD](hdphoto-format-overview.md) , ma esistono alcune differenze tra i due formati.</span><span class="sxs-lookup"><span data-stu-id="0a807-118">The JPEG XR standard is largely based on the [HD Photo](hdphoto-format-overview.md) format, but there are some differences between the two formats.</span></span> <span data-ttu-id="0a807-119">In Windows 8 il codec foto HD è stato aggiornato per supportare il formato JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="0a807-119">In Windows 8, the HD Photo codec has been updated to support JPEG XR.</span></span> <span data-ttu-id="0a807-120">Il codificatore ora restituisce sempre un flusso di bit conforme a JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="0a807-120">The encoder now always outputs a JPEG XR–compliant bit stream.</span></span> <span data-ttu-id="0a807-121">Il decodificatore può decodificare le immagini JPEG XR e HD Photo.</span><span class="sxs-lookup"><span data-stu-id="0a807-121">The decoder can decode both JPEG XR and HD Photo images.</span></span>

<span data-ttu-id="0a807-122">Miglioramenti sostanziali in termini di prestazioni, in relazione al codec Photo HD, sono stati apportati al codec JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="0a807-122">Substantial performance improvements, in relation to the HD Photo codec, have been made to the JPEG XR codec.</span></span> <span data-ttu-id="0a807-123">Ad esempio, la decodifica delle immagini con risoluzione secondaria, ad esempio la generazione di anteprime, è stata migliorata, nonché la decodifica delle immagini a bassa risoluzione.</span><span class="sxs-lookup"><span data-stu-id="0a807-123">For example, sub-resolution image decoding, such as thumbnail generation, has been improved, as well as low-resolution image decoding.</span></span> <span data-ttu-id="0a807-124">È consigliabile usare il formato JPEG XR anziché il formato foto HD.</span><span class="sxs-lookup"><span data-stu-id="0a807-124">It is recommended that you use the JPEG XR format instead of the HD Photo format.</span></span>

## <a name="codec-information"></a><span data-ttu-id="0a807-125">Informazioni sui codec</span><span class="sxs-lookup"><span data-stu-id="0a807-125">Codec Information</span></span>



|                     |                                                                         |
|---------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="0a807-126">Estensione del file</span><span class="sxs-lookup"><span data-stu-id="0a807-126">File name extension</span></span> | <span data-ttu-id="0a807-127">"JXR" e "WDP"</span><span class="sxs-lookup"><span data-stu-id="0a807-127">"jxr" and "wdp"</span></span>                                                         |
| <span data-ttu-id="0a807-128">GUID contenitore</span><span class="sxs-lookup"><span data-stu-id="0a807-128">Container GUID</span></span>      | <span data-ttu-id="0a807-129">**GUID \_ ContainerFormatWmp**</span><span class="sxs-lookup"><span data-stu-id="0a807-129">**GUID\_ContainerFormatWmp**</span></span>                                            |
| <span data-ttu-id="0a807-130">GUID decodificatore</span><span class="sxs-lookup"><span data-stu-id="0a807-130">Decoder GUID</span></span>        | <span data-ttu-id="0a807-131">**\_WICWMPDECODER CLSID**</span><span class="sxs-lookup"><span data-stu-id="0a807-131">**CLSID\_WICWmpDecoder**</span></span>                                                |
| <span data-ttu-id="0a807-132">GUID codificatore</span><span class="sxs-lookup"><span data-stu-id="0a807-132">Encoder GUID</span></span>        | <span data-ttu-id="0a807-133">**\_WICWMPENCODER CLSID**</span><span class="sxs-lookup"><span data-stu-id="0a807-133">**CLSID\_WICWmpEncoder**</span></span>                                                |
| <span data-ttu-id="0a807-134">Supporto del profilo</span><span class="sxs-lookup"><span data-stu-id="0a807-134">Profile Support</span></span>     | <span data-ttu-id="0a807-135">Il codificatore e il decodificatore supportano il profilo principale fino al livello 128.</span><span class="sxs-lookup"><span data-stu-id="0a807-135">The encoder and decoder support up to Main Profile and up to level 128.</span></span> |



 

## <a name="codec-features"></a><span data-ttu-id="0a807-136">Funzionalità di codec</span><span class="sxs-lookup"><span data-stu-id="0a807-136">Codec Features</span></span>

### <a name="high-dynamic-range"></a><span data-ttu-id="0a807-137">Intervallo dinamico elevato</span><span class="sxs-lookup"><span data-stu-id="0a807-137">High Dynamic Range</span></span>

<span data-ttu-id="0a807-138">Il formato JPEG XR supporta le immagini con intervallo dinamico elevato, usando i colori a virgola mobile o a virgola fissa.</span><span class="sxs-lookup"><span data-stu-id="0a807-138">JPEG XR supports high-dynamic range images, using floating-point or fixed-point colors.</span></span> <span data-ttu-id="0a807-139">In questi formati di colore, l'intervallo numerico di un pixel è maggiore dell'intervallo visibile, quindi è possibile modificare i colori sopra o sotto l'intervallo visibile durante le fasi di elaborazione intermedia.</span><span class="sxs-lookup"><span data-stu-id="0a807-139">In these color formats, the numerical range of a pixel is larger than the visible range, so you can adjust colors above or below the visible range during intermediate processing stages.</span></span>

-   <span data-ttu-id="0a807-140">A virgola fissa: in una rappresentazione a virgola fissa, 0 rappresenta il nero e 1,0 rappresenta la saturazione massima.</span><span class="sxs-lookup"><span data-stu-id="0a807-140">Fixed-point: In a fixed-point representation, 0 represents black and 1.0 represents maximum saturation.</span></span> <span data-ttu-id="0a807-141">Il codec JPEG XR supporta entrambi i formati a virgola fissa a 16 bit e a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="0a807-141">The JPEG XR codec supports both 16-bit and 32-bit fixed-point formats.</span></span> <span data-ttu-id="0a807-142">Per 16 bit, 1,0 = 0x2000h, che fornisce 13 bit per l'intervallo visibile \[ 0... 1 \] .</span><span class="sxs-lookup"><span data-stu-id="0a807-142">For 16-bit, 1.0 = 0x2000h, which gives 13 bits for the visible range \[0...1\].</span></span> <span data-ttu-id="0a807-143">L'intervallo totale è da-4,0 a + 3,999 e viene mappato in modo lineare.</span><span class="sxs-lookup"><span data-stu-id="0a807-143">The total range is –4.0 to +3.999, and is mapped linearly.</span></span> <span data-ttu-id="0a807-144">Per 32 bit, 1,0 = 0x01000000h, l'intervallo visibile è a 24 bit e l'intervallo totale è – 128 a + 127,999.</span><span class="sxs-lookup"><span data-stu-id="0a807-144">For 32-bit, 1.0 = 0x01000000h, the visible range is 24 bits, and the total range is –128 to +127.999.</span></span>
-   <span data-ttu-id="0a807-145">Virgola mobile: in una rappresentazione a virgola mobile, 0 rappresenta il nero e 1,0 rappresenta la saturazione massima.</span><span class="sxs-lookup"><span data-stu-id="0a807-145">Floating-point: In a floating-point representation, 0 represents black and 1.0 represents maximum saturation.</span></span> <span data-ttu-id="0a807-146">Il codec JPEG XR supporta sia i formati a virgola mobile a 16 bit che quelli a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="0a807-146">The JPEG XR codec supports both 16-bit and 32-bit floating-point formats.</span></span>

### <a name="tiles"></a><span data-ttu-id="0a807-147">Riquadri</span><span class="sxs-lookup"><span data-stu-id="0a807-147">Tiles</span></span>

<span data-ttu-id="0a807-148">Un frame può essere partizionato in sottoaree rettangolari denominate *riquadri*.</span><span class="sxs-lookup"><span data-stu-id="0a807-148">A frame can be partitioned into rectangular subregions called *tiles*.</span></span> <span data-ttu-id="0a807-149">Un riquadro è un'area di un'immagine che contiene matrici rettangolari di macroblocchi.</span><span class="sxs-lookup"><span data-stu-id="0a807-149">A tile is an area of a image that contains rectangular arrays of macroblocks.</span></span> <span data-ttu-id="0a807-150">I riquadri consentono di decodificare le aree dell'immagine senza elaborare l'intera immagine.</span><span class="sxs-lookup"><span data-stu-id="0a807-150">Tiles enable regions of the image to be decoded without processing the entire image.</span></span>

<span data-ttu-id="0a807-151">Durante la codifica, selezionare il numero di riquadri impostando le proprietà **HorizontalTileSlices** e **VerticalTileSlices** .</span><span class="sxs-lookup"><span data-stu-id="0a807-151">During encoding, select the number of tiles by setting the **HorizontalTileSlices** and **VerticalTileSlices** properties.</span></span> <span data-ttu-id="0a807-152">La dimensione minima del riquadro è 16 × 16 pixel.</span><span class="sxs-lookup"><span data-stu-id="0a807-152">The minimum tile size is 16 × 16 pixels.</span></span> <span data-ttu-id="0a807-153">Il codificatore regola il numero di riquadri per mantenere questa restrizione.</span><span class="sxs-lookup"><span data-stu-id="0a807-153">The encoder adjusts the number of tiles to maintain this restriction.</span></span> <span data-ttu-id="0a807-154">A ogni sezione è associato un overhead di archiviazione ed elaborazione, quindi è necessario considerare il numero di riquadri necessari per determinati scenari.</span><span class="sxs-lookup"><span data-stu-id="0a807-154">There is storage and processing overhead associated with each tile, so you should consider the number of tiles that are needed for particular scenarios.</span></span>

### <a name="image-stream-output"></a><span data-ttu-id="0a807-155">Output del flusso di immagini</span><span class="sxs-lookup"><span data-stu-id="0a807-155">Image Stream Output</span></span>

<span data-ttu-id="0a807-156">Lo standard JPEG-XR definisce due parti di un file JPEG-XR:</span><span class="sxs-lookup"><span data-stu-id="0a807-156">The JPEG-XR standard defines two parts of a JPEG-XR file:</span></span>

-   <span data-ttu-id="0a807-157">Flusso di bit dell'immagine, definito nel corpo dello standard.</span><span class="sxs-lookup"><span data-stu-id="0a807-157">The image bit stream, defined in the body of the standard.</span></span>
-   <span data-ttu-id="0a807-158">Contenitore di immagini.</span><span class="sxs-lookup"><span data-stu-id="0a807-158">The image container.</span></span> <span data-ttu-id="0a807-159">Il file contiene i metadati EXIF e XMP ed è definito nell'allegato A dello standard.</span><span class="sxs-lookup"><span data-stu-id="0a807-159">The file contains Exif and XMP metadata, and is defined in Annex A of the standard.</span></span>

<span data-ttu-id="0a807-160">È possibile, e consentito dallo standard, incorporare il flusso di immagini all'interno di un altro tipo di contenitore di file.</span><span class="sxs-lookup"><span data-stu-id="0a807-160">It is possible, and allowed by the standard, to embed the image stream inside another type of file container.</span></span> <span data-ttu-id="0a807-161">Il codificatore supporta una modalità di solo flusso, che restituisce il flusso di bit dell'immagine non elaborata senza contenitore di immagini.</span><span class="sxs-lookup"><span data-stu-id="0a807-161">The encoder supports a stream-only mode, which outputs the raw image bit stream with no image container.</span></span> <span data-ttu-id="0a807-162">Un'applicazione può archiviare il flusso di bit in un altro formato di contenitore.</span><span class="sxs-lookup"><span data-stu-id="0a807-162">An application can store the bit stream in some other container format.</span></span>

<span data-ttu-id="0a807-163">Per abilitare la modalità solo flusso, impostare la proprietà **StreamOnly** .</span><span class="sxs-lookup"><span data-stu-id="0a807-163">To enable stream-only mode, set the **StreamOnly** property.</span></span>

### <a name="image-quality-settings"></a><span data-ttu-id="0a807-164">Impostazioni qualità immagine</span><span class="sxs-lookup"><span data-stu-id="0a807-164">Image Quality Settings</span></span>

<span data-ttu-id="0a807-165">Diverse proprietà del codec controllano la qualità dell'immagine di output dal codificatore.</span><span class="sxs-lookup"><span data-stu-id="0a807-165">Several codec properties control the quality of the output image from the encoder.</span></span>

-   <span data-ttu-id="0a807-166">[ImageQuality](#imagequality) è una proprietà comune nei codec WIC.</span><span class="sxs-lookup"><span data-stu-id="0a807-166">[ImageQuality](#imagequality) is a property common across WIC codecs.</span></span> <span data-ttu-id="0a807-167">Specifica la qualità dell'immagine come singolo valore a virgola mobile da 0,0-1.0,</span><span class="sxs-lookup"><span data-stu-id="0a807-167">It specifies image quality as a single floating-point value from 0.0–1.0,</span></span>
-   <span data-ttu-id="0a807-168">Le proprietà [qualità](#image-quality-settings), [sovrapposizione](#overlap)e [sottocampionamento](#subsampling) offrono maggiore controllo sulle impostazioni di qualità.</span><span class="sxs-lookup"><span data-stu-id="0a807-168">The [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties give more control over the quality settings.</span></span>

<span data-ttu-id="0a807-169">Per utilizzare le proprietà [qualità](#image-quality-settings), [sovrapposizione](#overlap)e [sottocampionamento](#subsampling) , impostare la proprietà [UseCodecOptions](#usecodecoptions) su **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="0a807-169">To use the [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties, set the [UseCodecOptions](#usecodecoptions) property to **VARIANT\_TRUE**.</span></span>

<span data-ttu-id="0a807-170">Se [UseCodecOptions](#usecodecoptions) è **Variant \_ false** (**variante \_ false** è l'impostazione predefinita), il codificatore usa la proprietà [ImageQuality](#imagequality) .</span><span class="sxs-lookup"><span data-stu-id="0a807-170">If [UseCodecOptions](#usecodecoptions) is **VARIANT\_FALSE** (**VARIANT\_FALSE** is the default) the encoder uses the [ImageQuality](#imagequality) property.</span></span> <span data-ttu-id="0a807-171">Il codificatore esegue il mapping del valore di ImageQuality alla [qualità](#image-quality-settings), alla [sovrapposizione](#overlap)e al [sottocampionamento](#subsampling) tramite una tabella di ricerca.</span><span class="sxs-lookup"><span data-stu-id="0a807-171">The encoder maps the value of ImageQuality to [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) through a lookup table.</span></span>

<span data-ttu-id="0a807-172">Il codificatore non supporta la proprietà **CompressionQuality** .</span><span class="sxs-lookup"><span data-stu-id="0a807-172">The encoder does not support the **CompressionQuality** property.</span></span>

### <a name="compressed-domain-transcode"></a><span data-ttu-id="0a807-173">Transcodifica del dominio compresso</span><span class="sxs-lookup"><span data-stu-id="0a807-173">Compressed Domain Transcode</span></span>

<span data-ttu-id="0a807-174">Il codec JPEG XR può eseguire alcune trasformazioni di immagini senza decodificare effettivamente i dati compressi e ricodificarli.</span><span class="sxs-lookup"><span data-stu-id="0a807-174">The JPEG XR codec can perform certain image transformations without actually decoding the compressed data and re-encoding it.</span></span> <span data-ttu-id="0a807-175">Le operazioni di dominio compresso sono molto efficienti ed evitano una perdita di qualità aggiuntiva tipica quando si decodifica e si ricodifica un'immagine compressa con perdite di codice.</span><span class="sxs-lookup"><span data-stu-id="0a807-175">Compressed domain operations are very efficient and avoid any additional quality loss that is typical when you decode and re-encode a lossy-compressed image.</span></span>

<span data-ttu-id="0a807-176">Sono supportate le operazioni di dominio compresso seguenti:</span><span class="sxs-lookup"><span data-stu-id="0a807-176">The following compressed domain operations are supported:</span></span>

-   <span data-ttu-id="0a807-177">Ritagliare un'area dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="0a807-177">Crop a region of the image.</span></span>
-   <span data-ttu-id="0a807-178">Ruotare o capovolgere l'immagine.</span><span class="sxs-lookup"><span data-stu-id="0a807-178">Rotate or flip the image.</span></span>
-   <span data-ttu-id="0a807-179">Rimuovere i dati sulla frequenza per creare un file di immagine più piccolo.</span><span class="sxs-lookup"><span data-stu-id="0a807-179">Discard frequency data to create a smaller image file.</span></span>
-   <span data-ttu-id="0a807-180">Riorganizzare l'immagine tra l'ordine spaziale e quello di frequenza.</span><span class="sxs-lookup"><span data-stu-id="0a807-180">Reorganize the image between spatial and frequency order.</span></span>

<span data-ttu-id="0a807-181">Il codificatore JPEG XR USA la transcodifica del dominio compresso, se possibile, quando l'immagine di origine è un'immagine JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="0a807-181">The JPEG XR encoder uses compressed domain transcoding, if possible, when the source image is a JPEG XR image.</span></span> <span data-ttu-id="0a807-182">Quando il codificatore esegue un'operazione di dominio compresso, ignora le proprietà del codec seguenti: [AlphaQuality](#alphaquality), [ImageQuality](#imagequality), [InterleavedAlpha](#interleavedalpha),[sovrapposizione](#overlap)senza [perdita di perdite](#lossless)e [qualità](#image-quality-settings).</span><span class="sxs-lookup"><span data-stu-id="0a807-182">When the encoder performs a compressed domain operation, it ignores the following codec properties: [AlphaQuality](#alphaquality), [ImageQuality](#imagequality), [InterleavedAlpha](#interleavedalpha), [Lossless](#lossless)[Overlap](#overlap), and [Quality](#image-quality-settings).</span></span> <span data-ttu-id="0a807-183">Se sono presenti le proprietà [HorizontalTileSlices](/windows) e [VerticalTileSlices](/windows) , è necessario impostarle su zero.</span><span class="sxs-lookup"><span data-stu-id="0a807-183">If the [HorizontalTileSlices](/windows) and [VerticalTileSlices](/windows) properties are present, you must set them to zero.</span></span> <span data-ttu-id="0a807-184">Non è possibile modificare le dimensioni del riquadro di un'immagine come parte di una transcodifica del dominio compresso.</span><span class="sxs-lookup"><span data-stu-id="0a807-184">You cannot change the tile size of an image as part of a compressed domain transcode.</span></span>

<span data-ttu-id="0a807-185">Nell'elenco seguente viene descritto come eseguire le trasformazioni di immagine.</span><span class="sxs-lookup"><span data-stu-id="0a807-185">The follow list describes how to perform the image transformations.</span></span>

-   <span data-ttu-id="0a807-186">Per ritagliare l'immagine, impostare l'area desiderata nel parametro [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) del metodo **WriteSource** .</span><span class="sxs-lookup"><span data-stu-id="0a807-186">To crop the image, set the desired region in the [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) parameter of the **WriteSource** method.</span></span>
-   <span data-ttu-id="0a807-187">Per ruotare o capovolgere l'immagine, impostare la proprietà [BitmapTransform](#bitmaptransform) .</span><span class="sxs-lookup"><span data-stu-id="0a807-187">To rotate or flip the image, set the [BitmapTransform](#bitmaptransform) property.</span></span>
-   <span data-ttu-id="0a807-188">Per eliminare i dati relativi alla frequenza nell'immagine, impostare la proprietà [ImageDataDiscard](#imagedatadiscard) .</span><span class="sxs-lookup"><span data-stu-id="0a807-188">To discard frequency data in the image, set the [ImageDataDiscard](#imagedatadiscard) property.</span></span> <span data-ttu-id="0a807-189">Per eliminare i dati relativi alla frequenza nel canale alfa, impostare la proprietà [AlphaDataDiscard](#alphadatadiscard) .</span><span class="sxs-lookup"><span data-stu-id="0a807-189">To discard frequency data in the alpha channel, set the [AlphaDataDiscard](#alphadatadiscard) property.</span></span> <span data-ttu-id="0a807-190">L'eliminazione dei dati di frequenza riduce le dimensioni del file codificato e può ridurre la risoluzione.</span><span class="sxs-lookup"><span data-stu-id="0a807-190">Discarding frequency data reduces the encoded file size and can reduce the resolution.</span></span>
-   <span data-ttu-id="0a807-191">Per modificare l'organizzazione delle immagini tra frequenza e ordinamento spaziale, impostare la proprietà [FrequencyOrdering](/windows) .</span><span class="sxs-lookup"><span data-stu-id="0a807-191">To change the image organization between frequency and spatial ordering, set the [FrequencyOrdering](/windows) property.</span></span>

<span data-ttu-id="0a807-192">Per disabilitare la transcodifica del dominio compresso e forzare il codificatore a codificare nuovamente l'immagine, impostare [UseCodecOptions](#usecodecoptions) su **Variant \_ true** e impostare [CompressedDomainTranscode](#compresseddomaintranscode) su **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="0a807-192">To disable compressed domain transcode and force the encoder to re-encode the image, set the [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE** and set [CompressedDomainTranscode](#compresseddomaintranscode) to **VARIANT\_FALSE**.</span></span>

## <a name="encoder-options"></a><span data-ttu-id="0a807-193">Opzioni del codificatore</span><span class="sxs-lookup"><span data-stu-id="0a807-193">Encoder Options</span></span>

<span data-ttu-id="0a807-194">Per impostare le proprietà di codifica, utilizzare l'interfaccia [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0a807-194">To set encoding properties, use the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface.</span></span> <span data-ttu-id="0a807-195">Per ulteriori informazioni, vedere [Cenni preliminari sulla codifica](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="0a807-195">For more information, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="0a807-196">Nell'elenco seguente vengono specificate le opzioni del codificatore.</span><span class="sxs-lookup"><span data-stu-id="0a807-196">The following list specifies the encoder options.</span></span>

-   [<span data-ttu-id="0a807-197">AlphaDataDiscard</span><span class="sxs-lookup"><span data-stu-id="0a807-197">AlphaDataDiscard</span></span>](#alphadatadiscard)
-   [<span data-ttu-id="0a807-198">AlphaQuality</span><span class="sxs-lookup"><span data-stu-id="0a807-198">AlphaQuality</span></span>](#alphaquality)
-   [<span data-ttu-id="0a807-199">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="0a807-199">BitmapTransform</span></span>](#bitmaptransform)
-   [<span data-ttu-id="0a807-200">CompressedDomainTranscode</span><span class="sxs-lookup"><span data-stu-id="0a807-200">CompressedDomainTranscode</span></span>](#compresseddomaintranscode)
-   [<span data-ttu-id="0a807-201">FrequencyOrder</span><span class="sxs-lookup"><span data-stu-id="0a807-201">FrequencyOrder</span></span>](#frequencyorder)
-   [<span data-ttu-id="0a807-202">HorizontalTileSlices</span><span class="sxs-lookup"><span data-stu-id="0a807-202">HorizontalTileSlices</span></span>](#horizontaltileslices)
-   [<span data-ttu-id="0a807-203">IgnoreOverlap</span><span class="sxs-lookup"><span data-stu-id="0a807-203">IgnoreOverlap</span></span>](#ignoreoverlap)
-   [<span data-ttu-id="0a807-204">ImageDataDiscard</span><span class="sxs-lookup"><span data-stu-id="0a807-204">ImageDataDiscard</span></span>](#imagedatadiscard)
-   [<span data-ttu-id="0a807-205">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="0a807-205">ImageQuality</span></span>](#imagequality)
-   [<span data-ttu-id="0a807-206">InterleavedAlpha</span><span class="sxs-lookup"><span data-stu-id="0a807-206">InterleavedAlpha</span></span>](#interleavedalpha)
-   [<span data-ttu-id="0a807-207">Lossless</span><span class="sxs-lookup"><span data-stu-id="0a807-207">Lossless</span></span>](#lossless)
-   [<span data-ttu-id="0a807-208">Overlap</span><span class="sxs-lookup"><span data-stu-id="0a807-208">Overlap</span></span>](#overlap)
-   [<span data-ttu-id="0a807-209">Codifica</span><span class="sxs-lookup"><span data-stu-id="0a807-209">ProgressiveMode</span></span>](#progressivemode)
-   [<span data-ttu-id="0a807-210">Qualità</span><span class="sxs-lookup"><span data-stu-id="0a807-210">Quality</span></span>](#image-quality-settings)
-   [<span data-ttu-id="0a807-211">StreamOnly</span><span class="sxs-lookup"><span data-stu-id="0a807-211">StreamOnly</span></span>](#streamonly)
-   [<span data-ttu-id="0a807-212">Sottocampionamento</span><span class="sxs-lookup"><span data-stu-id="0a807-212">Subsampling</span></span>](#subsampling)
-   [<span data-ttu-id="0a807-213">UseCodecOptions</span><span class="sxs-lookup"><span data-stu-id="0a807-213">UseCodecOptions</span></span>](#usecodecoptions)
-   [<span data-ttu-id="0a807-214">VerticalTileSlices</span><span class="sxs-lookup"><span data-stu-id="0a807-214">VerticalTileSlices</span></span>](#verticaltileslices)

### <a name="alphadatadiscard"></a><span data-ttu-id="0a807-215">AlphaDataDiscard</span><span class="sxs-lookup"><span data-stu-id="0a807-215">AlphaDataDiscard</span></span>

<span data-ttu-id="0a807-216">Imposta la quantità di dati di frequenza alfa da eliminare durante una transcodifica del dominio compresso.</span><span class="sxs-lookup"><span data-stu-id="0a807-216">Sets the amount of alpha frequency data to discard during a compressed domain transcode.</span></span>



| <span data-ttu-id="0a807-217">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0a807-217">Data type</span></span> | <span data-ttu-id="0a807-218">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0a807-218">VARTYPE</span></span>     | <span data-ttu-id="0a807-219">Range</span><span class="sxs-lookup"><span data-stu-id="0a807-219">Range</span></span> | <span data-ttu-id="0a807-220">Predefinito</span><span class="sxs-lookup"><span data-stu-id="0a807-220">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="0a807-221">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="0a807-221">**UCHAR**</span></span> | <span data-ttu-id="0a807-222">**\_Ui1 VT**</span><span class="sxs-lookup"><span data-stu-id="0a807-222">**VT\_UI1**</span></span> | <span data-ttu-id="0a807-223">0 – 4</span><span class="sxs-lookup"><span data-stu-id="0a807-223">0–4</span></span>   | <span data-ttu-id="0a807-224">nessuno</span><span class="sxs-lookup"><span data-stu-id="0a807-224">None</span></span>    |



 

<span data-ttu-id="0a807-225">Questa proprietà si applica solo se la proprietà [CompressedDomainTranscode](#compresseddomaintranscode) è impostata su **Variant \_ true** e l'immagine contiene un canale alfa planare o un canale alfa con interfoliazione; in caso contrario, viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="0a807-225">This property applies only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE** and the image contains either a planar alpha channel or interleaved alpha channel; otherwise it is ignored.</span></span>

<span data-ttu-id="0a807-226">Per le immagini che contengono un canale alfa planare, i valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="0a807-226">For images that contain a planar alpha channel, the following values are valid.</span></span>



| <span data-ttu-id="0a807-227">Valore</span><span class="sxs-lookup"><span data-stu-id="0a807-227">Value</span></span> | <span data-ttu-id="0a807-228">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a807-228">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a807-229">0</span><span class="sxs-lookup"><span data-stu-id="0a807-229">0</span></span>     | <span data-ttu-id="0a807-230">Non viene eliminato nessun dato di frequenza dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="0a807-230">No image frequency data is discarded.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="0a807-231">1</span><span class="sxs-lookup"><span data-stu-id="0a807-231">1</span></span>     | <span data-ttu-id="0a807-232">I FlexBits vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="0a807-232">The flexbits are discarded.</span></span> <span data-ttu-id="0a807-233">In questo modo si riduce arbitrariamente la qualità del canale alfa planare per l'immagine transcodificata.</span><span class="sxs-lookup"><span data-stu-id="0a807-233">This arbitrarily reduces the quality of the planar alpha channel for the transcoded image.</span></span> <span data-ttu-id="0a807-234">, senza una modifica nella risoluzione effettiva.</span><span class="sxs-lookup"><span data-stu-id="0a807-234">, without a change in the effective resolution.</span></span> <span data-ttu-id="0a807-235">La riduzione esatta delle dimensioni e della qualità dei file dipende da numerosi fattori e non può essere specificata esattamente.</span><span class="sxs-lookup"><span data-stu-id="0a807-235">The exact reduction in file size and quality depends on numerous factors and cannot be exactly specified.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="0a807-236">2</span><span class="sxs-lookup"><span data-stu-id="0a807-236">2</span></span>     | <span data-ttu-id="0a807-237">La banda di dati con frequenza di passaggio superiore viene scartata, incluso FlexBits.</span><span class="sxs-lookup"><span data-stu-id="0a807-237">The high-pass frequency data band is discarded, including the flexbits.</span></span> <span data-ttu-id="0a807-238">Questo consente di ridurre in modo efficace la risoluzione del canale alfa planare per un fattore di 4 in entrambe le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="0a807-238">This effectively reduces the resolution of the planar alpha channel by a factor of 4 in both dimensions.</span></span> <span data-ttu-id="0a807-239">Le dimensioni effettive dell'immagine transcodificata rimangono invariate, ma l'immagine perde tutti i dettagli in ogni blocco 4x4 di pixel del canale alfa.</span><span class="sxs-lookup"><span data-stu-id="0a807-239">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 4x4 block of alpha-channel pixels.</span></span> <span data-ttu-id="0a807-240">In genere, è consigliabile impostare questo valore solo quando la proprietà [ImageDataDiscard](#imagedatadiscard) ha lo stesso valore.</span><span class="sxs-lookup"><span data-stu-id="0a807-240">Typically, you should set this value only when the [ImageDataDiscard](#imagedatadiscard) property has the same value.</span></span>                            |
| <span data-ttu-id="0a807-241">3</span><span class="sxs-lookup"><span data-stu-id="0a807-241">3</span></span>     | <span data-ttu-id="0a807-242">Entrambe le bande di dati con frequenza superata e bassa passano, inclusa la FlexBits.</span><span class="sxs-lookup"><span data-stu-id="0a807-242">Both the high-pass and low-pass frequency data bands are discarded, including the flexbits.</span></span> <span data-ttu-id="0a807-243">Questo ffectively riduce la risoluzione del canale alfa planare per un fattore di 16 in entrambe le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="0a807-243">This ffectively reduces the resolution of the planar alpha channel by a factor of 16 in both dimensions.</span></span> <span data-ttu-id="0a807-244">Le dimensioni effettive dell'immagine transcodificata rimangono invariate, ma l'immagine perde tutti i dettagli in ogni 16x16 macroblocco dei pixel del canale alfa.</span><span class="sxs-lookup"><span data-stu-id="0a807-244">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 16x16 macroblock of alpha-channel pixels.</span></span> <span data-ttu-id="0a807-245">In genere, è consigliabile impostare questo valore solo quando la proprietà [ImageDataDiscard](#imagedatadiscard) ha lo stesso valore.</span><span class="sxs-lookup"><span data-stu-id="0a807-245">Typically, you should set this value only when the [ImageDataDiscard](#imagedatadiscard) property has the same value.</span></span> |
| <span data-ttu-id="0a807-246">4</span><span class="sxs-lookup"><span data-stu-id="0a807-246">4</span></span>     | <span data-ttu-id="0a807-247">Il canale alfa viene eliminato completamente.</span><span class="sxs-lookup"><span data-stu-id="0a807-247">The alpha channel is completely discarded.</span></span> <span data-ttu-id="0a807-248">Il formato pixel dell'immagine transcodificata viene modificato per riflettere la rimozione del canale alfa.</span><span class="sxs-lookup"><span data-stu-id="0a807-248">The pixel format of the transcoded image is changed to reflect the removal of the alpha channel.</span></span>                                                                                                                                                                                                                                                                                                                                |



 

<span data-ttu-id="0a807-249">Per le immagini che contengono un canale alfa con interfoliazione, il valore seguente è valido.</span><span class="sxs-lookup"><span data-stu-id="0a807-249">For images that contain an interleaved alpha channel, the following value is valid.</span></span>



| <span data-ttu-id="0a807-250">Valore</span><span class="sxs-lookup"><span data-stu-id="0a807-250">Value</span></span> | <span data-ttu-id="0a807-251">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a807-251">Description</span></span>                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a807-252">4</span><span class="sxs-lookup"><span data-stu-id="0a807-252">4</span></span>     | <span data-ttu-id="0a807-253">Il canale alfa viene eliminato completamente.</span><span class="sxs-lookup"><span data-stu-id="0a807-253">The alpha channel is completely discarded.</span></span> <span data-ttu-id="0a807-254">Il formato pixel dell'immagine transcodificata viene modificato per riflettere la rimozione del canale alfa.</span><span class="sxs-lookup"><span data-stu-id="0a807-254">The pixel format of the transcoded image is changed to reflect the removal of the alpha channel.</span></span> |



 

<span data-ttu-id="0a807-255">Per l'alfa con interfoliazione, a meno che questa proprietà non sia impostata su 4, il canale alfa viene elaborato allo stesso modo dei dati dell'immagine, in base al valore della proprietà [ImageDataDiscard](#imagedatadiscard) .</span><span class="sxs-lookup"><span data-stu-id="0a807-255">For interleaved alpha, unless this property is set to 4, the alpha channel is processed the same as the image data, according to the value of the [ImageDataDiscard](#imagedatadiscard) property.</span></span>

### <a name="alphaquality"></a><span data-ttu-id="0a807-256">AlphaQuality</span><span class="sxs-lookup"><span data-stu-id="0a807-256">AlphaQuality</span></span>

<span data-ttu-id="0a807-257">Imposta la qualità di compressione per l'immagine del canale alfa planare.</span><span class="sxs-lookup"><span data-stu-id="0a807-257">Sets the compression quality for the planar alpha channel image.</span></span>



| <span data-ttu-id="0a807-258">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0a807-258">Data type</span></span> | <span data-ttu-id="0a807-259">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0a807-259">VARTYPE</span></span>     | <span data-ttu-id="0a807-260">Range</span><span class="sxs-lookup"><span data-stu-id="0a807-260">Range</span></span> | <span data-ttu-id="0a807-261">Predefinito</span><span class="sxs-lookup"><span data-stu-id="0a807-261">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="0a807-262">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="0a807-262">**UCHAR**</span></span> | <span data-ttu-id="0a807-263">**\_Ui1 VT**</span><span class="sxs-lookup"><span data-stu-id="0a807-263">**VT\_UI1**</span></span> | <span data-ttu-id="0a807-264">da 1 a 255</span><span class="sxs-lookup"><span data-stu-id="0a807-264">1–255</span></span> | <span data-ttu-id="0a807-265">1</span><span class="sxs-lookup"><span data-stu-id="0a807-265">1</span></span>       |



 

<span data-ttu-id="0a807-266">Questa proprietà si applica quando l'immagine ha un canale alfa e la proprietà [InterleavedAlpha](#interleavedalpha) è **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="0a807-266">This property applies when the image has an alpha channel and the [InterleavedAlpha](#interleavedalpha) property is **VARIANT\_FALSE**.</span></span> <span data-ttu-id="0a807-267">Il valore 1 indica la modalità lossless.</span><span class="sxs-lookup"><span data-stu-id="0a807-267">The value 1 indicates lossless mode.</span></span> <span data-ttu-id="0a807-268">L'aumento dei valori comporta percentuali di compressione più elevate e una minore qualità dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="0a807-268">Increasing values result in higher compression ratios and lower image quality.</span></span>

### <a name="bitmaptransform"></a><span data-ttu-id="0a807-269">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="0a807-269">BitmapTransform</span></span>

<span data-ttu-id="0a807-270">Specifica se l'immagine viene ruotata o capovolta quando viene decodificata.</span><span class="sxs-lookup"><span data-stu-id="0a807-270">Specifies whether the image is rotated or flipped when decoded.</span></span>



| <span data-ttu-id="0a807-271">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0a807-271">Data type</span></span> | <span data-ttu-id="0a807-272">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0a807-272">VARTYPE</span></span>     | <span data-ttu-id="0a807-273">Range</span><span class="sxs-lookup"><span data-stu-id="0a807-273">Range</span></span>                                                                     | <span data-ttu-id="0a807-274">Predefinito</span><span class="sxs-lookup"><span data-stu-id="0a807-274">Default</span></span>                       |
|-----------|-------------|---------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="0a807-275">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="0a807-275">**UCHAR**</span></span> | <span data-ttu-id="0a807-276">**\_Ui1 VT**</span><span class="sxs-lookup"><span data-stu-id="0a807-276">**VT\_UI1**</span></span> | [<span data-ttu-id="0a807-277">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="0a807-277">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | <span data-ttu-id="0a807-278">**WICBitmapTransformRotate0**</span><span class="sxs-lookup"><span data-stu-id="0a807-278">**WICBitmapTransformRotate0**</span></span> |



 

### <a name="compresseddomaintranscode"></a><span data-ttu-id="0a807-279">CompressedDomainTranscode</span><span class="sxs-lookup"><span data-stu-id="0a807-279">CompressedDomainTranscode</span></span>

<span data-ttu-id="0a807-280">Abilita o Disabilita la transcodifica del dominio compresso.</span><span class="sxs-lookup"><span data-stu-id="0a807-280">Enables or disables compressed domain transcoding.</span></span>



| <span data-ttu-id="0a807-281">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0a807-281">Data type</span></span>         | <span data-ttu-id="0a807-282">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0a807-282">VARTYPE</span></span>      | <span data-ttu-id="0a807-283">Predefinito</span><span class="sxs-lookup"><span data-stu-id="0a807-283">Default</span></span>           |
|-------------------|--------------|-------------------|
| <span data-ttu-id="0a807-284">**\_bool Variant**</span><span class="sxs-lookup"><span data-stu-id="0a807-284">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="0a807-285">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="0a807-285">**VT\_BOOL**</span></span> | <span data-ttu-id="0a807-286">**VARIANT \_ true**</span><span class="sxs-lookup"><span data-stu-id="0a807-286">**VARIANT\_TRUE**</span></span> |



 

<span data-ttu-id="0a807-287">Per disabilitare le operazioni di dominio compresso, impostare questa proprietà su **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="0a807-287">To disable compressed domain operations, set this property to **VARIANT\_FALSE**.</span></span>

### <a name="frequencyorder"></a><span data-ttu-id="0a807-288">FrequencyOrder</span><span class="sxs-lookup"><span data-stu-id="0a807-288">FrequencyOrder</span></span>

<span data-ttu-id="0a807-289">Abilita la codifica in ordine di frequenza.</span><span class="sxs-lookup"><span data-stu-id="0a807-289">Enables encoding in frequency order.</span></span> <span data-ttu-id="0a807-290">Le implementazioni del dispositivo dei codificatori JPEG XR possono organizzare un file in ordine spaziale per ridurre la memoria necessaria durante la codifica.</span><span class="sxs-lookup"><span data-stu-id="0a807-290">Device implementations of JPEG XR encoders can organize a file in spatial order to reduce the memory required during encoding.</span></span>



| <span data-ttu-id="0a807-291">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0a807-291">Data type</span></span>         | <span data-ttu-id="0a807-292">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0a807-292">VARTYPE</span></span>      | <span data-ttu-id="0a807-293">Predefinito</span><span class="sxs-lookup"><span data-stu-id="0a807-293">Default</span></span>           |
|-------------------|--------------|-------------------|
| <span data-ttu-id="0a807-294">**\_bool Variant**</span><span class="sxs-lookup"><span data-stu-id="0a807-294">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="0a807-295">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="0a807-295">**VT\_BOOL**</span></span> | <span data-ttu-id="0a807-296">**VARIANT \_ true**</span><span class="sxs-lookup"><span data-stu-id="0a807-296">**VARIANT\_TRUE**</span></span> |



 

-   <span data-ttu-id="0a807-297">**Variante \_ TRUE**: ordine di frequenza.</span><span class="sxs-lookup"><span data-stu-id="0a807-297">**VARIANT\_TRUE**: Frequency order.</span></span> <span data-ttu-id="0a807-298">I dati con frequenza più bassa vengono visualizzati per primi nel file e il contenuto dell'immagine viene raggruppato in base alla relativa frequenza anziché all'orientamento spaziale.</span><span class="sxs-lookup"><span data-stu-id="0a807-298">The lowest frequency data appears first in the file, and image content is grouped by its frequency rather than its spatial orientation.</span></span> <span data-ttu-id="0a807-299">L'organizzazione di un file in base all'ordine di frequenza offre le migliori prestazioni per qualsiasi decodifica basata sulla frequenza.</span><span class="sxs-lookup"><span data-stu-id="0a807-299">Organizing a file by frequency order provides the best performance for any frequency-based decoding.</span></span>
-   <span data-ttu-id="0a807-300">**Variante \_ FALSE**: ordine spaziale.</span><span class="sxs-lookup"><span data-stu-id="0a807-300">**VARIANT\_FALSE**: Spatial order.</span></span> <span data-ttu-id="0a807-301">L'ordine spaziale riduce la memoria necessaria durante la codifica</span><span class="sxs-lookup"><span data-stu-id="0a807-301">Spatial order reduces the memory required during encoding</span></span>

<span data-ttu-id="0a807-302">È consigliabile utilizzare l'ordine di frequenza, a meno che non si disponga di motivi di prestazioni o specifici dell'applicazione per utilizzare l'ordine spaziale.</span><span class="sxs-lookup"><span data-stu-id="0a807-302">Frequency order is recommended unless you have performance or application-specific reasons to use spatial order.</span></span>

### <a name="horizontaltileslices"></a><span data-ttu-id="0a807-303">HorizontalTileSlices</span><span class="sxs-lookup"><span data-stu-id="0a807-303">HorizontalTileSlices</span></span>

<span data-ttu-id="0a807-304">Imposta il numero di riquadri orizzontali.</span><span class="sxs-lookup"><span data-stu-id="0a807-304">Sets the number of horizontal tiles.</span></span>



| <span data-ttu-id="0a807-305">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0a807-305">Data type</span></span>  | <span data-ttu-id="0a807-306">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0a807-306">VARTYPE</span></span>     | <span data-ttu-id="0a807-307">Range</span><span class="sxs-lookup"><span data-stu-id="0a807-307">Range</span></span>  | <span data-ttu-id="0a807-308">Predefinito</span><span class="sxs-lookup"><span data-stu-id="0a807-308">Default</span></span>                      |
|------------|-------------|--------|------------------------------|
| <span data-ttu-id="0a807-309">**USHORT**</span><span class="sxs-lookup"><span data-stu-id="0a807-309">**USHORT**</span></span> | <span data-ttu-id="0a807-310">**\_UI2 VT**</span><span class="sxs-lookup"><span data-stu-id="0a807-310">**VT\_UI2**</span></span> | <span data-ttu-id="0a807-311">0 – 4095</span><span class="sxs-lookup"><span data-stu-id="0a807-311">0–4095</span></span> | <span data-ttu-id="0a807-312">(larghezza immagine-1)  >> 8</span><span class="sxs-lookup"><span data-stu-id="0a807-312">(image width – 1) >> 8</span></span> |



 

<span data-ttu-id="0a807-313">Il valore è il numero di suddivisioni orizzontali; ovvero il numero di riquadri orizzontali-1.</span><span class="sxs-lookup"><span data-stu-id="0a807-313">The value is the number of horizontal subdivisions; that is, the number of horizontal tiles – 1.</span></span>

### <a name="ignoreoverlap"></a><span data-ttu-id="0a807-314">IgnoreOverlap</span><span class="sxs-lookup"><span data-stu-id="0a807-314">IgnoreOverlap</span></span>

<span data-ttu-id="0a807-315">Specifica il modo in cui il codificatore gestisce i limiti del riquadro durante una transcodifica del dominio compresso.</span><span class="sxs-lookup"><span data-stu-id="0a807-315">Specifies how the encoder handles tile boundaries during a compressed domain transcode.</span></span>



| <span data-ttu-id="0a807-316">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0a807-316">Data type</span></span>         | <span data-ttu-id="0a807-317">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0a807-317">VARTYPE</span></span>      | <span data-ttu-id="0a807-318">Predefinito</span><span class="sxs-lookup"><span data-stu-id="0a807-318">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="0a807-319">**\_bool Variant**</span><span class="sxs-lookup"><span data-stu-id="0a807-319">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="0a807-320">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="0a807-320">**VT\_BOOL**</span></span> | <span data-ttu-id="0a807-321">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="0a807-321">**VARIANT\_FALSE**</span></span> |



 

<span data-ttu-id="0a807-322">Questa proprietà viene applicata solo se la proprietà [CompressedDomainTranscode](#compresseddomaintranscode) è impostata su **Variant \_ true** e viene eseguita una transcodifica dell'area secondaria di esattamente uno o più riquadri.</span><span class="sxs-lookup"><span data-stu-id="0a807-322">This property is applied only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE** and a sub-region transcode of exactly one or more tiles is performed.</span></span>

<span data-ttu-id="0a807-323">L'operazione predefinita per la transcodifica di un'area consiste nell'espandere l'area richiesta in modo da includere i pixel circostanti necessari per la decodifica di sovrapposizione dei bordi dell'area.</span><span class="sxs-lookup"><span data-stu-id="0a807-323">The default operation for a region transcode is to expand the requested region to include the surrounding pixels that are required for overlap decoding of the region edges.</span></span> <span data-ttu-id="0a807-324">Se questa proprietà è impostata su **Variant \_ true**, il codec ignora i pixel circostanti e vengono estratti solo il riquadro o i riquadri selezionati.</span><span class="sxs-lookup"><span data-stu-id="0a807-324">If this property is set to **VARIANT\_TRUE**, the codec ignores the surrounding pixels, and only the selected tile or tiles are extracted.</span></span> <span data-ttu-id="0a807-325">Se l'immagine di origine non è affiancata o se l'area richiesta include riquadri parziali, questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="0a807-325">If the source image is not tiled or if the requested region includes partial tiles, this parameter is ignored.</span></span>

### <a name="imagedatadiscard"></a><span data-ttu-id="0a807-326">ImageDataDiscard</span><span class="sxs-lookup"><span data-stu-id="0a807-326">ImageDataDiscard</span></span>

<span data-ttu-id="0a807-327">Imposta la quantità di dati relativi alla frequenza delle immagini da eliminare durante una transcodifica del dominio compresso.</span><span class="sxs-lookup"><span data-stu-id="0a807-327">Sets the amount of image frequency data to discard during a compressed domain transcode.</span></span>



| <span data-ttu-id="0a807-328">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0a807-328">Data type</span></span> | <span data-ttu-id="0a807-329">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0a807-329">VARTYPE</span></span>     | <span data-ttu-id="0a807-330">Range</span><span class="sxs-lookup"><span data-stu-id="0a807-330">Range</span></span> | <span data-ttu-id="0a807-331">Predefinito</span><span class="sxs-lookup"><span data-stu-id="0a807-331">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="0a807-332">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="0a807-332">**UCHAR**</span></span> | <span data-ttu-id="0a807-333">**\_Ui1 VT**</span><span class="sxs-lookup"><span data-stu-id="0a807-333">**VT\_UI1**</span></span> | <span data-ttu-id="0a807-334">0 – 3</span><span class="sxs-lookup"><span data-stu-id="0a807-334">0–3</span></span>   | <span data-ttu-id="0a807-335">0</span><span class="sxs-lookup"><span data-stu-id="0a807-335">0</span></span>       |



 

<span data-ttu-id="0a807-336">Questa proprietà viene applicata solo se la proprietà [CompressedDomainTranscode](#compresseddomaintranscode) è impostata su **Variant \_ true**. in caso contrario, viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="0a807-336">This property applies only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE**; otherwise it is ignored.</span></span>



| <span data-ttu-id="0a807-337">Valore</span><span class="sxs-lookup"><span data-stu-id="0a807-337">Value</span></span> | <span data-ttu-id="0a807-338">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a807-338">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a807-339">0</span><span class="sxs-lookup"><span data-stu-id="0a807-339">0</span></span>     | <span data-ttu-id="0a807-340">Non viene eliminato nessun dato di frequenza dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="0a807-340">No image frequency data is discarded.</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="0a807-341">1</span><span class="sxs-lookup"><span data-stu-id="0a807-341">1</span></span>     | <span data-ttu-id="0a807-342">I FlexBits vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="0a807-342">The flexbits are discarded.</span></span> <span data-ttu-id="0a807-343">In questo modo si riduce arbitrariamente la qualità dell'immagine transcodificata senza modificare la risoluzione effettiva dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="0a807-343">This arbitrarily reduces the quality of the transcoded image without changing the effective resolution of the image.</span></span> <span data-ttu-id="0a807-344">La riduzione esatta delle dimensioni e della qualità dei file dipende da numerosi fattori e non può essere specificata esattamente.</span><span class="sxs-lookup"><span data-stu-id="0a807-344">The exact reduction in file size and quality depends on numerous factors and cannot be exactly specified.</span></span> <span data-ttu-id="0a807-345">Questo valore restituisce un errore specificato per un canale alfa con interfoliazione.</span><span class="sxs-lookup"><span data-stu-id="0a807-345">This value returns an error specified for an interleaved alpha channel.</span></span>                                                                                |
| <span data-ttu-id="0a807-346">2</span><span class="sxs-lookup"><span data-stu-id="0a807-346">2</span></span>     | <span data-ttu-id="0a807-347">La banda di dati con frequenza di passaggio superiore viene scartata, incluso FlexBits.</span><span class="sxs-lookup"><span data-stu-id="0a807-347">The high-pass frequency data band is discarded, including the flexbits.</span></span> <span data-ttu-id="0a807-348">In questo modo si riduce la risoluzione dell'immagine transcodificata in base a un fattore 4 in entrambe le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="0a807-348">This reduces the resolution of the transcoded image by a factor of 4 in both dimensions.</span></span> <span data-ttu-id="0a807-349">Le dimensioni effettive dell'immagine transcodificata rimangono invariate, ma l'immagine perde tutti i dettagli in ogni blocco di pixel 4x4.</span><span class="sxs-lookup"><span data-stu-id="0a807-349">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 4x4 block of pixels.</span></span> <span data-ttu-id="0a807-350">Pertanto, l'immagine transcodificata deve essere downsampling di conseguenza ogni volta che viene decodificata.</span><span class="sxs-lookup"><span data-stu-id="0a807-350">Therefore, the transcoded image should be downsampled accordingly whenever it is decoded.</span></span>                             |
| <span data-ttu-id="0a807-351">3</span><span class="sxs-lookup"><span data-stu-id="0a807-351">3</span></span>     | <span data-ttu-id="0a807-352">Entrambe le bande di dati con frequenza superata e bassa passano, inclusa la FlexBits.</span><span class="sxs-lookup"><span data-stu-id="0a807-352">Both the high-pass and low-pass frequency data bands are discarded, including the flexbits.</span></span> <span data-ttu-id="0a807-353">In questo modo si riduce la risoluzione dell'immagine transcodificata in base a un fattore pari a 16 in entrambe le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="0a807-353">This reduces the resolution of the transcoded image by a factor of 16 in both dimensions.</span></span> <span data-ttu-id="0a807-354">Le dimensioni effettive dell'immagine transcodificata rimangono invariate, ma l'immagine perde tutti i dettagli in ogni 16x16 macroblocco di pixel.</span><span class="sxs-lookup"><span data-stu-id="0a807-354">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 16x16 macroblock of pixels.</span></span> <span data-ttu-id="0a807-355">Pertanto, l'immagine transcodificata deve essere downsampling di conseguenza ogni volta che viene decodificata.</span><span class="sxs-lookup"><span data-stu-id="0a807-355">Therefore, the transcoded image should be downsampled accordingly whenever it is decoded.</span></span> |



 

<span data-ttu-id="0a807-356">Se l'immagine contiene un canale alfa Interleaved, il valore di [ImageDataDiscard](#imagedatadiscard) viene applicato al canale alfa, a meno che la proprietà [AlphaDataDiscard](#alphadatadiscard) sia impostata su 4, nel qual caso il canale alfa viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="0a807-356">If the image contains an interleaved alpha channel, the value of [ImageDataDiscard](#imagedatadiscard) is applied to the alpha channel unless the [AlphaDataDiscard](#alphadatadiscard) property is set to 4, in which case the alpha channel is discarded.</span></span>

<span data-ttu-id="0a807-357">Per il piano alfa planare, i dati relativi alla frequenza eliminati sono controllati dalla proprietà [AlphaDataDiscard](#alphadatadiscard) .</span><span class="sxs-lookup"><span data-stu-id="0a807-357">For planar alpha, the frequency data that is discarded is controlled by the [AlphaDataDiscard](#alphadatadiscard) property.</span></span>

### <a name="imagequality"></a><span data-ttu-id="0a807-358">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="0a807-358">ImageQuality</span></span>

<span data-ttu-id="0a807-359">Imposta la qualità dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="0a807-359">Sets the image quality.</span></span>



| <span data-ttu-id="0a807-360">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0a807-360">Data type</span></span> | <span data-ttu-id="0a807-361">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0a807-361">VARTYPE</span></span>    | <span data-ttu-id="0a807-362">Range</span><span class="sxs-lookup"><span data-stu-id="0a807-362">Range</span></span> | <span data-ttu-id="0a807-363">Predefinito</span><span class="sxs-lookup"><span data-stu-id="0a807-363">Default</span></span> |
|-----------|------------|-------|---------|
| <span data-ttu-id="0a807-364">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="0a807-364">**FLOAT**</span></span> | <span data-ttu-id="0a807-365">**\_R4 VT**</span><span class="sxs-lookup"><span data-stu-id="0a807-365">**VT\_R4**</span></span> | <span data-ttu-id="0a807-366">0 – 1,0</span><span class="sxs-lookup"><span data-stu-id="0a807-366">0–1.0</span></span> | <span data-ttu-id="0a807-367">0.9</span><span class="sxs-lookup"><span data-stu-id="0a807-367">0.9</span></span>     |



 

<span data-ttu-id="0a807-368">Il livello 1,0 garantisce una compressione senza perdita di codici.</span><span class="sxs-lookup"><span data-stu-id="0a807-368">Level 1.0 gives mathematically lossless compression.</span></span>

<span data-ttu-id="0a807-369">Il livello 0,0 è l'impostazione di qualità più bassa.</span><span class="sxs-lookup"><span data-stu-id="0a807-369">Level 0.0 is the lowest quality setting.</span></span>

### <a name="interleavedalpha"></a><span data-ttu-id="0a807-370">InterleavedAlpha</span><span class="sxs-lookup"><span data-stu-id="0a807-370">InterleavedAlpha</span></span>

<span data-ttu-id="0a807-371">Specifica se codificare alfa o Planar con interfoliazione.</span><span class="sxs-lookup"><span data-stu-id="0a807-371">Specifies whether to encode interleaved alpha or planar alpha.</span></span>



| <span data-ttu-id="0a807-372">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0a807-372">Data type</span></span>         | <span data-ttu-id="0a807-373">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0a807-373">VARTYPE</span></span>      | <span data-ttu-id="0a807-374">Predefinito</span><span class="sxs-lookup"><span data-stu-id="0a807-374">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="0a807-375">**\_bool Variant**</span><span class="sxs-lookup"><span data-stu-id="0a807-375">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="0a807-376">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="0a807-376">**VT\_BOOL**</span></span> | <span data-ttu-id="0a807-377">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="0a807-377">**VARIANT\_FALSE**</span></span> |



 

-   <span data-ttu-id="0a807-378">**Variante \_ TRUE**: Alfa Interleaved.</span><span class="sxs-lookup"><span data-stu-id="0a807-378">**VARIANT\_TRUE**: Interleaved alpha.</span></span> <span data-ttu-id="0a807-379">Le informazioni sul canale alfa sono codificate come canale Interleaved aggiuntivo, senza correlazione con i canali del contenuto di immagine.</span><span class="sxs-lookup"><span data-stu-id="0a807-379">Alpha channel information is encoded as an additional interleaved channel, with no correlation to the image content channels.</span></span> <span data-ttu-id="0a807-380">Questa modalità è utile per la decodifica di alfa simultaneamente con l'immagine durante il flusso dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="0a807-380">This mode is useful for decoding alpha simultaneously with the image when the image is streaming.</span></span>
-   <span data-ttu-id="0a807-381">VARIANT \_ false: alfa planare.</span><span class="sxs-lookup"><span data-stu-id="0a807-381">VARIANT\_FALSE: Planar alpha.</span></span> <span data-ttu-id="0a807-382">Un canale alfa planare viene codificato come immagine separata.</span><span class="sxs-lookup"><span data-stu-id="0a807-382">A planar alpha channel is encoded as a separate image.</span></span> <span data-ttu-id="0a807-383">I dati dell'immagine e il canale alfa vengono decodificati in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="0a807-383">The image data and the alpha channel are decoded independently.</span></span> <span data-ttu-id="0a807-384">Facoltativamente, è possibile impostare il livello di qualità del canale alfa impostando la proprietà [AlphaQuality](#alphaquality) .</span><span class="sxs-lookup"><span data-stu-id="0a807-384">Optionally, you can set the quality level of the alpha channel by setting the [AlphaQuality](#alphaquality) property.</span></span>

<span data-ttu-id="0a807-385">L'Alpha Interleaved è supportato solo per determinati formati pixel RGB.</span><span class="sxs-lookup"><span data-stu-id="0a807-385">Interleaved alpha is supported only for certain RGB pixel formats.</span></span> <span data-ttu-id="0a807-386">Planar Alpha è supportato per qualsiasi formato di immagine che definisce un canale alfa.</span><span class="sxs-lookup"><span data-stu-id="0a807-386">Planar alpha is supported for any image format that defines an alpha channel.</span></span>

### <a name="lossless"></a><span data-ttu-id="0a807-387">Lossless</span><span class="sxs-lookup"><span data-stu-id="0a807-387">Lossless</span></span>

<span data-ttu-id="0a807-388">Abilita la compressione delle perdite.</span><span class="sxs-lookup"><span data-stu-id="0a807-388">Enables losses compression.</span></span>



| <span data-ttu-id="0a807-389">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0a807-389">Data type</span></span>         | <span data-ttu-id="0a807-390">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0a807-390">VARTYPE</span></span>      | <span data-ttu-id="0a807-391">Predefinito</span><span class="sxs-lookup"><span data-stu-id="0a807-391">Default</span></span>        |
|-------------------|--------------|----------------|
| <span data-ttu-id="0a807-392">**\_bool Variant**</span><span class="sxs-lookup"><span data-stu-id="0a807-392">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="0a807-393">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="0a807-393">**VT\_BOOL**</span></span> | <span data-ttu-id="0a807-394">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="0a807-394">VARIANT\_FALSE</span></span> |



 

<span data-ttu-id="0a807-395">Se il valore è **Variant \_ true**, il codificatore usa la compressione senza perdita di perdite.</span><span class="sxs-lookup"><span data-stu-id="0a807-395">If the value is **VARIANT\_TRUE**, the encoder uses lossless compression.</span></span> <span data-ttu-id="0a807-396">Se impostata su **Variant \_ true**, questa proprietà esegue l'override della proprietà [ImageQuality](#imagequality) .</span><span class="sxs-lookup"><span data-stu-id="0a807-396">When set to **VARIANT\_TRUE**, this property overrides the [ImageQuality](#imagequality) property.</span></span>

### <a name="overlap"></a><span data-ttu-id="0a807-397">Overlap</span><span class="sxs-lookup"><span data-stu-id="0a807-397">Overlap</span></span>

<span data-ttu-id="0a807-398">Imposta il livello di filtro di sovrapposizione.</span><span class="sxs-lookup"><span data-stu-id="0a807-398">Sets the level of overlap filtering.</span></span> <span data-ttu-id="0a807-399">Con il filtro di sovrapposizione, i coefficienti di trasformazione vengono applicati tra i limiti Block e macroblocco.</span><span class="sxs-lookup"><span data-stu-id="0a807-399">With overlap filtering, transform coefficients are applied across block and macroblock boundaries.</span></span> <span data-ttu-id="0a807-400">Questo può ridurre gli artefatti di blocco.</span><span class="sxs-lookup"><span data-stu-id="0a807-400">This can reduce blocking artifacts.</span></span>



| <span data-ttu-id="0a807-401">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0a807-401">Data type</span></span> | <span data-ttu-id="0a807-402">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0a807-402">VARTYPE</span></span>     | <span data-ttu-id="0a807-403">Range</span><span class="sxs-lookup"><span data-stu-id="0a807-403">Range</span></span> | <span data-ttu-id="0a807-404">Predefinito</span><span class="sxs-lookup"><span data-stu-id="0a807-404">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="0a807-405">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="0a807-405">**UCHAR**</span></span> | <span data-ttu-id="0a807-406">**\_Ui1 VT**</span><span class="sxs-lookup"><span data-stu-id="0a807-406">**VT\_UI1**</span></span> | <span data-ttu-id="0a807-407">0 – 4</span><span class="sxs-lookup"><span data-stu-id="0a807-407">0–4</span></span>   | <span data-ttu-id="0a807-408">1</span><span class="sxs-lookup"><span data-stu-id="0a807-408">1</span></span>       |



 



| <span data-ttu-id="0a807-409">Valore</span><span class="sxs-lookup"><span data-stu-id="0a807-409">Value</span></span> | <span data-ttu-id="0a807-410">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a807-410">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="0a807-411">0</span><span class="sxs-lookup"><span data-stu-id="0a807-411">0</span></span>     | <span data-ttu-id="0a807-412">Nessuna sovrapposizione.</span><span class="sxs-lookup"><span data-stu-id="0a807-412">No overlap.</span></span>                                   |
| <span data-ttu-id="0a807-413">1</span><span class="sxs-lookup"><span data-stu-id="0a807-413">1</span></span>     | <span data-ttu-id="0a807-414">Un livello di sovrapposizione, affiancamento flessibile.</span><span class="sxs-lookup"><span data-stu-id="0a807-414">One level of overlap, soft tiling.</span></span> <span data-ttu-id="0a807-415">(impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="0a807-415">(Default.)</span></span> |
| <span data-ttu-id="0a807-416">2</span><span class="sxs-lookup"><span data-stu-id="0a807-416">2</span></span>     | <span data-ttu-id="0a807-417">Due livelli di sovrapposizione, affiancamento flessibile.</span><span class="sxs-lookup"><span data-stu-id="0a807-417">Two levels of overlap, soft tiling.</span></span>           |
| <span data-ttu-id="0a807-418">3</span><span class="sxs-lookup"><span data-stu-id="0a807-418">3</span></span>     | <span data-ttu-id="0a807-419">Un livello di sovrapposizione, rivestimento rigido</span><span class="sxs-lookup"><span data-stu-id="0a807-419">One level of overlap, hard tiling</span></span>             |
| <span data-ttu-id="0a807-420">4</span><span class="sxs-lookup"><span data-stu-id="0a807-420">4</span></span>     | <span data-ttu-id="0a807-421">Due livelli di sovrapposizione, disco rigido.</span><span class="sxs-lookup"><span data-stu-id="0a807-421">Two levels of overlap, hard tiling.</span></span>           |



 

<span data-ttu-id="0a807-422">Definizioni:</span><span class="sxs-lookup"><span data-stu-id="0a807-422">Definitions:</span></span>

-   <span data-ttu-id="0a807-423">Un livello di sovrapposizione: i valori codificati dei blocchi 4x4 vengono modificati in base ai blocchi adiacenti.</span><span class="sxs-lookup"><span data-stu-id="0a807-423">One level of overlap: The encoded values of 4x4 blocks are modified based on neighboring blocks.</span></span>
-   <span data-ttu-id="0a807-424">Due livelli di sovrapposizione: viene applicato il primo livello di sovrapposizione.</span><span class="sxs-lookup"><span data-stu-id="0a807-424">Two levels of overlap: The first level of overlap is applied.</span></span> <span data-ttu-id="0a807-425">Inoltre, i valori codificati di 16x16 macroblocchi vengono modificati in base ai macroblocchi adiacenti.</span><span class="sxs-lookup"><span data-stu-id="0a807-425">In addition, the encoded values of 16x16 macroblocks are modified based on the neighboring macroblocks.</span></span>
-   <span data-ttu-id="0a807-426">Affiancamento flessibile: i filtri sovrapposti vengono applicati tra i limiti del riquadro.</span><span class="sxs-lookup"><span data-stu-id="0a807-426">Soft tiling: Overlap filtering is applied across tile boundaries.</span></span>
-   <span data-ttu-id="0a807-427">Affiancamento rigido: i filtri sovrapposti non vengono applicati tra i limiti dei riquadri.</span><span class="sxs-lookup"><span data-stu-id="0a807-427">Hard tiling: Overlap filtering is not applied across tile boundaries.</span></span> <span data-ttu-id="0a807-428">I riquadri rigidi possono introdurre alcuni artefatti visivi lungo i confini dei riquadri.</span><span class="sxs-lookup"><span data-stu-id="0a807-428">Hard tiles can introduce some visual artifacts along tile boundaries.</span></span>

<span data-ttu-id="0a807-429">Se si imposta questa proprietà, impostare anche [UseCodecOptions](#usecodecoptions) su **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="0a807-429">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="progressivemode"></a><span data-ttu-id="0a807-430">Codifica</span><span class="sxs-lookup"><span data-stu-id="0a807-430">ProgressiveMode</span></span>

<span data-ttu-id="0a807-431">Abilita o Disabilita la codifica progressiva.</span><span class="sxs-lookup"><span data-stu-id="0a807-431">Enables or disables progressive encoding.</span></span>



| <span data-ttu-id="0a807-432">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0a807-432">Data type</span></span>         | <span data-ttu-id="0a807-433">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0a807-433">VARTYPE</span></span>      | <span data-ttu-id="0a807-434">Predefinito</span><span class="sxs-lookup"><span data-stu-id="0a807-434">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="0a807-435">**\_bool Variant**</span><span class="sxs-lookup"><span data-stu-id="0a807-435">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="0a807-436">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="0a807-436">**VT\_BOOL**</span></span> | <span data-ttu-id="0a807-437">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="0a807-437">**VARIANT\_FALSE**</span></span> |



 



| <span data-ttu-id="0a807-438">Valore</span><span class="sxs-lookup"><span data-stu-id="0a807-438">Value</span></span>              | <span data-ttu-id="0a807-439">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a807-439">Description</span></span>                |
|--------------------|----------------------------|
| <span data-ttu-id="0a807-440">**VARIANT \_ true**</span><span class="sxs-lookup"><span data-stu-id="0a807-440">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="0a807-441">Modalità sequenziale (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="0a807-441">Sequential mode (default).</span></span> |
| <span data-ttu-id="0a807-442">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="0a807-442">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="0a807-443">Modalità progressiva.</span><span class="sxs-lookup"><span data-stu-id="0a807-443">Progressive mode.</span></span>          |



 

### <a name="quality"></a><span data-ttu-id="0a807-444">Qualità</span><span class="sxs-lookup"><span data-stu-id="0a807-444">Quality</span></span>

<span data-ttu-id="0a807-445">Imposta la qualità di compressione.</span><span class="sxs-lookup"><span data-stu-id="0a807-445">Sets the compression quality.</span></span>



| <span data-ttu-id="0a807-446">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0a807-446">Data type</span></span> | <span data-ttu-id="0a807-447">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0a807-447">VARTYPE</span></span>     | <span data-ttu-id="0a807-448">Range</span><span class="sxs-lookup"><span data-stu-id="0a807-448">Range</span></span> | <span data-ttu-id="0a807-449">Predefinito</span><span class="sxs-lookup"><span data-stu-id="0a807-449">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="0a807-450">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="0a807-450">**UCHAR**</span></span> | <span data-ttu-id="0a807-451">**\_Ui1 VT**</span><span class="sxs-lookup"><span data-stu-id="0a807-451">**VT\_UI1**</span></span> | <span data-ttu-id="0a807-452">da 1 a 255</span><span class="sxs-lookup"><span data-stu-id="0a807-452">1–255</span></span> | <span data-ttu-id="0a807-453">1</span><span class="sxs-lookup"><span data-stu-id="0a807-453">1</span></span>       |



 

<span data-ttu-id="0a807-454">Il valore 1 indica la modalità lossless.</span><span class="sxs-lookup"><span data-stu-id="0a807-454">The value 1 indicates lossless mode.</span></span> <span data-ttu-id="0a807-455">L'aumento dei valori comporta percentuali di compressione più elevate e una minore qualità dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="0a807-455">Increasing values result in higher compression ratios and lower image quality.</span></span>

<span data-ttu-id="0a807-456">Se si imposta questa proprietà, impostare anche [UseCodecOptions](#usecodecoptions) su **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="0a807-456">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="streamonly"></a><span data-ttu-id="0a807-457">StreamOnly</span><span class="sxs-lookup"><span data-stu-id="0a807-457">StreamOnly</span></span>

<span data-ttu-id="0a807-458">Abilita o Disabilita la modalità di sola trasmissione.</span><span class="sxs-lookup"><span data-stu-id="0a807-458">Enables or disables stream-only mode.</span></span>



| <span data-ttu-id="0a807-459">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0a807-459">Data type</span></span>         | <span data-ttu-id="0a807-460">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0a807-460">VARTYPE</span></span>      | <span data-ttu-id="0a807-461">Predefinito</span><span class="sxs-lookup"><span data-stu-id="0a807-461">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="0a807-462">**\_bool Variant**</span><span class="sxs-lookup"><span data-stu-id="0a807-462">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="0a807-463">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="0a807-463">**VT\_BOOL**</span></span> | <span data-ttu-id="0a807-464">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="0a807-464">**VARIANT\_FALSE**</span></span> |



 



| <span data-ttu-id="0a807-465">Valore</span><span class="sxs-lookup"><span data-stu-id="0a807-465">Value</span></span>              | <span data-ttu-id="0a807-466">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a807-466">Description</span></span>                                                            |
|--------------------|------------------------------------------------------------------------|
| <span data-ttu-id="0a807-467">**VARIANT \_ true**</span><span class="sxs-lookup"><span data-stu-id="0a807-467">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="0a807-468">Il codificatore restituisce il flusso dell'immagine non elaborata senza metadati.</span><span class="sxs-lookup"><span data-stu-id="0a807-468">The encoder outputs the raw image stream without metadata.</span></span>             |
| <span data-ttu-id="0a807-469">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="0a807-469">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="0a807-470">Il codificatore restituisce il formato del contenitore (flusso di immagini e metadati).</span><span class="sxs-lookup"><span data-stu-id="0a807-470">The encoder outputs the container format (image stream plus metadata).</span></span> |



 

### <a name="subsampling"></a><span data-ttu-id="0a807-471">Sottocampionamento</span><span class="sxs-lookup"><span data-stu-id="0a807-471">Subsampling</span></span>

<span data-ttu-id="0a807-472">Imposta il sottocampionamento Chroma.</span><span class="sxs-lookup"><span data-stu-id="0a807-472">Sets the chroma subsampling.</span></span> <span data-ttu-id="0a807-473">Questa proprietà si applica solo alle immagini RGB.</span><span class="sxs-lookup"><span data-stu-id="0a807-473">This property applies only to RGB images.</span></span>



| <span data-ttu-id="0a807-474">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0a807-474">Data type</span></span> | <span data-ttu-id="0a807-475">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0a807-475">VARTYPE</span></span>     | <span data-ttu-id="0a807-476">Range</span><span class="sxs-lookup"><span data-stu-id="0a807-476">Range</span></span> | <span data-ttu-id="0a807-477">Predefinito</span><span class="sxs-lookup"><span data-stu-id="0a807-477">Default</span></span>                                                  |
|-----------|-------------|-------|----------------------------------------------------------|
| <span data-ttu-id="0a807-478">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="0a807-478">**UCHAR**</span></span> | <span data-ttu-id="0a807-479">**\_Ui1 VT**</span><span class="sxs-lookup"><span data-stu-id="0a807-479">**VT\_UI1**</span></span> | <span data-ttu-id="0a807-480">0 – 3</span><span class="sxs-lookup"><span data-stu-id="0a807-480">0–3</span></span>   | <span data-ttu-id="0a807-481">3 Se [ImageQuality](#imagequality) > 0,8; in caso contrario, 1</span><span class="sxs-lookup"><span data-stu-id="0a807-481">3 if [ImageQuality](#imagequality) > 0.8; otherwise 1</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0a807-482">Valore</span><span class="sxs-lookup"><span data-stu-id="0a807-482">Value</span></span></th>
<th><span data-ttu-id="0a807-483">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a807-483">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0a807-484">3</span><span class="sxs-lookup"><span data-stu-id="0a807-484">3</span></span></td>
<td><span data-ttu-id="0a807-485">codifica 4:4:4.</span><span class="sxs-lookup"><span data-stu-id="0a807-485">4:4:4 encoding.</span></span> <span data-ttu-id="0a807-486">Conserva la risoluzione Chroma completa.</span><span class="sxs-lookup"><span data-stu-id="0a807-486">Preserves full chroma resolution.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a807-487">2</span><span class="sxs-lookup"><span data-stu-id="0a807-487">2</span></span></td>
<td><span data-ttu-id="0a807-488">codifica 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="0a807-488">4:2:2 encoding.</span></span> <span data-ttu-id="0a807-489">La risoluzione Chroma è 1/2 della risoluzione della luminanza.</span><span class="sxs-lookup"><span data-stu-id="0a807-489">Chroma resolution is ½ of luminance resolution.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a807-490">1</span><span class="sxs-lookup"><span data-stu-id="0a807-490">1</span></span></td>
<td><span data-ttu-id="0a807-491">codifica 4:2:0.</span><span class="sxs-lookup"><span data-stu-id="0a807-491">4:2:0 encoding.</span></span> <span data-ttu-id="0a807-492">La risoluzione Chroma è 1/4 della risoluzione della luminanza.</span><span class="sxs-lookup"><span data-stu-id="0a807-492">Chroma resolution is ¼ of luminance resolution.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a807-493">0</span><span class="sxs-lookup"><span data-stu-id="0a807-493">0</span></span></td>
<td><span data-ttu-id="0a807-494">Codifica 4:0:0.</span><span class="sxs-lookup"><span data-stu-id="0a807-494">4:0:0 encoding.</span></span> <span data-ttu-id="0a807-495">Elimina tutti i valori Chroma e conserva solo la luminanza.</span><span class="sxs-lookup"><span data-stu-id="0a807-495">Discards all chroma values and preserves luminance only.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="0a807-496">Questa modalità non è consigliata, perché il codec usa una definizione di luminanza leggermente modificata per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="0a807-496">This mode is not recommended, because the codec uses a slightly modified definition of luminance to improve performance.</span></span> <span data-ttu-id="0a807-497">È invece preferibile convertire l'immagine in monocromatico prima della codifica.</span><span class="sxs-lookup"><span data-stu-id="0a807-497">Instead, it is better to convert the image to monochrome before encoding.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0a807-498">4:2:2 e 4:2:0 conservano i dettagli della luminanza a scapito dei dettagli del colore.</span><span class="sxs-lookup"><span data-stu-id="0a807-498">4:2:2 and 4:2:0 preserve luminance detail at the expense of color detail.</span></span>

<span data-ttu-id="0a807-499">Se si imposta questa proprietà, impostare anche [UseCodecOptions](#usecodecoptions) su **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="0a807-499">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="usecodecoptions"></a><span data-ttu-id="0a807-500">UseCodecOptions</span><span class="sxs-lookup"><span data-stu-id="0a807-500">UseCodecOptions</span></span>

<span data-ttu-id="0a807-501">Specifica se utilizzare le proprietà [qualità](#image-quality-settings), [sovrapposizione](#overlap)e [sottocampionamento](#subsampling) invece della proprietà [ImageQuality](#imagequality) generica.</span><span class="sxs-lookup"><span data-stu-id="0a807-501">Specifies whether to use the [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties instead of the generic [ImageQuality](#imagequality) property.</span></span>



| <span data-ttu-id="0a807-502">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0a807-502">Data type</span></span>         | <span data-ttu-id="0a807-503">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0a807-503">VARTYPE</span></span>      | <span data-ttu-id="0a807-504">Predefinito</span><span class="sxs-lookup"><span data-stu-id="0a807-504">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="0a807-505">**\_bool Variant**</span><span class="sxs-lookup"><span data-stu-id="0a807-505">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="0a807-506">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="0a807-506">**VT\_BOOL**</span></span> | <span data-ttu-id="0a807-507">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="0a807-507">**VARIANT\_FALSE**</span></span> |



 

### <a name="verticaltileslices"></a><span data-ttu-id="0a807-508">VerticalTileSlices</span><span class="sxs-lookup"><span data-stu-id="0a807-508">VerticalTileSlices</span></span>

<span data-ttu-id="0a807-509">Imposta il numero di riquadri orizzontali.</span><span class="sxs-lookup"><span data-stu-id="0a807-509">Sets the number of horizontal tiles.</span></span>



| <span data-ttu-id="0a807-510">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0a807-510">Data type</span></span>  | <span data-ttu-id="0a807-511">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0a807-511">VARTYPE</span></span>     | <span data-ttu-id="0a807-512">Range</span><span class="sxs-lookup"><span data-stu-id="0a807-512">Range</span></span>  | <span data-ttu-id="0a807-513">Predefinito</span><span class="sxs-lookup"><span data-stu-id="0a807-513">Default</span></span>                       |
|------------|-------------|--------|-------------------------------|
| <span data-ttu-id="0a807-514">**USHORT**</span><span class="sxs-lookup"><span data-stu-id="0a807-514">**USHORT**</span></span> | <span data-ttu-id="0a807-515">**\_UI2 VT**</span><span class="sxs-lookup"><span data-stu-id="0a807-515">**VT\_UI2**</span></span> | <span data-ttu-id="0a807-516">0 – 4095</span><span class="sxs-lookup"><span data-stu-id="0a807-516">0–4095</span></span> | <span data-ttu-id="0a807-517">(altezza immagine-1)  >> 8</span><span class="sxs-lookup"><span data-stu-id="0a807-517">(image height – 1) >> 8</span></span> |



 

<span data-ttu-id="0a807-518">Il valore è il numero di suddivisioni verticali; ovvero il numero di riquadri verticali-1.</span><span class="sxs-lookup"><span data-stu-id="0a807-518">The value is the number of vertical subdivisions; that is, the number of vertical tiles – 1.</span></span>

## <a name="supported-color-formats"></a><span data-ttu-id="0a807-519">Formati di colore supportati</span><span class="sxs-lookup"><span data-stu-id="0a807-519">Supported Color Formats</span></span>

<span data-ttu-id="0a807-520">Per ulteriori informazioni su questi formati, vedere [formati di pixel nativi](-wic-codec-native-pixel-formats.md).</span><span class="sxs-lookup"><span data-stu-id="0a807-520">For more information about these formats, see [Native Pixel Formats](-wic-codec-native-pixel-formats.md).</span></span>

-   <span data-ttu-id="0a807-521">**Formati RGB Integer**</span><span class="sxs-lookup"><span data-stu-id="0a807-521">**Integer RGB formats**</span></span>
    -   <span data-ttu-id="0a807-522">GUID \_ WICPixelFormat24bppRGB</span><span class="sxs-lookup"><span data-stu-id="0a807-522">GUID\_WICPixelFormat24bppRGB</span></span>
    -   <span data-ttu-id="0a807-523">GUID \_ WICPixelFormat24bppBGR</span><span class="sxs-lookup"><span data-stu-id="0a807-523">GUID\_WICPixelFormat24bppBGR</span></span>
    -   <span data-ttu-id="0a807-524">GUID \_ WICPixelFormat32bppBGR</span><span class="sxs-lookup"><span data-stu-id="0a807-524">GUID\_WICPixelFormat32bppBGR</span></span>
    -   <span data-ttu-id="0a807-525">GUID \_ WICPixelFormat48bppRGB</span><span class="sxs-lookup"><span data-stu-id="0a807-525">GUID\_WICPixelFormat48bppRGB</span></span>
    -   <span data-ttu-id="0a807-526">GUID \_ WICPixelFormat32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="0a807-526">GUID\_WICPixelFormat32bppBGRA</span></span>
    -   <span data-ttu-id="0a807-527">GUID \_ WICPixelFormat64bppRGBA</span><span class="sxs-lookup"><span data-stu-id="0a807-527">GUID\_WICPixelFormat64bppRGBA</span></span>
    -   <span data-ttu-id="0a807-528">GUID \_ WICPixelFormat32bppPBGRA</span><span class="sxs-lookup"><span data-stu-id="0a807-528">GUID\_WICPixelFormat32bppPBGRA</span></span>
    -   <span data-ttu-id="0a807-529">GUID \_ WICPixelFormat64bppPRGBA</span><span class="sxs-lookup"><span data-stu-id="0a807-529">GUID\_WICPixelFormat64bppPRGBA</span></span>
-   <span data-ttu-id="0a807-530">**Formati RGB a virgola fissa**</span><span class="sxs-lookup"><span data-stu-id="0a807-530">**Fixed-point RGB formats**</span></span>
    -   <span data-ttu-id="0a807-531">GUID \_ WICPixelFormat48bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="0a807-531">GUID\_WICPixelFormat48bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="0a807-532">GUID \_ WICPixelFormat64bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="0a807-532">GUID\_WICPixelFormat64bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="0a807-533">GUID \_ WICPixelFormat96bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="0a807-533">GUID\_WICPixelFormat96bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="0a807-534">GUID \_ WICPixelFormat128bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="0a807-534">GUID\_WICPixelFormat128bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="0a807-535">GUID \_ WICPixelFormat128bppRGBAFixedPoint</span><span class="sxs-lookup"><span data-stu-id="0a807-535">GUID\_WICPixelFormat128bppRGBAFixedPoint</span></span>
-   <span data-ttu-id="0a807-536">**Formati RGB a virgola mobile**</span><span class="sxs-lookup"><span data-stu-id="0a807-536">**Floating-point RGB formats**</span></span>
    -   <span data-ttu-id="0a807-537">GUID \_ WICPixelFormat48bppRGBHalf</span><span class="sxs-lookup"><span data-stu-id="0a807-537">GUID\_WICPixelFormat48bppRGBHalf</span></span>
    -   <span data-ttu-id="0a807-538">GUID \_ WICPixelFormat64bppRGBHalf</span><span class="sxs-lookup"><span data-stu-id="0a807-538">GUID\_WICPixelFormat64bppRGBHalf</span></span>
    -   <span data-ttu-id="0a807-539">GUID \_ WICPixelFormat128bppRGBFloat</span><span class="sxs-lookup"><span data-stu-id="0a807-539">GUID\_WICPixelFormat128bppRGBFloat</span></span>
    -   <span data-ttu-id="0a807-540">GUID \_ WICPixelFormat64bppRGBAFixedPoint</span><span class="sxs-lookup"><span data-stu-id="0a807-540">GUID\_WICPixelFormat64bppRGBAFixedPoint</span></span>
    -   <span data-ttu-id="0a807-541">GUID \_ WICPixelFormat64bppRGBAHalf</span><span class="sxs-lookup"><span data-stu-id="0a807-541">GUID\_WICPixelFormat64bppRGBAHalf</span></span>
    -   <span data-ttu-id="0a807-542">GUID \_ WICPixelFormat128bppRGBAFloat</span><span class="sxs-lookup"><span data-stu-id="0a807-542">GUID\_WICPixelFormat128bppRGBAFloat</span></span>
    -   <span data-ttu-id="0a807-543">GUID \_ WICPixelFormat128bppPRGBAFloat</span><span class="sxs-lookup"><span data-stu-id="0a807-543">GUID\_WICPixelFormat128bppPRGBAFloat</span></span>
-   <span data-ttu-id="0a807-544">**Formati di scala di grigi**</span><span class="sxs-lookup"><span data-stu-id="0a807-544">**Grayscale formats**</span></span>
    -   <span data-ttu-id="0a807-545">GUID \_ WICPixelFormat8bppGray</span><span class="sxs-lookup"><span data-stu-id="0a807-545">GUID\_WICPixelFormat8bppGray</span></span>
    -   <span data-ttu-id="0a807-546">GUID \_ WICPixelFormat16bppGray</span><span class="sxs-lookup"><span data-stu-id="0a807-546">GUID\_WICPixelFormat16bppGray</span></span>
    -   <span data-ttu-id="0a807-547">GUID \_ WICPixelFormat16bppGrayFixedPoint</span><span class="sxs-lookup"><span data-stu-id="0a807-547">GUID\_WICPixelFormat16bppGrayFixedPoint</span></span>
    -   <span data-ttu-id="0a807-548">GUID \_ WICPixelFormat16bppGrayHalf</span><span class="sxs-lookup"><span data-stu-id="0a807-548">GUID\_WICPixelFormat16bppGrayHalf</span></span>
    -   <span data-ttu-id="0a807-549">GUID \_ WICPixelFormat32bppGrayFixedPoint</span><span class="sxs-lookup"><span data-stu-id="0a807-549">GUID\_WICPixelFormat32bppGrayFixedPoint</span></span>
    -   <span data-ttu-id="0a807-550">GUID \_ WICPixelFormat32bppGrayFloat</span><span class="sxs-lookup"><span data-stu-id="0a807-550">GUID\_WICPixelFormat32bppGrayFloat</span></span>
-   <span data-ttu-id="0a807-551">**Formati compressi**</span><span class="sxs-lookup"><span data-stu-id="0a807-551">**Packed formats**</span></span>
    -   <span data-ttu-id="0a807-552">GUID \_ WICPixelFormat16bppBGR555</span><span class="sxs-lookup"><span data-stu-id="0a807-552">GUID\_WICPixelFormat16bppBGR555</span></span>
    -   <span data-ttu-id="0a807-553">GUID \_ WICPixelFormat16bppBGR565</span><span class="sxs-lookup"><span data-stu-id="0a807-553">GUID\_WICPixelFormat16bppBGR565</span></span>
    -   <span data-ttu-id="0a807-554">GUID \_ WICPixelFormat32bppBGR101010</span><span class="sxs-lookup"><span data-stu-id="0a807-554">GUID\_WICPixelFormat32bppBGR101010</span></span>
    -   <span data-ttu-id="0a807-555">GUID \_ WICPixelFormat32bppRGBE</span><span class="sxs-lookup"><span data-stu-id="0a807-555">GUID\_WICPixelFormat32bppRGBE</span></span>
-   <span data-ttu-id="0a807-556">**Formati CMYK**</span><span class="sxs-lookup"><span data-stu-id="0a807-556">**CMYK formats**</span></span>
    -   <span data-ttu-id="0a807-557">GUID \_ WICPixelFormat40bppCMYKAlpha</span><span class="sxs-lookup"><span data-stu-id="0a807-557">GUID\_WICPixelFormat40bppCMYKAlpha</span></span>
    -   <span data-ttu-id="0a807-558">GUID \_ WICPixelFormat64bppCMYK</span><span class="sxs-lookup"><span data-stu-id="0a807-558">GUID\_WICPixelFormat64bppCMYK</span></span>
    -   <span data-ttu-id="0a807-559">GUID \_ WICPixelFormat80bppCMYKAlpha</span><span class="sxs-lookup"><span data-stu-id="0a807-559">GUID\_WICPixelFormat80bppCMYKAlpha</span></span>
-   <span data-ttu-id="0a807-560">**Formati N-Channel**</span><span class="sxs-lookup"><span data-stu-id="0a807-560">**N-channel formats**</span></span>
    -   <span data-ttu-id="0a807-561">GUID \_ WICPixelFormat32bpp4Channels</span><span class="sxs-lookup"><span data-stu-id="0a807-561">GUID\_WICPixelFormat32bpp4Channels</span></span>
    -   <span data-ttu-id="0a807-562">GUID \_ WICPixelFormat40bpp5Channels</span><span class="sxs-lookup"><span data-stu-id="0a807-562">GUID\_WICPixelFormat40bpp5Channels</span></span>
    -   <span data-ttu-id="0a807-563">GUID \_ WICPixelFormat48bpp6Channels</span><span class="sxs-lookup"><span data-stu-id="0a807-563">GUID\_WICPixelFormat48bpp6Channels</span></span>
    -   <span data-ttu-id="0a807-564">GUID \_ WICPixelFormat56bpp7Channels</span><span class="sxs-lookup"><span data-stu-id="0a807-564">GUID\_WICPixelFormat56bpp7Channels</span></span>
    -   <span data-ttu-id="0a807-565">GUID \_ WICPixelFormat64bpp8Channels</span><span class="sxs-lookup"><span data-stu-id="0a807-565">GUID\_WICPixelFormat64bpp8Channels</span></span>
    -   <span data-ttu-id="0a807-566">GUID \_ WICPixelFormat32bpp3ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="0a807-566">GUID\_WICPixelFormat32bpp3ChannelsAlpha</span></span>
    -   <span data-ttu-id="0a807-567">GUID \_ WICPixelFormat40bpp4ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="0a807-567">GUID\_WICPixelFormat40bpp4ChannelsAlpha</span></span>
    -   <span data-ttu-id="0a807-568">GUID \_ WICPixelFormat48bpp5ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="0a807-568">GUID\_WICPixelFormat48bpp5ChannelsAlpha</span></span>
    -   <span data-ttu-id="0a807-569">GUID \_ WICPixelFormat56bpp6ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="0a807-569">GUID\_WICPixelFormat56bpp6ChannelsAlpha</span></span>
    -   <span data-ttu-id="0a807-570">GUID \_ WICPixelFormat64bpp7ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="0a807-570">GUID\_WICPixelFormat64bpp7ChannelsAlpha</span></span>
    -   <span data-ttu-id="0a807-571">GUID \_ WICPixelFormat72bpp8ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="0a807-571">GUID\_WICPixelFormat72bpp8ChannelsAlpha</span></span>
    -   <span data-ttu-id="0a807-572">GUID \_ WICPixelFormat48bpp3Channels</span><span class="sxs-lookup"><span data-stu-id="0a807-572">GUID\_WICPixelFormat48bpp3Channels</span></span>
    -   <span data-ttu-id="0a807-573">GUID \_ WICPixelFormat64bpp4Channels</span><span class="sxs-lookup"><span data-stu-id="0a807-573">GUID\_WICPixelFormat64bpp4Channels</span></span>
    -   <span data-ttu-id="0a807-574">GUID \_ WICPixelFormat80bpp5Channels</span><span class="sxs-lookup"><span data-stu-id="0a807-574">GUID\_WICPixelFormat80bpp5Channels</span></span>
    -   <span data-ttu-id="0a807-575">GUID \_ WICPixelFormat96bpp6Channels</span><span class="sxs-lookup"><span data-stu-id="0a807-575">GUID\_WICPixelFormat96bpp6Channels</span></span>
    -   <span data-ttu-id="0a807-576">GUID \_ WICPixelFormat128bpp8Channels</span><span class="sxs-lookup"><span data-stu-id="0a807-576">GUID\_WICPixelFormat128bpp8Channels</span></span>
    -   <span data-ttu-id="0a807-577">GUID \_ WICPixelFormat64bpp3ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="0a807-577">GUID\_WICPixelFormat64bpp3ChannelsAlpha</span></span>
    -   <span data-ttu-id="0a807-578">GUID \_ WICPixelFormat80bpp4ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="0a807-578">GUID\_WICPixelFormat80bpp4ChannelsAlpha</span></span>
    -   <span data-ttu-id="0a807-579">GUID \_ WICPixelFormat96bpp5ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="0a807-579">GUID\_WICPixelFormat96bpp5ChannelsAlpha</span></span>
    -   <span data-ttu-id="0a807-580">GUID \_ WICPixelFormat112bpp6ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="0a807-580">GUID\_WICPixelFormat112bpp6ChannelsAlpha</span></span>
    -   <span data-ttu-id="0a807-581">GUID \_ WICPixelFormat128bpp7ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="0a807-581">GUID\_WICPixelFormat128bpp7ChannelsAlpha</span></span>
    -   <span data-ttu-id="0a807-582">GUID \_ WICPixelFormat144bpp8ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="0a807-582">GUID\_WICPixelFormat144bpp8ChannelsAlpha</span></span>

 

 
