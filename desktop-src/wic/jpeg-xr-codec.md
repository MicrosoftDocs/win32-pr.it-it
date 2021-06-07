---
description: Il codec XR JPEG nativo è disponibile tramite Windows Imaging Component (WIC). Il formato JPEG XR supportato dal codec è progettato per la fotografia digitale consumer e professionale.
ms.assetid: CB8D1A5F-B544-462E-8927-F45512CED873
title: Panoramica del codec JPEG XR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d39608535f9be09821d8db3615641a84fd95a6
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444463"
---
# <a name="jpeg-xr-codec-overview"></a><span data-ttu-id="c621e-104">Panoramica del codec JPEG XR</span><span class="sxs-lookup"><span data-stu-id="c621e-104">JPEG XR Codec Overview</span></span>

<span data-ttu-id="c621e-105">Il codec XR JPEG nativo è disponibile tramite Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="c621e-105">The native JPEG XR codec is available through the Windows Imaging Component (WIC).</span></span> <span data-ttu-id="c621e-106">Il formato JPEG XR supportato dal codec è progettato per la fotografia digitale consumer e professionale.</span><span class="sxs-lookup"><span data-stu-id="c621e-106">The JPEG XR format, which the codec supports, is designed for consumer and professional digital photography.</span></span>

<span data-ttu-id="c621e-107">Il formato JPEG XR può ottenere fino al doppio dell'efficienza di compressione del formato JPEG originale, con artefatti di compressione meno evidenti.</span><span class="sxs-lookup"><span data-stu-id="c621e-107">The JPEG XR format can achieve up to twice the compression efficiency of the original JPEG format, with less noticeable compression artifacts.</span></span> <span data-ttu-id="c621e-108">Le funzionalità di JPEG XR includono:</span><span class="sxs-lookup"><span data-stu-id="c621e-108">Features of JPEG XR include:</span></span>

-   <span data-ttu-id="c621e-109">Supporto per immagini monocroma, RGB, CMYK e n canali</span><span class="sxs-lookup"><span data-stu-id="c621e-109">Support for monochrome, RGB, CMYK, and n-channel images</span></span>
-   <span data-ttu-id="c621e-110">Formati integer a 8, 16 e 32 bit</span><span class="sxs-lookup"><span data-stu-id="c621e-110">8-, 16-, and 32-bit integer formats</span></span>
-   <span data-ttu-id="c621e-111">Intervallo dinamico elevato, formati wide gamut, con valori di colore a virgola fissa o a virgola mobile</span><span class="sxs-lookup"><span data-stu-id="c621e-111">High dynamic range, wide-gamut formats, using fixed point or floating point color values</span></span>
-   <span data-ttu-id="c621e-112">Decodifica progressiva</span><span class="sxs-lookup"><span data-stu-id="c621e-112">Progressive decoding</span></span>
-   <span data-ttu-id="c621e-113">Codifica senza perdita di dati con lo stesso algoritmo di compressione</span><span class="sxs-lookup"><span data-stu-id="c621e-113">Lossy or lossless encoding using the same compression algorithm</span></span>
-   <span data-ttu-id="c621e-114">Supporto per la decodifica di aree di interesse in immagini di grandi dimensioni</span><span class="sxs-lookup"><span data-stu-id="c621e-114">Support for decoding of regions of interest in large images</span></span>

<span data-ttu-id="c621e-115">Il formato JPEG XR è definito nei documenti standard seguenti:</span><span class="sxs-lookup"><span data-stu-id="c621e-115">The JPEG XR format is defined in the following standards documents:</span></span>

-   <span data-ttu-id="c621e-116">ITU-T T.832: *Information technology – Jpeg XR image coding system – Image coding specification*</span><span class="sxs-lookup"><span data-stu-id="c621e-116">ITU-T T.832: *Information technology – JPEG XR image coding system – Image coding specification*</span></span>
-   <span data-ttu-id="c621e-117">ISO/IEC 29199-2:2010: *Information technology — Jpeg XR image coding system — Part 2: Image coding specification*</span><span class="sxs-lookup"><span data-stu-id="c621e-117">ISO/IEC 29199-2:2010: *Information technology — JPEG XR image coding system — Part 2: Image coding specification*</span></span>

<span data-ttu-id="c621e-118">Lo standard JPEG XR è in gran parte basato sul formato [HD Photo,](hdphoto-format-overview.md) ma esistono alcune differenze tra i due formati.</span><span class="sxs-lookup"><span data-stu-id="c621e-118">The JPEG XR standard is largely based on the [HD Photo](hdphoto-format-overview.md) format, but there are some differences between the two formats.</span></span> <span data-ttu-id="c621e-119">In Windows 8, il codec HD Photo è stato aggiornato per supportare JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="c621e-119">In Windows 8, the HD Photo codec has been updated to support JPEG XR.</span></span> <span data-ttu-id="c621e-120">Il codificatore ora restituisce sempre un flusso di bit conforme a JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="c621e-120">The encoder now always outputs a JPEG XR–compliant bit stream.</span></span> <span data-ttu-id="c621e-121">Il decodificatore può decodificare immagini JPEG XR e HD Photo.</span><span class="sxs-lookup"><span data-stu-id="c621e-121">The decoder can decode both JPEG XR and HD Photo images.</span></span>

<span data-ttu-id="c621e-122">Sono stati apportati notevoli miglioramenti delle prestazioni, in relazione al codec HD Photo, al codec JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="c621e-122">Substantial performance improvements, in relation to the HD Photo codec, have been made to the JPEG XR codec.</span></span> <span data-ttu-id="c621e-123">Ad esempio, la decodifica delle immagini con risoluzione secondaria, ad esempio la generazione di anteprime, è stata migliorata, nonché la decodifica delle immagini a bassa risoluzione.</span><span class="sxs-lookup"><span data-stu-id="c621e-123">For example, sub-resolution image decoding, such as thumbnail generation, has been improved, as well as low-resolution image decoding.</span></span> <span data-ttu-id="c621e-124">È consigliabile usare il formato JPEG XR invece del formato HD Photo.</span><span class="sxs-lookup"><span data-stu-id="c621e-124">It is recommended that you use the JPEG XR format instead of the HD Photo format.</span></span>

## <a name="codec-information"></a><span data-ttu-id="c621e-125">Informazioni sui codec</span><span class="sxs-lookup"><span data-stu-id="c621e-125">Codec Information</span></span>



|      <span data-ttu-id="c621e-126">Componente</span><span class="sxs-lookup"><span data-stu-id="c621e-126">Component</span></span>      |    <span data-ttu-id="c621e-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c621e-127">Description</span></span>                                                          |
|---------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="c621e-128">Estensione del file</span><span class="sxs-lookup"><span data-stu-id="c621e-128">File name extension</span></span> | <span data-ttu-id="c621e-129">"jxr" e "wdp"</span><span class="sxs-lookup"><span data-stu-id="c621e-129">"jxr" and "wdp"</span></span>                                                         |
| <span data-ttu-id="c621e-130">GUID contenitore</span><span class="sxs-lookup"><span data-stu-id="c621e-130">Container GUID</span></span>      | <span data-ttu-id="c621e-131">**GUID \_ ContainerFormatWmp**</span><span class="sxs-lookup"><span data-stu-id="c621e-131">**GUID\_ContainerFormatWmp**</span></span>                                            |
| <span data-ttu-id="c621e-132">GUID decodificatore</span><span class="sxs-lookup"><span data-stu-id="c621e-132">Decoder GUID</span></span>        | <span data-ttu-id="c621e-133">**CLSID \_ WICWmpDecoder**</span><span class="sxs-lookup"><span data-stu-id="c621e-133">**CLSID\_WICWmpDecoder**</span></span>                                                |
| <span data-ttu-id="c621e-134">GUID del codificatore</span><span class="sxs-lookup"><span data-stu-id="c621e-134">Encoder GUID</span></span>        | <span data-ttu-id="c621e-135">**CLSID \_ WICWmpEncoder**</span><span class="sxs-lookup"><span data-stu-id="c621e-135">**CLSID\_WICWmpEncoder**</span></span>                                                |
| <span data-ttu-id="c621e-136">Supporto dei profili</span><span class="sxs-lookup"><span data-stu-id="c621e-136">Profile Support</span></span>     | <span data-ttu-id="c621e-137">Il codificatore e il decodificatore supportano fino al profilo principale e fino al livello 128.</span><span class="sxs-lookup"><span data-stu-id="c621e-137">The encoder and decoder support up to Main Profile and up to level 128.</span></span> |



 

## <a name="codec-features"></a><span data-ttu-id="c621e-138">Funzionalità dei codec</span><span class="sxs-lookup"><span data-stu-id="c621e-138">Codec Features</span></span>

### <a name="high-dynamic-range"></a><span data-ttu-id="c621e-139">High Dynamic Range</span><span class="sxs-lookup"><span data-stu-id="c621e-139">High Dynamic Range</span></span>

<span data-ttu-id="c621e-140">JPEG XR supporta immagini a intervalli dinamici elevati, usando colori a virgola mobile o a virgola fissa.</span><span class="sxs-lookup"><span data-stu-id="c621e-140">JPEG XR supports high-dynamic range images, using floating-point or fixed-point colors.</span></span> <span data-ttu-id="c621e-141">In questi formati di colore l'intervallo numerico di un pixel è maggiore dell'intervallo visibile, quindi è possibile regolare i colori al di sopra o al di sotto dell'intervallo visibile durante le fasi di elaborazione intermedie.</span><span class="sxs-lookup"><span data-stu-id="c621e-141">In these color formats, the numerical range of a pixel is larger than the visible range, so you can adjust colors above or below the visible range during intermediate processing stages.</span></span>

-   <span data-ttu-id="c621e-142">A virgola fissa: in una rappresentazione a virgola fissa, 0 rappresenta il nero e 1,0 rappresenta la saturazione massima.</span><span class="sxs-lookup"><span data-stu-id="c621e-142">Fixed-point: In a fixed-point representation, 0 represents black and 1.0 represents maximum saturation.</span></span> <span data-ttu-id="c621e-143">Il codec JPEG XR supporta sia i formati a virgola fissa a 16 che a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="c621e-143">The JPEG XR codec supports both 16-bit and 32-bit fixed-point formats.</span></span> <span data-ttu-id="c621e-144">Per 16 bit, 1,0 = 0x2000h, che fornisce 13 bit per l'intervallo \[ visibile 0...1. \]</span><span class="sxs-lookup"><span data-stu-id="c621e-144">For 16-bit, 1.0 = 0x2000h, which gives 13 bits for the visible range \[0...1\].</span></span> <span data-ttu-id="c621e-145">L'intervallo totale è compreso tra -4,0 e +3,999 e viene mappato in modo lineare.</span><span class="sxs-lookup"><span data-stu-id="c621e-145">The total range is –4.0 to +3.999, and is mapped linearly.</span></span> <span data-ttu-id="c621e-146">Per 32 bit, 1,0 = 0x01000000h, l'intervallo visibile è 24 bit e l'intervallo totale è compreso tra -128 e +127,999.</span><span class="sxs-lookup"><span data-stu-id="c621e-146">For 32-bit, 1.0 = 0x01000000h, the visible range is 24 bits, and the total range is –128 to +127.999.</span></span>
-   <span data-ttu-id="c621e-147">Virgola mobile: in una rappresentazione a virgola mobile, 0 rappresenta il nero e 1,0 rappresenta la saturazione massima.</span><span class="sxs-lookup"><span data-stu-id="c621e-147">Floating-point: In a floating-point representation, 0 represents black and 1.0 represents maximum saturation.</span></span> <span data-ttu-id="c621e-148">Il codec JPEG XR supporta sia i formati a virgola mobile a 16 bit che a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="c621e-148">The JPEG XR codec supports both 16-bit and 32-bit floating-point formats.</span></span>

### <a name="tiles"></a><span data-ttu-id="c621e-149">Riquadri</span><span class="sxs-lookup"><span data-stu-id="c621e-149">Tiles</span></span>

<span data-ttu-id="c621e-150">Un frame può essere partizionato in sottoaree rettangolari denominate *riquadri.*</span><span class="sxs-lookup"><span data-stu-id="c621e-150">A frame can be partitioned into rectangular subregions called *tiles*.</span></span> <span data-ttu-id="c621e-151">Un riquadro è un'area di un'immagine che contiene matrici rettangolari di macroblock.</span><span class="sxs-lookup"><span data-stu-id="c621e-151">A tile is an area of a image that contains rectangular arrays of macroblocks.</span></span> <span data-ttu-id="c621e-152">I riquadri consentono di decodificare le aree dell'immagine senza elaborare l'intera immagine.</span><span class="sxs-lookup"><span data-stu-id="c621e-152">Tiles enable regions of the image to be decoded without processing the entire image.</span></span>

<span data-ttu-id="c621e-153">Durante la codifica, selezionare il numero di riquadri impostando le **proprietà HorizontalTileSlices** e **VerticalTileSlices.**</span><span class="sxs-lookup"><span data-stu-id="c621e-153">During encoding, select the number of tiles by setting the **HorizontalTileSlices** and **VerticalTileSlices** properties.</span></span> <span data-ttu-id="c621e-154">Le dimensioni minime del riquadro sono 16 × 16 pixel.</span><span class="sxs-lookup"><span data-stu-id="c621e-154">The minimum tile size is 16 × 16 pixels.</span></span> <span data-ttu-id="c621e-155">Il codificatore regola il numero di riquadri per mantenere questa restrizione.</span><span class="sxs-lookup"><span data-stu-id="c621e-155">The encoder adjusts the number of tiles to maintain this restriction.</span></span> <span data-ttu-id="c621e-156">Esiste un sovraccarico di archiviazione ed elaborazione associato a ogni riquadro, pertanto è consigliabile considerare il numero di riquadri necessari per scenari specifici.</span><span class="sxs-lookup"><span data-stu-id="c621e-156">There is storage and processing overhead associated with each tile, so you should consider the number of tiles that are needed for particular scenarios.</span></span>

### <a name="image-stream-output"></a><span data-ttu-id="c621e-157">Output del flusso di immagini</span><span class="sxs-lookup"><span data-stu-id="c621e-157">Image Stream Output</span></span>

<span data-ttu-id="c621e-158">Lo standard JPEG-XR definisce due parti di un file JPEG-XR:</span><span class="sxs-lookup"><span data-stu-id="c621e-158">The JPEG-XR standard defines two parts of a JPEG-XR file:</span></span>

-   <span data-ttu-id="c621e-159">Flusso di bit dell'immagine, definito nel corpo dello standard.</span><span class="sxs-lookup"><span data-stu-id="c621e-159">The image bit stream, defined in the body of the standard.</span></span>
-   <span data-ttu-id="c621e-160">Contenitore di immagini.</span><span class="sxs-lookup"><span data-stu-id="c621e-160">The image container.</span></span> <span data-ttu-id="c621e-161">Il file contiene metadati Exif e XMP ed è definito nell'allegato A dello standard.</span><span class="sxs-lookup"><span data-stu-id="c621e-161">The file contains Exif and XMP metadata, and is defined in Annex A of the standard.</span></span>

<span data-ttu-id="c621e-162">È possibile, e consentito dallo standard, incorporare il flusso di immagini all'interno di un altro tipo di contenitore di file.</span><span class="sxs-lookup"><span data-stu-id="c621e-162">It is possible, and allowed by the standard, to embed the image stream inside another type of file container.</span></span> <span data-ttu-id="c621e-163">Il codificatore supporta una modalità solo flusso, che restituisce il flusso di bit dell'immagine non elaborata senza contenitore di immagini.</span><span class="sxs-lookup"><span data-stu-id="c621e-163">The encoder supports a stream-only mode, which outputs the raw image bit stream with no image container.</span></span> <span data-ttu-id="c621e-164">Un'applicazione può archiviare il flusso di bit in un altro formato di contenitore.</span><span class="sxs-lookup"><span data-stu-id="c621e-164">An application can store the bit stream in some other container format.</span></span>

<span data-ttu-id="c621e-165">Per abilitare la modalità solo flusso, impostare la **proprietà StreamOnly.**</span><span class="sxs-lookup"><span data-stu-id="c621e-165">To enable stream-only mode, set the **StreamOnly** property.</span></span>

### <a name="image-quality-settings"></a><span data-ttu-id="c621e-166">Impostazioni di qualità dell'immagine</span><span class="sxs-lookup"><span data-stu-id="c621e-166">Image Quality Settings</span></span>

<span data-ttu-id="c621e-167">Diverse proprietà del codec controllano la qualità dell'immagine di output dal codificatore.</span><span class="sxs-lookup"><span data-stu-id="c621e-167">Several codec properties control the quality of the output image from the encoder.</span></span>

-   <span data-ttu-id="c621e-168">[ImageQuality](#imagequality) è una proprietà comune nei codec WIC.</span><span class="sxs-lookup"><span data-stu-id="c621e-168">[ImageQuality](#imagequality) is a property common across WIC codecs.</span></span> <span data-ttu-id="c621e-169">Specifica la qualità dell'immagine come singolo valore a virgola mobile compreso tra 0,0 e 1,0,</span><span class="sxs-lookup"><span data-stu-id="c621e-169">It specifies image quality as a single floating-point value from 0.0–1.0,</span></span>
-   <span data-ttu-id="c621e-170">Le [proprietà Quality](#image-quality-settings), [Overlap](#overlap)e [Subsampling](#subsampling) offrono un maggiore controllo sulle impostazioni di qualità.</span><span class="sxs-lookup"><span data-stu-id="c621e-170">The [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties give more control over the quality settings.</span></span>

<span data-ttu-id="c621e-171">Per usare [le proprietà Quality](#image-quality-settings), [Overlap](#overlap)e [Subsampling,](#subsampling) impostare la [proprietà UseCodecOptions](#usecodecoptions) su VARIANT **\_ TRUE.**</span><span class="sxs-lookup"><span data-stu-id="c621e-171">To use the [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties, set the [UseCodecOptions](#usecodecoptions) property to **VARIANT\_TRUE**.</span></span>

<span data-ttu-id="c621e-172">Se [UseCodecOptions è](#usecodecoptions) **VARIANT \_ FALSE** (l'impostazione predefinita **è VARIANT \_ FALSE),** il codificatore usa la [proprietà ImageQuality.](#imagequality)</span><span class="sxs-lookup"><span data-stu-id="c621e-172">If [UseCodecOptions](#usecodecoptions) is **VARIANT\_FALSE** (**VARIANT\_FALSE** is the default) the encoder uses the [ImageQuality](#imagequality) property.</span></span> <span data-ttu-id="c621e-173">Il codificatore esegue il mapping del valore di ImageQuality a [Quality,](#image-quality-settings) [Overlap](#overlap)e [Subsampling](#subsampling) tramite una tabella di ricerca.</span><span class="sxs-lookup"><span data-stu-id="c621e-173">The encoder maps the value of ImageQuality to [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) through a lookup table.</span></span>

<span data-ttu-id="c621e-174">Il codificatore non supporta la **proprietà CompressionQuality.**</span><span class="sxs-lookup"><span data-stu-id="c621e-174">The encoder does not support the **CompressionQuality** property.</span></span>

### <a name="compressed-domain-transcode"></a><span data-ttu-id="c621e-175">Transcodifica di dominio compresso</span><span class="sxs-lookup"><span data-stu-id="c621e-175">Compressed Domain Transcode</span></span>

<span data-ttu-id="c621e-176">Il codec JPEG XR può eseguire determinate trasformazioni delle immagini senza decodificare effettivamente i dati compressi e ri-codificarlo.</span><span class="sxs-lookup"><span data-stu-id="c621e-176">The JPEG XR codec can perform certain image transformations without actually decoding the compressed data and re-encoding it.</span></span> <span data-ttu-id="c621e-177">Le operazioni di dominio compresso sono molto efficienti ed evitano qualsiasi perdita di qualità aggiuntiva tipica quando si decodifica e si ricodifica un'immagine compressa con perdita.</span><span class="sxs-lookup"><span data-stu-id="c621e-177">Compressed domain operations are very efficient and avoid any additional quality loss that is typical when you decode and re-encode a lossy-compressed image.</span></span>

<span data-ttu-id="c621e-178">Sono supportate le operazioni di dominio compresso seguenti:</span><span class="sxs-lookup"><span data-stu-id="c621e-178">The following compressed domain operations are supported:</span></span>

-   <span data-ttu-id="c621e-179">Ritagliare un'area dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="c621e-179">Crop a region of the image.</span></span>
-   <span data-ttu-id="c621e-180">Ruotare o capovolgere l'immagine.</span><span class="sxs-lookup"><span data-stu-id="c621e-180">Rotate or flip the image.</span></span>
-   <span data-ttu-id="c621e-181">Eliminare i dati relativi alla frequenza per creare un file di immagine più piccolo.</span><span class="sxs-lookup"><span data-stu-id="c621e-181">Discard frequency data to create a smaller image file.</span></span>
-   <span data-ttu-id="c621e-182">Riorganizzare l'immagine tra l'ordine spaziale e quello di frequenza.</span><span class="sxs-lookup"><span data-stu-id="c621e-182">Reorganize the image between spatial and frequency order.</span></span>

<span data-ttu-id="c621e-183">Il codificatore JPEG XR usa la transcodella di dominio compressa, se possibile, quando l'immagine di origine è un'immagine XR JPEG.</span><span class="sxs-lookup"><span data-stu-id="c621e-183">The JPEG XR encoder uses compressed domain transcoding, if possible, when the source image is a JPEG XR image.</span></span> <span data-ttu-id="c621e-184">Quando il codificatore esegue un'operazione di dominio compresso, ignora le proprietà del codec seguenti: [AlphaQuality,](#alphaquality) [ImageQuality,](#imagequality) [InterleavedAlpha,](#interleavedalpha) [Lossless](#lossless)[Overlap](#overlap)e [Quality.](#image-quality-settings)</span><span class="sxs-lookup"><span data-stu-id="c621e-184">When the encoder performs a compressed domain operation, it ignores the following codec properties: [AlphaQuality](#alphaquality), [ImageQuality](#imagequality), [InterleavedAlpha](#interleavedalpha), [Lossless](#lossless)[Overlap](#overlap), and [Quality](#image-quality-settings).</span></span> <span data-ttu-id="c621e-185">Se le [proprietà HorizontalTileSlices](/windows) e [VerticalTileSlices](/windows) sono presenti, è necessario impostarle su zero.</span><span class="sxs-lookup"><span data-stu-id="c621e-185">If the [HorizontalTileSlices](/windows) and [VerticalTileSlices](/windows) properties are present, you must set them to zero.</span></span> <span data-ttu-id="c621e-186">Non è possibile modificare le dimensioni del riquadro di un'immagine come parte di una transcodifica di dominio compressa.</span><span class="sxs-lookup"><span data-stu-id="c621e-186">You cannot change the tile size of an image as part of a compressed domain transcode.</span></span>

<span data-ttu-id="c621e-187">L'elenco seguente descrive come eseguire le trasformazioni delle immagini.</span><span class="sxs-lookup"><span data-stu-id="c621e-187">The follow list describes how to perform the image transformations.</span></span>

-   <span data-ttu-id="c621e-188">Per ritagliare l'immagine, impostare l'area desiderata nel [**parametro WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) del **metodo WriteSource.**</span><span class="sxs-lookup"><span data-stu-id="c621e-188">To crop the image, set the desired region in the [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) parameter of the **WriteSource** method.</span></span>
-   <span data-ttu-id="c621e-189">Per ruotare o capovolgere l'immagine, impostare la [proprietà BitmapTransform.](#bitmaptransform)</span><span class="sxs-lookup"><span data-stu-id="c621e-189">To rotate or flip the image, set the [BitmapTransform](#bitmaptransform) property.</span></span>
-   <span data-ttu-id="c621e-190">Per eliminare i dati relativi alla frequenza nell'immagine, impostare la [proprietà ImageDataDiscard.](#imagedatadiscard)</span><span class="sxs-lookup"><span data-stu-id="c621e-190">To discard frequency data in the image, set the [ImageDataDiscard](#imagedatadiscard) property.</span></span> <span data-ttu-id="c621e-191">Per eliminare i dati relativi alla frequenza nel canale alfa, impostare la [proprietà AlphaDataDiscard.](#alphadatadiscard)</span><span class="sxs-lookup"><span data-stu-id="c621e-191">To discard frequency data in the alpha channel, set the [AlphaDataDiscard](#alphadatadiscard) property.</span></span> <span data-ttu-id="c621e-192">La rimozione dei dati relativi alla frequenza riduce le dimensioni del file codificato e può ridurre la risoluzione.</span><span class="sxs-lookup"><span data-stu-id="c621e-192">Discarding frequency data reduces the encoded file size and can reduce the resolution.</span></span>
-   <span data-ttu-id="c621e-193">Per modificare l'organizzazione dell'immagine tra la frequenza e l'ordinamento spaziale, impostare la [proprietà FrequencyOrdering.](/windows)</span><span class="sxs-lookup"><span data-stu-id="c621e-193">To change the image organization between frequency and spatial ordering, set the [FrequencyOrdering](/windows) property.</span></span>

<span data-ttu-id="c621e-194">Per disabilitare la transcodifica del dominio compresso e forzare la ricodifica dell'immagine da parte del codificatore, impostare [UseCodecOptions](#usecodecoptions) su **VARIANT \_ TRUE** e [impostare CompressedDomainTranscode](#compresseddomaintranscode) su **VARIANT \_ FALSE.**</span><span class="sxs-lookup"><span data-stu-id="c621e-194">To disable compressed domain transcode and force the encoder to re-encode the image, set the [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE** and set [CompressedDomainTranscode](#compresseddomaintranscode) to **VARIANT\_FALSE**.</span></span>

## <a name="encoder-options"></a><span data-ttu-id="c621e-195">Opzioni del codificatore</span><span class="sxs-lookup"><span data-stu-id="c621e-195">Encoder Options</span></span>

<span data-ttu-id="c621e-196">Per impostare le proprietà di codifica, usare [**l'interfaccia IPropertyBag2.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c621e-196">To set encoding properties, use the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface.</span></span> <span data-ttu-id="c621e-197">Per altre informazioni, vedere Cenni [preliminari sulla codifica](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="c621e-197">For more information, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="c621e-198">L'elenco seguente specifica le opzioni del codificatore.</span><span class="sxs-lookup"><span data-stu-id="c621e-198">The following list specifies the encoder options.</span></span>

-   [<span data-ttu-id="c621e-199">AlphaDataDiscard</span><span class="sxs-lookup"><span data-stu-id="c621e-199">AlphaDataDiscard</span></span>](#alphadatadiscard)
-   [<span data-ttu-id="c621e-200">AlphaQuality</span><span class="sxs-lookup"><span data-stu-id="c621e-200">AlphaQuality</span></span>](#alphaquality)
-   [<span data-ttu-id="c621e-201">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="c621e-201">BitmapTransform</span></span>](#bitmaptransform)
-   [<span data-ttu-id="c621e-202">CompressedDomainTranscode</span><span class="sxs-lookup"><span data-stu-id="c621e-202">CompressedDomainTranscode</span></span>](#compresseddomaintranscode)
-   [<span data-ttu-id="c621e-203">FrequencyOrder</span><span class="sxs-lookup"><span data-stu-id="c621e-203">FrequencyOrder</span></span>](#frequencyorder)
-   [<span data-ttu-id="c621e-204">HorizontalTileSlices</span><span class="sxs-lookup"><span data-stu-id="c621e-204">HorizontalTileSlices</span></span>](#horizontaltileslices)
-   [<span data-ttu-id="c621e-205">IgnoreOverlap</span><span class="sxs-lookup"><span data-stu-id="c621e-205">IgnoreOverlap</span></span>](#ignoreoverlap)
-   [<span data-ttu-id="c621e-206">ImageDataDiscard</span><span class="sxs-lookup"><span data-stu-id="c621e-206">ImageDataDiscard</span></span>](#imagedatadiscard)
-   [<span data-ttu-id="c621e-207">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="c621e-207">ImageQuality</span></span>](#imagequality)
-   [<span data-ttu-id="c621e-208">InterleavedAlpha</span><span class="sxs-lookup"><span data-stu-id="c621e-208">InterleavedAlpha</span></span>](#interleavedalpha)
-   [<span data-ttu-id="c621e-209">Lossless</span><span class="sxs-lookup"><span data-stu-id="c621e-209">Lossless</span></span>](#lossless)
-   [<span data-ttu-id="c621e-210">Overlap</span><span class="sxs-lookup"><span data-stu-id="c621e-210">Overlap</span></span>](#overlap)
-   [<span data-ttu-id="c621e-211">Modalità progressiva</span><span class="sxs-lookup"><span data-stu-id="c621e-211">ProgressiveMode</span></span>](#progressivemode)
-   [<span data-ttu-id="c621e-212">Qualità</span><span class="sxs-lookup"><span data-stu-id="c621e-212">Quality</span></span>](#image-quality-settings)
-   [<span data-ttu-id="c621e-213">StreamOnly</span><span class="sxs-lookup"><span data-stu-id="c621e-213">StreamOnly</span></span>](#streamonly)
-   [<span data-ttu-id="c621e-214">Sottocampionamento</span><span class="sxs-lookup"><span data-stu-id="c621e-214">Subsampling</span></span>](#subsampling)
-   [<span data-ttu-id="c621e-215">UseCodecOptions</span><span class="sxs-lookup"><span data-stu-id="c621e-215">UseCodecOptions</span></span>](#usecodecoptions)
-   [<span data-ttu-id="c621e-216">VerticalTileSlices</span><span class="sxs-lookup"><span data-stu-id="c621e-216">VerticalTileSlices</span></span>](#verticaltileslices)

### <a name="alphadatadiscard"></a><span data-ttu-id="c621e-217">AlphaDataDiscard</span><span class="sxs-lookup"><span data-stu-id="c621e-217">AlphaDataDiscard</span></span>

<span data-ttu-id="c621e-218">Imposta la quantità di dati di frequenza alfa da eliminare durante la transcodifica di un dominio compresso.</span><span class="sxs-lookup"><span data-stu-id="c621e-218">Sets the amount of alpha frequency data to discard during a compressed domain transcode.</span></span>



| <span data-ttu-id="c621e-219">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c621e-219">Data type</span></span> | <span data-ttu-id="c621e-220">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c621e-220">VARTYPE</span></span>     | <span data-ttu-id="c621e-221">Intervallo</span><span class="sxs-lookup"><span data-stu-id="c621e-221">Range</span></span> | <span data-ttu-id="c621e-222">Predefinito</span><span class="sxs-lookup"><span data-stu-id="c621e-222">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="c621e-223">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="c621e-223">**UCHAR**</span></span> | <span data-ttu-id="c621e-224">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="c621e-224">**VT\_UI1**</span></span> | <span data-ttu-id="c621e-225">0–4</span><span class="sxs-lookup"><span data-stu-id="c621e-225">0–4</span></span>   | <span data-ttu-id="c621e-226">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c621e-226">None</span></span>    |



 

<span data-ttu-id="c621e-227">Questa proprietà si applica solo se la proprietà [CompressedDomainTranscode](#compresseddomaintranscode) è impostata su **VARIANT \_ TRUE** e l'immagine contiene un canale alfa planare o un canale alfa interleaved; in caso contrario, viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="c621e-227">This property applies only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE** and the image contains either a planar alpha channel or interleaved alpha channel; otherwise it is ignored.</span></span>

<span data-ttu-id="c621e-228">Per le immagini che contengono un canale alfa planare, sono validi i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c621e-228">For images that contain a planar alpha channel, the following values are valid.</span></span>



| <span data-ttu-id="c621e-229">Valore</span><span class="sxs-lookup"><span data-stu-id="c621e-229">Value</span></span> | <span data-ttu-id="c621e-230">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c621e-230">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c621e-231">0</span><span class="sxs-lookup"><span data-stu-id="c621e-231">0</span></span>     | <span data-ttu-id="c621e-232">Non viene eliminato nessun dato di frequenza dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="c621e-232">No image frequency data is discarded.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="c621e-233">1</span><span class="sxs-lookup"><span data-stu-id="c621e-233">1</span></span>     | <span data-ttu-id="c621e-234">I flexbit vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="c621e-234">The flexbits are discarded.</span></span> <span data-ttu-id="c621e-235">In questo modo si riduce arbitrariamente la qualità del canale alfa planare per l'immagine transcodificata.</span><span class="sxs-lookup"><span data-stu-id="c621e-235">This arbitrarily reduces the quality of the planar alpha channel for the transcoded image.</span></span> <span data-ttu-id="c621e-236">, senza alcuna modifica nella risoluzione effettiva.</span><span class="sxs-lookup"><span data-stu-id="c621e-236">, without a change in the effective resolution.</span></span> <span data-ttu-id="c621e-237">La riduzione esatta delle dimensioni e della qualità del file dipende da numerosi fattori e non può essere specificata esattamente.</span><span class="sxs-lookup"><span data-stu-id="c621e-237">The exact reduction in file size and quality depends on numerous factors and cannot be exactly specified.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="c621e-238">2</span><span class="sxs-lookup"><span data-stu-id="c621e-238">2</span></span>     | <span data-ttu-id="c621e-239">La banda di dati a frequenza elevata viene eliminata, inclusi i flexbit.</span><span class="sxs-lookup"><span data-stu-id="c621e-239">The high-pass frequency data band is discarded, including the flexbits.</span></span> <span data-ttu-id="c621e-240">Ciò riduce in modo efficace la risoluzione del canale alfa planare di un fattore di 4 in entrambe le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="c621e-240">This effectively reduces the resolution of the planar alpha channel by a factor of 4 in both dimensions.</span></span> <span data-ttu-id="c621e-241">Le dimensioni effettive dell'immagine transcodificata rimangono invariate, ma l'immagine perde tutti i dettagli in ogni blocco 4x4 di pixel del canale alfa.</span><span class="sxs-lookup"><span data-stu-id="c621e-241">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 4x4 block of alpha-channel pixels.</span></span> <span data-ttu-id="c621e-242">In genere, è consigliabile impostare questo valore solo quando la [proprietà ImageDataDiscard](#imagedatadiscard) ha lo stesso valore.</span><span class="sxs-lookup"><span data-stu-id="c621e-242">Typically, you should set this value only when the [ImageDataDiscard](#imagedatadiscard) property has the same value.</span></span>                            |
| <span data-ttu-id="c621e-243">3</span><span class="sxs-lookup"><span data-stu-id="c621e-243">3</span></span>     | <span data-ttu-id="c621e-244">Entrambe le bande dati con frequenza high pass e low-pass vengono eliminate, inclusi i flexbit.</span><span class="sxs-lookup"><span data-stu-id="c621e-244">Both the high-pass and low-pass frequency data bands are discarded, including the flexbits.</span></span> <span data-ttu-id="c621e-245">Questo riduce in modo ffectiva la risoluzione del canale alfa planare di un fattore di 16 in entrambe le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="c621e-245">This ffectively reduces the resolution of the planar alpha channel by a factor of 16 in both dimensions.</span></span> <span data-ttu-id="c621e-246">Le dimensioni effettive dell'immagine transcodificata rimangono invariate, ma l'immagine perde tutti i dettagli in ogni macroblocco 16x16 di pixel del canale alfa.</span><span class="sxs-lookup"><span data-stu-id="c621e-246">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 16x16 macroblock of alpha-channel pixels.</span></span> <span data-ttu-id="c621e-247">In genere, è consigliabile impostare questo valore solo quando la [proprietà ImageDataDiscard](#imagedatadiscard) ha lo stesso valore.</span><span class="sxs-lookup"><span data-stu-id="c621e-247">Typically, you should set this value only when the [ImageDataDiscard](#imagedatadiscard) property has the same value.</span></span> |
| <span data-ttu-id="c621e-248">4</span><span class="sxs-lookup"><span data-stu-id="c621e-248">4</span></span>     | <span data-ttu-id="c621e-249">Il canale alfa viene eliminato completamente.</span><span class="sxs-lookup"><span data-stu-id="c621e-249">The alpha channel is completely discarded.</span></span> <span data-ttu-id="c621e-250">Il formato pixel dell'immagine transcodificata viene modificato per riflettere la rimozione del canale alfa.</span><span class="sxs-lookup"><span data-stu-id="c621e-250">The pixel format of the transcoded image is changed to reflect the removal of the alpha channel.</span></span>                                                                                                                                                                                                                                                                                                                                |



 

<span data-ttu-id="c621e-251">Per le immagini che contengono un canale alfa interleaved, il valore seguente è valido.</span><span class="sxs-lookup"><span data-stu-id="c621e-251">For images that contain an interleaved alpha channel, the following value is valid.</span></span>



| <span data-ttu-id="c621e-252">Valore</span><span class="sxs-lookup"><span data-stu-id="c621e-252">Value</span></span> | <span data-ttu-id="c621e-253">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c621e-253">Description</span></span>                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c621e-254">4</span><span class="sxs-lookup"><span data-stu-id="c621e-254">4</span></span>     | <span data-ttu-id="c621e-255">Il canale alfa viene eliminato completamente.</span><span class="sxs-lookup"><span data-stu-id="c621e-255">The alpha channel is completely discarded.</span></span> <span data-ttu-id="c621e-256">Il formato pixel dell'immagine transcodificata viene modificato per riflettere la rimozione del canale alfa.</span><span class="sxs-lookup"><span data-stu-id="c621e-256">The pixel format of the transcoded image is changed to reflect the removal of the alpha channel.</span></span> |



 

<span data-ttu-id="c621e-257">Per i valori alfa interleaved, a meno che questa proprietà non sia impostata su 4, il canale alfa viene elaborato come i dati dell'immagine, in base al valore della [proprietà ImageDataDiscard.](#imagedatadiscard)</span><span class="sxs-lookup"><span data-stu-id="c621e-257">For interleaved alpha, unless this property is set to 4, the alpha channel is processed the same as the image data, according to the value of the [ImageDataDiscard](#imagedatadiscard) property.</span></span>

### <a name="alphaquality"></a><span data-ttu-id="c621e-258">AlphaQuality</span><span class="sxs-lookup"><span data-stu-id="c621e-258">AlphaQuality</span></span>

<span data-ttu-id="c621e-259">Imposta la qualità di compressione per l'immagine del canale alfa planare.</span><span class="sxs-lookup"><span data-stu-id="c621e-259">Sets the compression quality for the planar alpha channel image.</span></span>



| <span data-ttu-id="c621e-260">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c621e-260">Data type</span></span> | <span data-ttu-id="c621e-261">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c621e-261">VARTYPE</span></span>     | <span data-ttu-id="c621e-262">Intervallo</span><span class="sxs-lookup"><span data-stu-id="c621e-262">Range</span></span> | <span data-ttu-id="c621e-263">Predefinito</span><span class="sxs-lookup"><span data-stu-id="c621e-263">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="c621e-264">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="c621e-264">**UCHAR**</span></span> | <span data-ttu-id="c621e-265">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="c621e-265">**VT\_UI1**</span></span> | <span data-ttu-id="c621e-266">1–255</span><span class="sxs-lookup"><span data-stu-id="c621e-266">1–255</span></span> | <span data-ttu-id="c621e-267">1</span><span class="sxs-lookup"><span data-stu-id="c621e-267">1</span></span>       |



 

<span data-ttu-id="c621e-268">Questa proprietà si applica quando l'immagine ha un canale alfa e la [proprietà InterleavedAlpha](#interleavedalpha) è **VARIANT \_ FALSE.**</span><span class="sxs-lookup"><span data-stu-id="c621e-268">This property applies when the image has an alpha channel and the [InterleavedAlpha](#interleavedalpha) property is **VARIANT\_FALSE**.</span></span> <span data-ttu-id="c621e-269">Il valore 1 indica la modalità senza perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="c621e-269">The value 1 indicates lossless mode.</span></span> <span data-ttu-id="c621e-270">L'aumento dei valori comporta rapporti di compressione più elevati e una qualità dell'immagine inferiore.</span><span class="sxs-lookup"><span data-stu-id="c621e-270">Increasing values result in higher compression ratios and lower image quality.</span></span>

### <a name="bitmaptransform"></a><span data-ttu-id="c621e-271">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="c621e-271">BitmapTransform</span></span>

<span data-ttu-id="c621e-272">Specifica se l'immagine viene ruotata o capovolta quando viene decodificata.</span><span class="sxs-lookup"><span data-stu-id="c621e-272">Specifies whether the image is rotated or flipped when decoded.</span></span>



| <span data-ttu-id="c621e-273">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c621e-273">Data type</span></span> | <span data-ttu-id="c621e-274">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c621e-274">VARTYPE</span></span>     | <span data-ttu-id="c621e-275">Intervallo</span><span class="sxs-lookup"><span data-stu-id="c621e-275">Range</span></span>                                                                     | <span data-ttu-id="c621e-276">Predefinito</span><span class="sxs-lookup"><span data-stu-id="c621e-276">Default</span></span>                       |
|-----------|-------------|---------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="c621e-277">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="c621e-277">**UCHAR**</span></span> | <span data-ttu-id="c621e-278">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="c621e-278">**VT\_UI1**</span></span> | [<span data-ttu-id="c621e-279">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="c621e-279">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | <span data-ttu-id="c621e-280">**WICBitmapTransformRotate0**</span><span class="sxs-lookup"><span data-stu-id="c621e-280">**WICBitmapTransformRotate0**</span></span> |



 

### <a name="compresseddomaintranscode"></a><span data-ttu-id="c621e-281">CompressedDomainTranscode</span><span class="sxs-lookup"><span data-stu-id="c621e-281">CompressedDomainTranscode</span></span>

<span data-ttu-id="c621e-282">Abilita o disabilita la transcoding di domini compressi.</span><span class="sxs-lookup"><span data-stu-id="c621e-282">Enables or disables compressed domain transcoding.</span></span>



| <span data-ttu-id="c621e-283">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c621e-283">Data type</span></span>         | <span data-ttu-id="c621e-284">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c621e-284">VARTYPE</span></span>      | <span data-ttu-id="c621e-285">Predefinito</span><span class="sxs-lookup"><span data-stu-id="c621e-285">Default</span></span>           |
|-------------------|--------------|-------------------|
| <span data-ttu-id="c621e-286">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="c621e-286">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="c621e-287">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="c621e-287">**VT\_BOOL**</span></span> | <span data-ttu-id="c621e-288">**VARIANT \_ TRUE**</span><span class="sxs-lookup"><span data-stu-id="c621e-288">**VARIANT\_TRUE**</span></span> |



 

<span data-ttu-id="c621e-289">Per disabilitare le operazioni di dominio compresso, impostare questa proprietà su **VARIANT \_ FALSE.**</span><span class="sxs-lookup"><span data-stu-id="c621e-289">To disable compressed domain operations, set this property to **VARIANT\_FALSE**.</span></span>

### <a name="frequencyorder"></a><span data-ttu-id="c621e-290">FrequencyOrder</span><span class="sxs-lookup"><span data-stu-id="c621e-290">FrequencyOrder</span></span>

<span data-ttu-id="c621e-291">Abilita la codifica nell'ordine di frequenza.</span><span class="sxs-lookup"><span data-stu-id="c621e-291">Enables encoding in frequency order.</span></span> <span data-ttu-id="c621e-292">Le implementazioni dei dispositivi dei codificatori JPEG XR possono organizzare un file in ordine spaziale per ridurre la memoria necessaria durante la codifica.</span><span class="sxs-lookup"><span data-stu-id="c621e-292">Device implementations of JPEG XR encoders can organize a file in spatial order to reduce the memory required during encoding.</span></span>



| <span data-ttu-id="c621e-293">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c621e-293">Data type</span></span>         | <span data-ttu-id="c621e-294">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c621e-294">VARTYPE</span></span>      | <span data-ttu-id="c621e-295">Predefinito</span><span class="sxs-lookup"><span data-stu-id="c621e-295">Default</span></span>           |
|-------------------|--------------|-------------------|
| <span data-ttu-id="c621e-296">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="c621e-296">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="c621e-297">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="c621e-297">**VT\_BOOL**</span></span> | <span data-ttu-id="c621e-298">**VARIANT \_ TRUE**</span><span class="sxs-lookup"><span data-stu-id="c621e-298">**VARIANT\_TRUE**</span></span> |



 

-   <span data-ttu-id="c621e-299">**VARIANT \_ TRUE:** ordine della frequenza.</span><span class="sxs-lookup"><span data-stu-id="c621e-299">**VARIANT\_TRUE**: Frequency order.</span></span> <span data-ttu-id="c621e-300">I dati con la frequenza più bassa vengono visualizzati per primi nel file e il contenuto dell'immagine viene raggruppato in base alla frequenza anziché all'orientamento spaziale.</span><span class="sxs-lookup"><span data-stu-id="c621e-300">The lowest frequency data appears first in the file, and image content is grouped by its frequency rather than its spatial orientation.</span></span> <span data-ttu-id="c621e-301">L'organizzazione di un file in base all'ordine di frequenza offre prestazioni ottimali per qualsiasi decodifica basata sulla frequenza.</span><span class="sxs-lookup"><span data-stu-id="c621e-301">Organizing a file by frequency order provides the best performance for any frequency-based decoding.</span></span>
-   <span data-ttu-id="c621e-302">**VARIANT \_ FALSE:** ordine spaziale.</span><span class="sxs-lookup"><span data-stu-id="c621e-302">**VARIANT\_FALSE**: Spatial order.</span></span> <span data-ttu-id="c621e-303">L'ordine spaziale riduce la memoria necessaria durante la codifica</span><span class="sxs-lookup"><span data-stu-id="c621e-303">Spatial order reduces the memory required during encoding</span></span>

<span data-ttu-id="c621e-304">L'ordine di frequenza è consigliato a meno che non si abbia un motivo specifico per le prestazioni o l'applicazione per usare l'ordine spaziale.</span><span class="sxs-lookup"><span data-stu-id="c621e-304">Frequency order is recommended unless you have performance or application-specific reasons to use spatial order.</span></span>

### <a name="horizontaltileslices"></a><span data-ttu-id="c621e-305">HorizontalTileSlices</span><span class="sxs-lookup"><span data-stu-id="c621e-305">HorizontalTileSlices</span></span>

<span data-ttu-id="c621e-306">Imposta il numero di riquadri orizzontali.</span><span class="sxs-lookup"><span data-stu-id="c621e-306">Sets the number of horizontal tiles.</span></span>



| <span data-ttu-id="c621e-307">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c621e-307">Data type</span></span>  | <span data-ttu-id="c621e-308">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c621e-308">VARTYPE</span></span>     | <span data-ttu-id="c621e-309">Intervallo</span><span class="sxs-lookup"><span data-stu-id="c621e-309">Range</span></span>  | <span data-ttu-id="c621e-310">Predefinito</span><span class="sxs-lookup"><span data-stu-id="c621e-310">Default</span></span>                      |
|------------|-------------|--------|------------------------------|
| <span data-ttu-id="c621e-311">**Ushort**</span><span class="sxs-lookup"><span data-stu-id="c621e-311">**USHORT**</span></span> | <span data-ttu-id="c621e-312">**Interfaccia utente \_ VT 2**</span><span class="sxs-lookup"><span data-stu-id="c621e-312">**VT\_UI2**</span></span> | <span data-ttu-id="c621e-313">0–4095</span><span class="sxs-lookup"><span data-stu-id="c621e-313">0–4095</span></span> | <span data-ttu-id="c621e-314">(larghezza immagine - 1) >> 8</span><span class="sxs-lookup"><span data-stu-id="c621e-314">(image width – 1) >> 8</span></span> |



 

<span data-ttu-id="c621e-315">Il valore è il numero di suddivisioni orizzontali. cio, il numero di riquadri orizzontali - 1.</span><span class="sxs-lookup"><span data-stu-id="c621e-315">The value is the number of horizontal subdivisions; that is, the number of horizontal tiles – 1.</span></span>

### <a name="ignoreoverlap"></a><span data-ttu-id="c621e-316">IgnoreOverlap</span><span class="sxs-lookup"><span data-stu-id="c621e-316">IgnoreOverlap</span></span>

<span data-ttu-id="c621e-317">Specifica il modo in cui il codificatore gestisce i limiti del riquadro durante una transcodifica di dominio compressa.</span><span class="sxs-lookup"><span data-stu-id="c621e-317">Specifies how the encoder handles tile boundaries during a compressed domain transcode.</span></span>



| <span data-ttu-id="c621e-318">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c621e-318">Data type</span></span>         | <span data-ttu-id="c621e-319">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c621e-319">VARTYPE</span></span>      | <span data-ttu-id="c621e-320">Predefinito</span><span class="sxs-lookup"><span data-stu-id="c621e-320">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="c621e-321">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="c621e-321">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="c621e-322">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="c621e-322">**VT\_BOOL**</span></span> | <span data-ttu-id="c621e-323">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="c621e-323">**VARIANT\_FALSE**</span></span> |



 

<span data-ttu-id="c621e-324">Questa proprietà viene applicata solo se la [proprietà CompressedDomainTranscode](#compresseddomaintranscode) è impostata su **VARIANT \_ TRUE** e viene eseguita una transcodifica di sottoarea di esattamente uno o più riquadri.</span><span class="sxs-lookup"><span data-stu-id="c621e-324">This property is applied only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE** and a sub-region transcode of exactly one or more tiles is performed.</span></span>

<span data-ttu-id="c621e-325">L'operazione predefinita per una transcodifica di area è espandere l'area richiesta in modo da includere i pixel circostanti necessari per la decodifica di sovrapposizione dei bordi dell'area.</span><span class="sxs-lookup"><span data-stu-id="c621e-325">The default operation for a region transcode is to expand the requested region to include the surrounding pixels that are required for overlap decoding of the region edges.</span></span> <span data-ttu-id="c621e-326">Se questa proprietà è impostata su **VARIANT \_ TRUE,** il codec ignora i pixel circostanti e vengono estratti solo il riquadro o i riquadri selezionati.</span><span class="sxs-lookup"><span data-stu-id="c621e-326">If this property is set to **VARIANT\_TRUE**, the codec ignores the surrounding pixels, and only the selected tile or tiles are extracted.</span></span> <span data-ttu-id="c621e-327">Se l'immagine di origine non è affiancata o se l'area richiesta include riquadri parziali, questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="c621e-327">If the source image is not tiled or if the requested region includes partial tiles, this parameter is ignored.</span></span>

### <a name="imagedatadiscard"></a><span data-ttu-id="c621e-328">ImageDataDiscard</span><span class="sxs-lookup"><span data-stu-id="c621e-328">ImageDataDiscard</span></span>

<span data-ttu-id="c621e-329">Imposta la quantità di dati di frequenza delle immagini da eliminare durante la transcodifica di un dominio compresso.</span><span class="sxs-lookup"><span data-stu-id="c621e-329">Sets the amount of image frequency data to discard during a compressed domain transcode.</span></span>



| <span data-ttu-id="c621e-330">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c621e-330">Data type</span></span> | <span data-ttu-id="c621e-331">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c621e-331">VARTYPE</span></span>     | <span data-ttu-id="c621e-332">Intervallo</span><span class="sxs-lookup"><span data-stu-id="c621e-332">Range</span></span> | <span data-ttu-id="c621e-333">Predefinito</span><span class="sxs-lookup"><span data-stu-id="c621e-333">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="c621e-334">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="c621e-334">**UCHAR**</span></span> | <span data-ttu-id="c621e-335">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="c621e-335">**VT\_UI1**</span></span> | <span data-ttu-id="c621e-336">0–3</span><span class="sxs-lookup"><span data-stu-id="c621e-336">0–3</span></span>   | <span data-ttu-id="c621e-337">0</span><span class="sxs-lookup"><span data-stu-id="c621e-337">0</span></span>       |



 

<span data-ttu-id="c621e-338">Questa proprietà si applica solo se la [proprietà CompressedDomainTranscode](#compresseddomaintranscode) è impostata su **VARIANT \_ TRUE;** in caso contrario, viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="c621e-338">This property applies only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE**; otherwise it is ignored.</span></span>



| <span data-ttu-id="c621e-339">Valore</span><span class="sxs-lookup"><span data-stu-id="c621e-339">Value</span></span> | <span data-ttu-id="c621e-340">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c621e-340">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c621e-341">0</span><span class="sxs-lookup"><span data-stu-id="c621e-341">0</span></span>     | <span data-ttu-id="c621e-342">Non viene eliminato nessun dato di frequenza dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="c621e-342">No image frequency data is discarded.</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="c621e-343">1</span><span class="sxs-lookup"><span data-stu-id="c621e-343">1</span></span>     | <span data-ttu-id="c621e-344">I flexbit vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="c621e-344">The flexbits are discarded.</span></span> <span data-ttu-id="c621e-345">In questo modo si riduce arbitrariamente la qualità dell'immagine transcodificata senza modificare la risoluzione effettiva dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="c621e-345">This arbitrarily reduces the quality of the transcoded image without changing the effective resolution of the image.</span></span> <span data-ttu-id="c621e-346">La riduzione esatta delle dimensioni e della qualità del file dipende da numerosi fattori e non può essere specificata esattamente.</span><span class="sxs-lookup"><span data-stu-id="c621e-346">The exact reduction in file size and quality depends on numerous factors and cannot be exactly specified.</span></span> <span data-ttu-id="c621e-347">Questo valore restituisce un errore specificato per un canale alfa interleaved.</span><span class="sxs-lookup"><span data-stu-id="c621e-347">This value returns an error specified for an interleaved alpha channel.</span></span>                                                                                |
| <span data-ttu-id="c621e-348">2</span><span class="sxs-lookup"><span data-stu-id="c621e-348">2</span></span>     | <span data-ttu-id="c621e-349">La banda di dati a frequenza elevata viene eliminata, inclusi i flexbit.</span><span class="sxs-lookup"><span data-stu-id="c621e-349">The high-pass frequency data band is discarded, including the flexbits.</span></span> <span data-ttu-id="c621e-350">In questo modo si riduce la risoluzione dell'immagine transcodificata di un fattore 4 in entrambe le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="c621e-350">This reduces the resolution of the transcoded image by a factor of 4 in both dimensions.</span></span> <span data-ttu-id="c621e-351">Le dimensioni effettive dell'immagine transcodificata rimangono invariate, ma l'immagine perde tutti i dettagli in ogni blocco di pixel 4x4.</span><span class="sxs-lookup"><span data-stu-id="c621e-351">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 4x4 block of pixels.</span></span> <span data-ttu-id="c621e-352">Pertanto, l'immagine transcodificata deve essere sottocampionata di conseguenza ogni volta che viene decodificata.</span><span class="sxs-lookup"><span data-stu-id="c621e-352">Therefore, the transcoded image should be downsampled accordingly whenever it is decoded.</span></span>                             |
| <span data-ttu-id="c621e-353">3</span><span class="sxs-lookup"><span data-stu-id="c621e-353">3</span></span>     | <span data-ttu-id="c621e-354">Entrambe le bande di dati con frequenza high pass e low-pass vengono eliminate, inclusi i flexbit.</span><span class="sxs-lookup"><span data-stu-id="c621e-354">Both the high-pass and low-pass frequency data bands are discarded, including the flexbits.</span></span> <span data-ttu-id="c621e-355">In questo modo si riduce la risoluzione dell'immagine transcodificata di un fattore di 16 in entrambe le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="c621e-355">This reduces the resolution of the transcoded image by a factor of 16 in both dimensions.</span></span> <span data-ttu-id="c621e-356">Le dimensioni effettive dell'immagine transcodificata rimangono invariate, ma l'immagine perde tutti i dettagli in ogni macroblock di pixel 16x16.</span><span class="sxs-lookup"><span data-stu-id="c621e-356">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 16x16 macroblock of pixels.</span></span> <span data-ttu-id="c621e-357">Pertanto, l'immagine transcodificata deve essere sottocampionata di conseguenza ogni volta che viene decodificata.</span><span class="sxs-lookup"><span data-stu-id="c621e-357">Therefore, the transcoded image should be downsampled accordingly whenever it is decoded.</span></span> |



 

<span data-ttu-id="c621e-358">Se l'immagine contiene un canale alfa interleaved, il valore di [ImageDataDiscard](#imagedatadiscard) viene applicato al canale alfa a meno che la proprietà [AlphaDataDiscard](#alphadatadiscard) non sia impostata su 4, nel qual caso il canale alfa viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="c621e-358">If the image contains an interleaved alpha channel, the value of [ImageDataDiscard](#imagedatadiscard) is applied to the alpha channel unless the [AlphaDataDiscard](#alphadatadiscard) property is set to 4, in which case the alpha channel is discarded.</span></span>

<span data-ttu-id="c621e-359">Per il valore alfa planare, i dati di frequenza che vengono eliminati sono controllati dalla [proprietà AlphaDataDiscard.](#alphadatadiscard)</span><span class="sxs-lookup"><span data-stu-id="c621e-359">For planar alpha, the frequency data that is discarded is controlled by the [AlphaDataDiscard](#alphadatadiscard) property.</span></span>

### <a name="imagequality"></a><span data-ttu-id="c621e-360">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="c621e-360">ImageQuality</span></span>

<span data-ttu-id="c621e-361">Imposta la qualità dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="c621e-361">Sets the image quality.</span></span>



| <span data-ttu-id="c621e-362">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c621e-362">Data type</span></span> | <span data-ttu-id="c621e-363">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c621e-363">VARTYPE</span></span>    | <span data-ttu-id="c621e-364">Intervallo</span><span class="sxs-lookup"><span data-stu-id="c621e-364">Range</span></span> | <span data-ttu-id="c621e-365">Predefinito</span><span class="sxs-lookup"><span data-stu-id="c621e-365">Default</span></span> |
|-----------|------------|-------|---------|
| <span data-ttu-id="c621e-366">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="c621e-366">**FLOAT**</span></span> | <span data-ttu-id="c621e-367">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="c621e-367">**VT\_R4**</span></span> | <span data-ttu-id="c621e-368">0–1.0</span><span class="sxs-lookup"><span data-stu-id="c621e-368">0–1.0</span></span> | <span data-ttu-id="c621e-369">0.9</span><span class="sxs-lookup"><span data-stu-id="c621e-369">0.9</span></span>     |



 

<span data-ttu-id="c621e-370">Il livello 1.0 offre una compressione matematicamente senza perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="c621e-370">Level 1.0 gives mathematically lossless compression.</span></span>

<span data-ttu-id="c621e-371">Livello 0.0 è l'impostazione di qualità più bassa.</span><span class="sxs-lookup"><span data-stu-id="c621e-371">Level 0.0 is the lowest quality setting.</span></span>

### <a name="interleavedalpha"></a><span data-ttu-id="c621e-372">InterleavedAlpha</span><span class="sxs-lookup"><span data-stu-id="c621e-372">InterleavedAlpha</span></span>

<span data-ttu-id="c621e-373">Specifica se codificare alfa interleaved o alfa planare.</span><span class="sxs-lookup"><span data-stu-id="c621e-373">Specifies whether to encode interleaved alpha or planar alpha.</span></span>



| <span data-ttu-id="c621e-374">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c621e-374">Data type</span></span>         | <span data-ttu-id="c621e-375">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c621e-375">VARTYPE</span></span>      | <span data-ttu-id="c621e-376">Predefinito</span><span class="sxs-lookup"><span data-stu-id="c621e-376">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="c621e-377">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="c621e-377">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="c621e-378">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="c621e-378">**VT\_BOOL**</span></span> | <span data-ttu-id="c621e-379">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="c621e-379">**VARIANT\_FALSE**</span></span> |



 

-   <span data-ttu-id="c621e-380">**VARIANT \_ TRUE:** alfa interleaved.</span><span class="sxs-lookup"><span data-stu-id="c621e-380">**VARIANT\_TRUE**: Interleaved alpha.</span></span> <span data-ttu-id="c621e-381">Le informazioni sul canale alfa vengono codificate come canale interleaved aggiuntivo, senza correlazione con i canali di contenuto dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="c621e-381">Alpha channel information is encoded as an additional interleaved channel, with no correlation to the image content channels.</span></span> <span data-ttu-id="c621e-382">Questa modalità è utile per decodificare alfa contemporaneamente all'immagine quando l'immagine è in streaming.</span><span class="sxs-lookup"><span data-stu-id="c621e-382">This mode is useful for decoding alpha simultaneously with the image when the image is streaming.</span></span>
-   <span data-ttu-id="c621e-383">VARIANT \_ FALSE: alfa planare.</span><span class="sxs-lookup"><span data-stu-id="c621e-383">VARIANT\_FALSE: Planar alpha.</span></span> <span data-ttu-id="c621e-384">Un canale alfa planare viene codificato come immagine separata.</span><span class="sxs-lookup"><span data-stu-id="c621e-384">A planar alpha channel is encoded as a separate image.</span></span> <span data-ttu-id="c621e-385">I dati dell'immagine e il canale alfa vengono decodificati in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="c621e-385">The image data and the alpha channel are decoded independently.</span></span> <span data-ttu-id="c621e-386">Facoltativamente, è possibile impostare il livello di qualità del canale alfa impostando la [proprietà AlphaQuality.](#alphaquality)</span><span class="sxs-lookup"><span data-stu-id="c621e-386">Optionally, you can set the quality level of the alpha channel by setting the [AlphaQuality](#alphaquality) property.</span></span>

<span data-ttu-id="c621e-387">L'alfa interfoliato è supportato solo per determinati formati di pixel RGB.</span><span class="sxs-lookup"><span data-stu-id="c621e-387">Interleaved alpha is supported only for certain RGB pixel formats.</span></span> <span data-ttu-id="c621e-388">Planare alpha è supportato per qualsiasi formato di immagine che definisce un canale alfa.</span><span class="sxs-lookup"><span data-stu-id="c621e-388">Planar alpha is supported for any image format that defines an alpha channel.</span></span>

### <a name="lossless"></a><span data-ttu-id="c621e-389">Lossless</span><span class="sxs-lookup"><span data-stu-id="c621e-389">Lossless</span></span>

<span data-ttu-id="c621e-390">Abilita la compressione delle perdite.</span><span class="sxs-lookup"><span data-stu-id="c621e-390">Enables losses compression.</span></span>



| <span data-ttu-id="c621e-391">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c621e-391">Data type</span></span>         | <span data-ttu-id="c621e-392">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c621e-392">VARTYPE</span></span>      | <span data-ttu-id="c621e-393">Predefinito</span><span class="sxs-lookup"><span data-stu-id="c621e-393">Default</span></span>        |
|-------------------|--------------|----------------|
| <span data-ttu-id="c621e-394">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="c621e-394">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="c621e-395">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="c621e-395">**VT\_BOOL**</span></span> | <span data-ttu-id="c621e-396">VARIANT \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="c621e-396">VARIANT\_FALSE</span></span> |



 

<span data-ttu-id="c621e-397">Se il valore è **VARIANT \_ TRUE,** il codificatore usa la compressione senza perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="c621e-397">If the value is **VARIANT\_TRUE**, the encoder uses lossless compression.</span></span> <span data-ttu-id="c621e-398">Se impostata **su VARIANT \_ TRUE,** questa proprietà esegue l'override [della proprietà ImageQuality.](#imagequality)</span><span class="sxs-lookup"><span data-stu-id="c621e-398">When set to **VARIANT\_TRUE**, this property overrides the [ImageQuality](#imagequality) property.</span></span>

### <a name="overlap"></a><span data-ttu-id="c621e-399">Overlap</span><span class="sxs-lookup"><span data-stu-id="c621e-399">Overlap</span></span>

<span data-ttu-id="c621e-400">Imposta il livello di filtro di sovrapposizione.</span><span class="sxs-lookup"><span data-stu-id="c621e-400">Sets the level of overlap filtering.</span></span> <span data-ttu-id="c621e-401">Con il filtro di sovrapposizione, i coefficienti di trasformazione vengono applicati attraverso i limiti dei blocchi e dei macroblock.</span><span class="sxs-lookup"><span data-stu-id="c621e-401">With overlap filtering, transform coefficients are applied across block and macroblock boundaries.</span></span> <span data-ttu-id="c621e-402">Ciò può ridurre gli artefatti di blocco.</span><span class="sxs-lookup"><span data-stu-id="c621e-402">This can reduce blocking artifacts.</span></span>



| <span data-ttu-id="c621e-403">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c621e-403">Data type</span></span> | <span data-ttu-id="c621e-404">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c621e-404">VARTYPE</span></span>     | <span data-ttu-id="c621e-405">Intervallo</span><span class="sxs-lookup"><span data-stu-id="c621e-405">Range</span></span> | <span data-ttu-id="c621e-406">Predefinito</span><span class="sxs-lookup"><span data-stu-id="c621e-406">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="c621e-407">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="c621e-407">**UCHAR**</span></span> | <span data-ttu-id="c621e-408">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="c621e-408">**VT\_UI1**</span></span> | <span data-ttu-id="c621e-409">0–4</span><span class="sxs-lookup"><span data-stu-id="c621e-409">0–4</span></span>   | <span data-ttu-id="c621e-410">1</span><span class="sxs-lookup"><span data-stu-id="c621e-410">1</span></span>       |



 



| <span data-ttu-id="c621e-411">Valore</span><span class="sxs-lookup"><span data-stu-id="c621e-411">Value</span></span> | <span data-ttu-id="c621e-412">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c621e-412">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="c621e-413">0</span><span class="sxs-lookup"><span data-stu-id="c621e-413">0</span></span>     | <span data-ttu-id="c621e-414">Nessuna sovrapposizione.</span><span class="sxs-lookup"><span data-stu-id="c621e-414">No overlap.</span></span>                                   |
| <span data-ttu-id="c621e-415">1</span><span class="sxs-lookup"><span data-stu-id="c621e-415">1</span></span>     | <span data-ttu-id="c621e-416">Un livello di sovrapposizione, soft-tiling.</span><span class="sxs-lookup"><span data-stu-id="c621e-416">One level of overlap, soft tiling.</span></span> <span data-ttu-id="c621e-417">(impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="c621e-417">(Default.)</span></span> |
| <span data-ttu-id="c621e-418">2</span><span class="sxs-lookup"><span data-stu-id="c621e-418">2</span></span>     | <span data-ttu-id="c621e-419">Due livelli di sovrapposizione, soft-tiling.</span><span class="sxs-lookup"><span data-stu-id="c621e-419">Two levels of overlap, soft tiling.</span></span>           |
| <span data-ttu-id="c621e-420">3</span><span class="sxs-lookup"><span data-stu-id="c621e-420">3</span></span>     | <span data-ttu-id="c621e-421">Un livello di sovrapposizione, tinte rigide</span><span class="sxs-lookup"><span data-stu-id="c621e-421">One level of overlap, hard tiling</span></span>             |
| <span data-ttu-id="c621e-422">4</span><span class="sxs-lookup"><span data-stu-id="c621e-422">4</span></span>     | <span data-ttu-id="c621e-423">Due livelli di sovrapposizione, hard-tiling.</span><span class="sxs-lookup"><span data-stu-id="c621e-423">Two levels of overlap, hard tiling.</span></span>           |



 

<span data-ttu-id="c621e-424">Definizioni:</span><span class="sxs-lookup"><span data-stu-id="c621e-424">Definitions:</span></span>

-   <span data-ttu-id="c621e-425">Un livello di sovrapposizione: i valori codificati dei blocchi 4x4 vengono modificati in base ai blocchi adiacenti.</span><span class="sxs-lookup"><span data-stu-id="c621e-425">One level of overlap: The encoded values of 4x4 blocks are modified based on neighboring blocks.</span></span>
-   <span data-ttu-id="c621e-426">Due livelli di sovrapposizione: viene applicato il primo livello di sovrapposizione.</span><span class="sxs-lookup"><span data-stu-id="c621e-426">Two levels of overlap: The first level of overlap is applied.</span></span> <span data-ttu-id="c621e-427">Inoltre, i valori codificati dei macroblock 16x16 vengono modificati in base ai macroblock adiacenti.</span><span class="sxs-lookup"><span data-stu-id="c621e-427">In addition, the encoded values of 16x16 macroblocks are modified based on the neighboring macroblocks.</span></span>
-   <span data-ttu-id="c621e-428">Affiancamento a soffio: il filtro delle sovrapposizioni viene applicato tra i limiti del riquadro.</span><span class="sxs-lookup"><span data-stu-id="c621e-428">Soft tiling: Overlap filtering is applied across tile boundaries.</span></span>
-   <span data-ttu-id="c621e-429">Hard-tiling: il filtro di sovrapposizione non viene applicato tra i limiti del riquadro.</span><span class="sxs-lookup"><span data-stu-id="c621e-429">Hard tiling: Overlap filtering is not applied across tile boundaries.</span></span> <span data-ttu-id="c621e-430">I riquadri rigidi possono introdurre alcuni artefatti visivi lungo i limiti dei riquadri.</span><span class="sxs-lookup"><span data-stu-id="c621e-430">Hard tiles can introduce some visual artifacts along tile boundaries.</span></span>

<span data-ttu-id="c621e-431">Se si imposta questa proprietà, impostare anche [UseCodecOptions](#usecodecoptions) su **VARIANT \_ TRUE.**</span><span class="sxs-lookup"><span data-stu-id="c621e-431">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="progressivemode"></a><span data-ttu-id="c621e-432">Modalità progressiva</span><span class="sxs-lookup"><span data-stu-id="c621e-432">ProgressiveMode</span></span>

<span data-ttu-id="c621e-433">Abilita o disabilita la codifica progressiva.</span><span class="sxs-lookup"><span data-stu-id="c621e-433">Enables or disables progressive encoding.</span></span>



| <span data-ttu-id="c621e-434">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c621e-434">Data type</span></span>         | <span data-ttu-id="c621e-435">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c621e-435">VARTYPE</span></span>      | <span data-ttu-id="c621e-436">Predefinito</span><span class="sxs-lookup"><span data-stu-id="c621e-436">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="c621e-437">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="c621e-437">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="c621e-438">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="c621e-438">**VT\_BOOL**</span></span> | <span data-ttu-id="c621e-439">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="c621e-439">**VARIANT\_FALSE**</span></span> |



 



| <span data-ttu-id="c621e-440">Valore</span><span class="sxs-lookup"><span data-stu-id="c621e-440">Value</span></span>              | <span data-ttu-id="c621e-441">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c621e-441">Description</span></span>                |
|--------------------|----------------------------|
| <span data-ttu-id="c621e-442">**VARIANT \_ TRUE**</span><span class="sxs-lookup"><span data-stu-id="c621e-442">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="c621e-443">Modalità sequenziale (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="c621e-443">Sequential mode (default).</span></span> |
| <span data-ttu-id="c621e-444">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="c621e-444">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="c621e-445">Modalità progressiva.</span><span class="sxs-lookup"><span data-stu-id="c621e-445">Progressive mode.</span></span>          |



 

### <a name="quality"></a><span data-ttu-id="c621e-446">Qualità</span><span class="sxs-lookup"><span data-stu-id="c621e-446">Quality</span></span>

<span data-ttu-id="c621e-447">Imposta la qualità di compressione.</span><span class="sxs-lookup"><span data-stu-id="c621e-447">Sets the compression quality.</span></span>



| <span data-ttu-id="c621e-448">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c621e-448">Data type</span></span> | <span data-ttu-id="c621e-449">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c621e-449">VARTYPE</span></span>     | <span data-ttu-id="c621e-450">Intervallo</span><span class="sxs-lookup"><span data-stu-id="c621e-450">Range</span></span> | <span data-ttu-id="c621e-451">Predefinito</span><span class="sxs-lookup"><span data-stu-id="c621e-451">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="c621e-452">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="c621e-452">**UCHAR**</span></span> | <span data-ttu-id="c621e-453">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="c621e-453">**VT\_UI1**</span></span> | <span data-ttu-id="c621e-454">1–255</span><span class="sxs-lookup"><span data-stu-id="c621e-454">1–255</span></span> | <span data-ttu-id="c621e-455">1</span><span class="sxs-lookup"><span data-stu-id="c621e-455">1</span></span>       |



 

<span data-ttu-id="c621e-456">Il valore 1 indica la modalità senza perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="c621e-456">The value 1 indicates lossless mode.</span></span> <span data-ttu-id="c621e-457">L'aumento dei valori comporta rapporti di compressione più elevati e una qualità dell'immagine inferiore.</span><span class="sxs-lookup"><span data-stu-id="c621e-457">Increasing values result in higher compression ratios and lower image quality.</span></span>

<span data-ttu-id="c621e-458">Se si imposta questa proprietà, impostare anche [UseCodecOptions](#usecodecoptions) su **VARIANT \_ TRUE.**</span><span class="sxs-lookup"><span data-stu-id="c621e-458">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="streamonly"></a><span data-ttu-id="c621e-459">StreamOnly</span><span class="sxs-lookup"><span data-stu-id="c621e-459">StreamOnly</span></span>

<span data-ttu-id="c621e-460">Abilita o disabilita la modalità solo flusso.</span><span class="sxs-lookup"><span data-stu-id="c621e-460">Enables or disables stream-only mode.</span></span>



| <span data-ttu-id="c621e-461">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c621e-461">Data type</span></span>         | <span data-ttu-id="c621e-462">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c621e-462">VARTYPE</span></span>      | <span data-ttu-id="c621e-463">Predefinito</span><span class="sxs-lookup"><span data-stu-id="c621e-463">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="c621e-464">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="c621e-464">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="c621e-465">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="c621e-465">**VT\_BOOL**</span></span> | <span data-ttu-id="c621e-466">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="c621e-466">**VARIANT\_FALSE**</span></span> |



 



| <span data-ttu-id="c621e-467">Valore</span><span class="sxs-lookup"><span data-stu-id="c621e-467">Value</span></span>              | <span data-ttu-id="c621e-468">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c621e-468">Description</span></span>                                                            |
|--------------------|------------------------------------------------------------------------|
| <span data-ttu-id="c621e-469">**VARIANT \_ TRUE**</span><span class="sxs-lookup"><span data-stu-id="c621e-469">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="c621e-470">Il codificatore restituisce il flusso di immagini non elaborato senza metadati.</span><span class="sxs-lookup"><span data-stu-id="c621e-470">The encoder outputs the raw image stream without metadata.</span></span>             |
| <span data-ttu-id="c621e-471">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="c621e-471">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="c621e-472">Il codificatore restituisce il formato del contenitore (flusso di immagini e metadati).</span><span class="sxs-lookup"><span data-stu-id="c621e-472">The encoder outputs the container format (image stream plus metadata).</span></span> |



 

### <a name="subsampling"></a><span data-ttu-id="c621e-473">Sottocampionamento</span><span class="sxs-lookup"><span data-stu-id="c621e-473">Subsampling</span></span>

<span data-ttu-id="c621e-474">Imposta il sottocampionamento della chroma.</span><span class="sxs-lookup"><span data-stu-id="c621e-474">Sets the chroma subsampling.</span></span> <span data-ttu-id="c621e-475">Questa proprietà si applica solo alle immagini RGB.</span><span class="sxs-lookup"><span data-stu-id="c621e-475">This property applies only to RGB images.</span></span>



| <span data-ttu-id="c621e-476">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c621e-476">Data type</span></span> | <span data-ttu-id="c621e-477">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c621e-477">VARTYPE</span></span>     | <span data-ttu-id="c621e-478">Intervallo</span><span class="sxs-lookup"><span data-stu-id="c621e-478">Range</span></span> | <span data-ttu-id="c621e-479">Predefinito</span><span class="sxs-lookup"><span data-stu-id="c621e-479">Default</span></span>                                                  |
|-----------|-------------|-------|----------------------------------------------------------|
| <span data-ttu-id="c621e-480">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="c621e-480">**UCHAR**</span></span> | <span data-ttu-id="c621e-481">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="c621e-481">**VT\_UI1**</span></span> | <span data-ttu-id="c621e-482">0–3</span><span class="sxs-lookup"><span data-stu-id="c621e-482">0–3</span></span>   | <span data-ttu-id="c621e-483">3 se [ImageQuality](#imagequality) > 0.8; in caso contrario, 1</span><span class="sxs-lookup"><span data-stu-id="c621e-483">3 if [ImageQuality](#imagequality) > 0.8; otherwise 1</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c621e-484">Valore</span><span class="sxs-lookup"><span data-stu-id="c621e-484">Value</span></span></th>
<th><span data-ttu-id="c621e-485">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c621e-485">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c621e-486">3</span><span class="sxs-lookup"><span data-stu-id="c621e-486">3</span></span></td>
<td><span data-ttu-id="c621e-487">Codifica 4:4:4.</span><span class="sxs-lookup"><span data-stu-id="c621e-487">4:4:4 encoding.</span></span> <span data-ttu-id="c621e-488">Mantiene la risoluzione chroma completa.</span><span class="sxs-lookup"><span data-stu-id="c621e-488">Preserves full chroma resolution.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c621e-489">2</span><span class="sxs-lookup"><span data-stu-id="c621e-489">2</span></span></td>
<td><span data-ttu-id="c621e-490">Codifica 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="c621e-490">4:2:2 encoding.</span></span> <span data-ttu-id="c621e-491">La risoluzione della luminazione è di 1/2.</span><span class="sxs-lookup"><span data-stu-id="c621e-491">Chroma resolution is ½ of luminance resolution.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c621e-492">1</span><span class="sxs-lookup"><span data-stu-id="c621e-492">1</span></span></td>
<td><span data-ttu-id="c621e-493">Codifica 4:2:0.</span><span class="sxs-lookup"><span data-stu-id="c621e-493">4:2:0 encoding.</span></span> <span data-ttu-id="c621e-494">La risoluzione della luminazione è di 1/4.</span><span class="sxs-lookup"><span data-stu-id="c621e-494">Chroma resolution is ¼ of luminance resolution.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c621e-495">0</span><span class="sxs-lookup"><span data-stu-id="c621e-495">0</span></span></td>
<td><span data-ttu-id="c621e-496">Codifica 4:0:0.</span><span class="sxs-lookup"><span data-stu-id="c621e-496">4:0:0 encoding.</span></span> <span data-ttu-id="c621e-497">Rimuove tutti i valori chroma e mantiene solo la luminance.</span><span class="sxs-lookup"><span data-stu-id="c621e-497">Discards all chroma values and preserves luminance only.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c621e-498">Questa modalità non è consigliata perché il codec usa una definizione di luminance leggermente modificata per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="c621e-498">This mode is not recommended, because the codec uses a slightly modified definition of luminance to improve performance.</span></span> <span data-ttu-id="c621e-499">È invece meglio convertire l'immagine in monocromatica prima della codifica.</span><span class="sxs-lookup"><span data-stu-id="c621e-499">Instead, it is better to convert the image to monochrome before encoding.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c621e-500">4:2:2 e 4:2:0 conservano i dettagli della luminazione a scapito dei dettagli del colore.</span><span class="sxs-lookup"><span data-stu-id="c621e-500">4:2:2 and 4:2:0 preserve luminance detail at the expense of color detail.</span></span>

<span data-ttu-id="c621e-501">Se si imposta questa proprietà, impostare anche [UseCodecOptions](#usecodecoptions) su **VARIANT \_ TRUE.**</span><span class="sxs-lookup"><span data-stu-id="c621e-501">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="usecodecoptions"></a><span data-ttu-id="c621e-502">UseCodecOptions</span><span class="sxs-lookup"><span data-stu-id="c621e-502">UseCodecOptions</span></span>

<span data-ttu-id="c621e-503">Specifica se usare le [proprietà Quality](#image-quality-settings), [Overlap](#overlap)e [Subsampling](#subsampling) anziché la [proprietà ImageQuality](#imagequality) generica.</span><span class="sxs-lookup"><span data-stu-id="c621e-503">Specifies whether to use the [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties instead of the generic [ImageQuality](#imagequality) property.</span></span>



| <span data-ttu-id="c621e-504">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c621e-504">Data type</span></span>         | <span data-ttu-id="c621e-505">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c621e-505">VARTYPE</span></span>      | <span data-ttu-id="c621e-506">Predefinito</span><span class="sxs-lookup"><span data-stu-id="c621e-506">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="c621e-507">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="c621e-507">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="c621e-508">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="c621e-508">**VT\_BOOL**</span></span> | <span data-ttu-id="c621e-509">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="c621e-509">**VARIANT\_FALSE**</span></span> |



 

### <a name="verticaltileslices"></a><span data-ttu-id="c621e-510">VerticalTileSlices</span><span class="sxs-lookup"><span data-stu-id="c621e-510">VerticalTileSlices</span></span>

<span data-ttu-id="c621e-511">Imposta il numero di riquadri orizzontali.</span><span class="sxs-lookup"><span data-stu-id="c621e-511">Sets the number of horizontal tiles.</span></span>



| <span data-ttu-id="c621e-512">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c621e-512">Data type</span></span>  | <span data-ttu-id="c621e-513">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c621e-513">VARTYPE</span></span>     | <span data-ttu-id="c621e-514">Intervallo</span><span class="sxs-lookup"><span data-stu-id="c621e-514">Range</span></span>  | <span data-ttu-id="c621e-515">Predefinito</span><span class="sxs-lookup"><span data-stu-id="c621e-515">Default</span></span>                       |
|------------|-------------|--------|-------------------------------|
| <span data-ttu-id="c621e-516">**Ushort**</span><span class="sxs-lookup"><span data-stu-id="c621e-516">**USHORT**</span></span> | <span data-ttu-id="c621e-517">**Interfaccia utente \_ VT 2**</span><span class="sxs-lookup"><span data-stu-id="c621e-517">**VT\_UI2**</span></span> | <span data-ttu-id="c621e-518">0–4095</span><span class="sxs-lookup"><span data-stu-id="c621e-518">0–4095</span></span> | <span data-ttu-id="c621e-519">(altezza immagine - 1) >> 8</span><span class="sxs-lookup"><span data-stu-id="c621e-519">(image height – 1) >> 8</span></span> |



 

<span data-ttu-id="c621e-520">Il valore è il numero di suddivisioni verticali. cio, il numero di riquadri verticali - 1.</span><span class="sxs-lookup"><span data-stu-id="c621e-520">The value is the number of vertical subdivisions; that is, the number of vertical tiles – 1.</span></span>

## <a name="supported-color-formats"></a><span data-ttu-id="c621e-521">Formati di colore supportati</span><span class="sxs-lookup"><span data-stu-id="c621e-521">Supported Color Formats</span></span>

<span data-ttu-id="c621e-522">Per altre informazioni su questi formati, vedere [Native Pixel Formats](-wic-codec-native-pixel-formats.md).</span><span class="sxs-lookup"><span data-stu-id="c621e-522">For more information about these formats, see [Native Pixel Formats](-wic-codec-native-pixel-formats.md).</span></span>

-   <span data-ttu-id="c621e-523">**Formati RGB integer**</span><span class="sxs-lookup"><span data-stu-id="c621e-523">**Integer RGB formats**</span></span>
    -   <span data-ttu-id="c621e-524">GUID \_ WICPixelFormat24bppRGB</span><span class="sxs-lookup"><span data-stu-id="c621e-524">GUID\_WICPixelFormat24bppRGB</span></span>
    -   <span data-ttu-id="c621e-525">GUID \_ WICPixelFormat24bppBGR</span><span class="sxs-lookup"><span data-stu-id="c621e-525">GUID\_WICPixelFormat24bppBGR</span></span>
    -   <span data-ttu-id="c621e-526">GUID \_ WICPixelFormat32bppBGR</span><span class="sxs-lookup"><span data-stu-id="c621e-526">GUID\_WICPixelFormat32bppBGR</span></span>
    -   <span data-ttu-id="c621e-527">GUID \_ WICPixelFormat48bppRGB</span><span class="sxs-lookup"><span data-stu-id="c621e-527">GUID\_WICPixelFormat48bppRGB</span></span>
    -   <span data-ttu-id="c621e-528">GUID \_ WICPixelFormat32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="c621e-528">GUID\_WICPixelFormat32bppBGRA</span></span>
    -   <span data-ttu-id="c621e-529">GUID \_ WICPixelFormat64bppRGBA</span><span class="sxs-lookup"><span data-stu-id="c621e-529">GUID\_WICPixelFormat64bppRGBA</span></span>
    -   <span data-ttu-id="c621e-530">GUID \_ WICPixelFormat32bppPBGRA</span><span class="sxs-lookup"><span data-stu-id="c621e-530">GUID\_WICPixelFormat32bppPBGRA</span></span>
    -   <span data-ttu-id="c621e-531">GUID \_ WICPixelFormat64bppPRGBA</span><span class="sxs-lookup"><span data-stu-id="c621e-531">GUID\_WICPixelFormat64bppPRGBA</span></span>
-   <span data-ttu-id="c621e-532">**Formati RGB a virgola fissa**</span><span class="sxs-lookup"><span data-stu-id="c621e-532">**Fixed-point RGB formats**</span></span>
    -   <span data-ttu-id="c621e-533">GUID \_ WICPixelFormat48bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="c621e-533">GUID\_WICPixelFormat48bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="c621e-534">GUID \_ WICPixelFormat64bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="c621e-534">GUID\_WICPixelFormat64bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="c621e-535">GUID \_ WICPixelFormat96bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="c621e-535">GUID\_WICPixelFormat96bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="c621e-536">GUID \_ WICPixelFormat128bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="c621e-536">GUID\_WICPixelFormat128bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="c621e-537">GUID \_ WICPixelFormat128bppRGBAFixedPoint</span><span class="sxs-lookup"><span data-stu-id="c621e-537">GUID\_WICPixelFormat128bppRGBAFixedPoint</span></span>
-   <span data-ttu-id="c621e-538">**Formati RGB a virgola mobile**</span><span class="sxs-lookup"><span data-stu-id="c621e-538">**Floating-point RGB formats**</span></span>
    -   <span data-ttu-id="c621e-539">GUID \_ WICPixelFormat48bppRGBHalf</span><span class="sxs-lookup"><span data-stu-id="c621e-539">GUID\_WICPixelFormat48bppRGBHalf</span></span>
    -   <span data-ttu-id="c621e-540">GUID \_ WICPixelFormat64bppRGBHalf</span><span class="sxs-lookup"><span data-stu-id="c621e-540">GUID\_WICPixelFormat64bppRGBHalf</span></span>
    -   <span data-ttu-id="c621e-541">GUID \_ WICPixelFormat128bppRGBFloat</span><span class="sxs-lookup"><span data-stu-id="c621e-541">GUID\_WICPixelFormat128bppRGBFloat</span></span>
    -   <span data-ttu-id="c621e-542">GUID \_ WICPixelFormat64bppRGBAFixedPoint</span><span class="sxs-lookup"><span data-stu-id="c621e-542">GUID\_WICPixelFormat64bppRGBAFixedPoint</span></span>
    -   <span data-ttu-id="c621e-543">GUID \_ WICPixelFormat64bppRGBAHalf</span><span class="sxs-lookup"><span data-stu-id="c621e-543">GUID\_WICPixelFormat64bppRGBAHalf</span></span>
    -   <span data-ttu-id="c621e-544">GUID \_ WICPixelFormat128bppRGBAFloat</span><span class="sxs-lookup"><span data-stu-id="c621e-544">GUID\_WICPixelFormat128bppRGBAFloat</span></span>
    -   <span data-ttu-id="c621e-545">GUID \_ WICPixelFormat128bppPRGBAFloat</span><span class="sxs-lookup"><span data-stu-id="c621e-545">GUID\_WICPixelFormat128bppPRGBAFloat</span></span>
-   <span data-ttu-id="c621e-546">**Formati in scala di grigi**</span><span class="sxs-lookup"><span data-stu-id="c621e-546">**Grayscale formats**</span></span>
    -   <span data-ttu-id="c621e-547">GUID \_ WICPixelFormat8bppGray</span><span class="sxs-lookup"><span data-stu-id="c621e-547">GUID\_WICPixelFormat8bppGray</span></span>
    -   <span data-ttu-id="c621e-548">GUID \_ WICPixelFormat16bppGray</span><span class="sxs-lookup"><span data-stu-id="c621e-548">GUID\_WICPixelFormat16bppGray</span></span>
    -   <span data-ttu-id="c621e-549">GUID \_ WICPixelFormat16bppGrayFixedPoint</span><span class="sxs-lookup"><span data-stu-id="c621e-549">GUID\_WICPixelFormat16bppGrayFixedPoint</span></span>
    -   <span data-ttu-id="c621e-550">GUID \_ WICPixelFormat16bppGrayHalf</span><span class="sxs-lookup"><span data-stu-id="c621e-550">GUID\_WICPixelFormat16bppGrayHalf</span></span>
    -   <span data-ttu-id="c621e-551">GUID \_ WICPixelFormat32bppGrayFixedPoint</span><span class="sxs-lookup"><span data-stu-id="c621e-551">GUID\_WICPixelFormat32bppGrayFixedPoint</span></span>
    -   <span data-ttu-id="c621e-552">GUID \_ WICPixelFormat32bppGrayFloat</span><span class="sxs-lookup"><span data-stu-id="c621e-552">GUID\_WICPixelFormat32bppGrayFloat</span></span>
-   <span data-ttu-id="c621e-553">**Formati imballati**</span><span class="sxs-lookup"><span data-stu-id="c621e-553">**Packed formats**</span></span>
    -   <span data-ttu-id="c621e-554">GUID \_ WICPixelFormat16bppBGR555</span><span class="sxs-lookup"><span data-stu-id="c621e-554">GUID\_WICPixelFormat16bppBGR555</span></span>
    -   <span data-ttu-id="c621e-555">GUID \_ WICPixelFormat16bppBGR565</span><span class="sxs-lookup"><span data-stu-id="c621e-555">GUID\_WICPixelFormat16bppBGR565</span></span>
    -   <span data-ttu-id="c621e-556">GUID \_ WICPixelFormat32bppBGR101010</span><span class="sxs-lookup"><span data-stu-id="c621e-556">GUID\_WICPixelFormat32bppBGR101010</span></span>
    -   <span data-ttu-id="c621e-557">GUID \_ WICPixelFormat32bppRGBE</span><span class="sxs-lookup"><span data-stu-id="c621e-557">GUID\_WICPixelFormat32bppRGBE</span></span>
-   <span data-ttu-id="c621e-558">**Formati CMYK**</span><span class="sxs-lookup"><span data-stu-id="c621e-558">**CMYK formats**</span></span>
    -   <span data-ttu-id="c621e-559">GUID \_ WICPixelFormat40bppCMYKAlpha</span><span class="sxs-lookup"><span data-stu-id="c621e-559">GUID\_WICPixelFormat40bppCMYKAlpha</span></span>
    -   <span data-ttu-id="c621e-560">GUID \_ WICPixelFormat64bppCMYK</span><span class="sxs-lookup"><span data-stu-id="c621e-560">GUID\_WICPixelFormat64bppCMYK</span></span>
    -   <span data-ttu-id="c621e-561">GUID \_ WICPixelFormat80bppCMYKAlpha</span><span class="sxs-lookup"><span data-stu-id="c621e-561">GUID\_WICPixelFormat80bppCMYKAlpha</span></span>
-   <span data-ttu-id="c621e-562">**Formati a N canali**</span><span class="sxs-lookup"><span data-stu-id="c621e-562">**N-channel formats**</span></span>
    -   <span data-ttu-id="c621e-563">GUID \_ WICPixelFormat32bpp4Channels</span><span class="sxs-lookup"><span data-stu-id="c621e-563">GUID\_WICPixelFormat32bpp4Channels</span></span>
    -   <span data-ttu-id="c621e-564">GUID \_ WICPixelFormat40bpp5Channels</span><span class="sxs-lookup"><span data-stu-id="c621e-564">GUID\_WICPixelFormat40bpp5Channels</span></span>
    -   <span data-ttu-id="c621e-565">GUID \_ WICPixelFormat48bpp6Channels</span><span class="sxs-lookup"><span data-stu-id="c621e-565">GUID\_WICPixelFormat48bpp6Channels</span></span>
    -   <span data-ttu-id="c621e-566">GUID \_ WICPixelFormat56bpp7Channels</span><span class="sxs-lookup"><span data-stu-id="c621e-566">GUID\_WICPixelFormat56bpp7Channels</span></span>
    -   <span data-ttu-id="c621e-567">GUID \_ WICPixelFormat64bpp8Channels</span><span class="sxs-lookup"><span data-stu-id="c621e-567">GUID\_WICPixelFormat64bpp8Channels</span></span>
    -   <span data-ttu-id="c621e-568">GUID \_ WICPixelFormat32bpp3ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="c621e-568">GUID\_WICPixelFormat32bpp3ChannelsAlpha</span></span>
    -   <span data-ttu-id="c621e-569">GUID \_ WICPixelFormat40bpp4ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="c621e-569">GUID\_WICPixelFormat40bpp4ChannelsAlpha</span></span>
    -   <span data-ttu-id="c621e-570">GUID \_ WICPixelFormat48bpp5ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="c621e-570">GUID\_WICPixelFormat48bpp5ChannelsAlpha</span></span>
    -   <span data-ttu-id="c621e-571">GUID \_ WICPixelFormat56bpp6ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="c621e-571">GUID\_WICPixelFormat56bpp6ChannelsAlpha</span></span>
    -   <span data-ttu-id="c621e-572">GUID \_ WICPixelFormat64bpp7ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="c621e-572">GUID\_WICPixelFormat64bpp7ChannelsAlpha</span></span>
    -   <span data-ttu-id="c621e-573">GUID \_ WICPixelFormat72bpp8ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="c621e-573">GUID\_WICPixelFormat72bpp8ChannelsAlpha</span></span>
    -   <span data-ttu-id="c621e-574">GUID \_ WICPixelFormat48bpp3Channels</span><span class="sxs-lookup"><span data-stu-id="c621e-574">GUID\_WICPixelFormat48bpp3Channels</span></span>
    -   <span data-ttu-id="c621e-575">GUID \_ WICPixelFormat64bpp4Channels</span><span class="sxs-lookup"><span data-stu-id="c621e-575">GUID\_WICPixelFormat64bpp4Channels</span></span>
    -   <span data-ttu-id="c621e-576">GUID \_ WICPixelFormat80bpp5Channels</span><span class="sxs-lookup"><span data-stu-id="c621e-576">GUID\_WICPixelFormat80bpp5Channels</span></span>
    -   <span data-ttu-id="c621e-577">GUID \_ WICPixelFormat96bpp6Channels</span><span class="sxs-lookup"><span data-stu-id="c621e-577">GUID\_WICPixelFormat96bpp6Channels</span></span>
    -   <span data-ttu-id="c621e-578">GUID \_ WICPixelFormat128bpp8Channels</span><span class="sxs-lookup"><span data-stu-id="c621e-578">GUID\_WICPixelFormat128bpp8Channels</span></span>
    -   <span data-ttu-id="c621e-579">GUID \_ WICPixelFormat64bpp3ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="c621e-579">GUID\_WICPixelFormat64bpp3ChannelsAlpha</span></span>
    -   <span data-ttu-id="c621e-580">GUID \_ WICPixelFormat80bpp4ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="c621e-580">GUID\_WICPixelFormat80bpp4ChannelsAlpha</span></span>
    -   <span data-ttu-id="c621e-581">GUID \_ WICPixelFormat96bpp5ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="c621e-581">GUID\_WICPixelFormat96bpp5ChannelsAlpha</span></span>
    -   <span data-ttu-id="c621e-582">GUID \_ WICPixelFormat112bpp6ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="c621e-582">GUID\_WICPixelFormat112bpp6ChannelsAlpha</span></span>
    -   <span data-ttu-id="c621e-583">GUID \_ WICPixelFormat128bpp7ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="c621e-583">GUID\_WICPixelFormat128bpp7ChannelsAlpha</span></span>
    -   <span data-ttu-id="c621e-584">GUID \_ WICPixelFormat1444bpp8ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="c621e-584">GUID\_WICPixelFormat144bpp8ChannelsAlpha</span></span>

 

 
