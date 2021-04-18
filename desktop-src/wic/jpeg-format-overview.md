---
description: In questo argomento vengono fornite informazioni sul codec JPEG nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: 9DCBCE9B-965B-4C18-992C-EFFFF32FCE5E
title: Panoramica sul formato JPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb953d1d6a02e47b41d1b7cf872f3381cd640151
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312389"
---
# <a name="jpeg-format-overview"></a><span data-ttu-id="d2d7d-103">Panoramica sul formato JPEG</span><span class="sxs-lookup"><span data-stu-id="d2d7d-103">JPEG Format Overview</span></span>

<span data-ttu-id="d2d7d-104">In questo argomento vengono fornite informazioni sul codec JPEG nativo disponibile tramite Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="d2d7d-104">This topic provides information about the native JPEG codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="d2d7d-105">Identità codec</span><span class="sxs-lookup"><span data-stu-id="d2d7d-105">Codec Identity</span></span>

<span data-ttu-id="d2d7d-106">Nella tabella seguente vengono fornite informazioni di identificazione del codec.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-106">The following table provides codec identification information.</span></span>



|                        |                                         |
|------------------------|-----------------------------------------|
| <span data-ttu-id="d2d7d-107">Nome/i formale/i</span><span class="sxs-lookup"><span data-stu-id="d2d7d-107">Formal Name(s)</span></span>         | <span data-ttu-id="d2d7d-108">Joint Photographic Experts Group (JPEG)</span><span class="sxs-lookup"><span data-stu-id="d2d7d-108">Joint Photographic Experts Group (JPEG)</span></span> |
| <span data-ttu-id="d2d7d-109">Estensioni del nome di file</span><span class="sxs-lookup"><span data-stu-id="d2d7d-109">File Name Extension(s)</span></span> | <span data-ttu-id="d2d7d-110">JPE, JPEG, jpg</span><span class="sxs-lookup"><span data-stu-id="d2d7d-110">jpe, jpeg, jpg</span></span>                          |
| <span data-ttu-id="d2d7d-111">tipo MIME</span><span class="sxs-lookup"><span data-stu-id="d2d7d-111">MIME type</span></span>              | <span data-ttu-id="d2d7d-112">image/jpeg, image/JPE, image/jpg</span><span class="sxs-lookup"><span data-stu-id="d2d7d-112">image/jpeg, image/jpe, image/jpg</span></span>        |
| <span data-ttu-id="d2d7d-113">Supporto delle specifiche</span><span class="sxs-lookup"><span data-stu-id="d2d7d-113">Specification Support</span></span>  | <span data-ttu-id="d2d7d-114">Specifica JFIF 1,02</span><span class="sxs-lookup"><span data-stu-id="d2d7d-114">JFIF Specification 1.02</span></span>                 |



 

<span data-ttu-id="d2d7d-115">Nella tabella seguente sono elencati i GUID utilizzati per identificare i componenti dei codec JPEG nativi.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-115">The following table lists the GUIDs used to identify the native JPEG codec components.</span></span>



| <span data-ttu-id="d2d7d-116">Componente</span><span class="sxs-lookup"><span data-stu-id="d2d7d-116">Component</span></span>        | <span data-ttu-id="d2d7d-117">Nome descrittivo</span><span class="sxs-lookup"><span data-stu-id="d2d7d-117">Friendly Name</span></span>             | <span data-ttu-id="d2d7d-118">GUID</span><span class="sxs-lookup"><span data-stu-id="d2d7d-118">GUID</span></span>                                |
|------------------|---------------------------|-------------------------------------|
| <span data-ttu-id="d2d7d-119">Formato contenitore</span><span class="sxs-lookup"><span data-stu-id="d2d7d-119">Container Format</span></span> | <span data-ttu-id="d2d7d-120">GUID \_ ContainerFormatJpeg</span><span class="sxs-lookup"><span data-stu-id="d2d7d-120">GUID\_ContainerFormatJpeg</span></span> | <span data-ttu-id="d2d7d-121">19e4a5aa-5662-4fc5-a0c01758028e1057</span><span class="sxs-lookup"><span data-stu-id="d2d7d-121">19e4a5aa-5662-4fc5-a0c01758028e1057</span></span> |
| <span data-ttu-id="d2d7d-122">Decodificatore</span><span class="sxs-lookup"><span data-stu-id="d2d7d-122">Decoder</span></span>          | <span data-ttu-id="d2d7d-123">\_WICJPEGDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="d2d7d-123">CLSID\_WICJpegDecoder</span></span>     | <span data-ttu-id="d2d7d-124">9456a480-e88b-43ea-9e730b2d9b71b1ca</span><span class="sxs-lookup"><span data-stu-id="d2d7d-124">9456a480-e88b-43ea-9e730b2d9b71b1ca</span></span> |
| <span data-ttu-id="d2d7d-125">Codificatore</span><span class="sxs-lookup"><span data-stu-id="d2d7d-125">Encoder</span></span>          | <span data-ttu-id="d2d7d-126">\_WICJPEGENCODER CLSID</span><span class="sxs-lookup"><span data-stu-id="d2d7d-126">CLSID\_WICJpegEncoder</span></span>     | <span data-ttu-id="d2d7d-127">1a34f5c1-4a5a-46dc-b6441f4567e7a676</span><span class="sxs-lookup"><span data-stu-id="d2d7d-127">1a34f5c1-4a5a-46dc-b6441f4567e7a676</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="d2d7d-128">Codifica</span><span class="sxs-lookup"><span data-stu-id="d2d7d-128">Encoding</span></span>

<span data-ttu-id="d2d7d-129">L'API di codifica WIC è progettata per essere indipendente dal codec e la codifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-129">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="d2d7d-130">Per ulteriori informazioni sulla codifica delle immagini tramite l'API WIC, vedere [Cenni preliminari sulla codifica](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="d2d7d-130">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="d2d7d-131">Opzioni del codificatore</span><span class="sxs-lookup"><span data-stu-id="d2d7d-131">Encoder Options</span></span>

<span data-ttu-id="d2d7d-132">I codec abilitati per WIC differiscono a livello di opzione di codifica.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-132">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="d2d7d-133">Le opzioni del codificatore riflettono le funzionalità di un codificatore di immagini e ogni codec nativo supporta un set di queste opzioni del codificatore.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-133">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="d2d7d-134">Le opzioni del codificatore possono essere opzioni supportate per WIC di base disponibili per tutti i codici abilitati per WIC (anche se non necessariamente supportati) o per le opzioni specifiche del codec progettate dal codec del formato di immagine.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-134">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="d2d7d-135">Per gestire queste opzioni di codifica durante il processo di codifica, WIC utilizza l'interfaccia [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d2d7d-135">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="d2d7d-136">Per ulteriori informazioni sull'utilizzo dell'interfaccia **IPropertyBag2** per la codifica WIC, vedere [Cenni preliminari sulla codifica](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="d2d7d-136">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="d2d7d-137">Il codec JPEG usa le opzioni WIC di base.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-137">The JPEG codec uses basic WIC options.</span></span> <span data-ttu-id="d2d7d-138">Nella tabella seguente sono elencate le opzioni del codificatore WIC supportate dal codec JPEG nativo.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-138">The following table lists the WIC encoder options supported by the native JPEG codec.</span></span>



| <span data-ttu-id="d2d7d-139">Nome della proprietà</span><span class="sxs-lookup"><span data-stu-id="d2d7d-139">Property Name</span></span>                                        | <span data-ttu-id="d2d7d-140">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="d2d7d-140">VARTYPE</span></span>           | <span data-ttu-id="d2d7d-141">Gamma valori</span><span class="sxs-lookup"><span data-stu-id="d2d7d-141">Value Range</span></span>                                                                       | <span data-ttu-id="d2d7d-142">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="d2d7d-142">Default Value</span></span>                                                                  |
|------------------------------------------------------|-------------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="d2d7d-143">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="d2d7d-143">ImageQuality</span></span>](#imagequality-option)                 | <span data-ttu-id="d2d7d-144">\_R4 VT</span><span class="sxs-lookup"><span data-stu-id="d2d7d-144">VT\_R4</span></span>            | <span data-ttu-id="d2d7d-145">0-1,0</span><span class="sxs-lookup"><span data-stu-id="d2d7d-145">0 - 1.0</span></span>                                                                           | <span data-ttu-id="d2d7d-146">0.9</span><span class="sxs-lookup"><span data-stu-id="d2d7d-146">0.9</span></span>                                                                            |
| [<span data-ttu-id="d2d7d-147">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="d2d7d-147">BitmapTransform</span></span>](#bitmaptransform-option)           | <span data-ttu-id="d2d7d-148">\_Ui1 VT</span><span class="sxs-lookup"><span data-stu-id="d2d7d-148">VT\_UI1</span></span>           | [<span data-ttu-id="d2d7d-149">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="d2d7d-149">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)         | [<span data-ttu-id="d2d7d-150">**WICBitmapTransformRotate0**</span><span class="sxs-lookup"><span data-stu-id="d2d7d-150">**WICBitmapTransformRotate0**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)      |
| [<span data-ttu-id="d2d7d-151">Luminanza</span><span class="sxs-lookup"><span data-stu-id="d2d7d-151">Luminance</span></span>](#luminance-option)                       | <span data-ttu-id="d2d7d-152">\_Array VT UI4/VT \_</span><span class="sxs-lookup"><span data-stu-id="d2d7d-152">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="d2d7d-153">64 voci (DCT)</span><span class="sxs-lookup"><span data-stu-id="d2d7d-153">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="d2d7d-154">Tabella luminanza predefinita.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-154">Default luminance table.</span></span>                                                       |
| [<span data-ttu-id="d2d7d-155">Chrominance</span><span class="sxs-lookup"><span data-stu-id="d2d7d-155">Chrominance</span></span>](#chrominance-option)                   | <span data-ttu-id="d2d7d-156">\_Array VT UI4/VT \_</span><span class="sxs-lookup"><span data-stu-id="d2d7d-156">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="d2d7d-157">64 voci (DCT)</span><span class="sxs-lookup"><span data-stu-id="d2d7d-157">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="d2d7d-158">Tabella cromatura predefinita.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-158">Default chrominance table.</span></span>                                                     |
| [<span data-ttu-id="d2d7d-159">JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="d2d7d-159">JpegYCrCbSubsampling</span></span>](#jpegycrcbsubsampling-option) | <span data-ttu-id="d2d7d-160">\_Ui1 VT</span><span class="sxs-lookup"><span data-stu-id="d2d7d-160">VT\_UI1</span></span>           | [<span data-ttu-id="d2d7d-161">**WICJpegYCrCbSubsamplingOption**</span><span class="sxs-lookup"><span data-stu-id="d2d7d-161">**WICJpegYCrCbSubsamplingOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | [<span data-ttu-id="d2d7d-162">**WICJpegYCrCbSubsampling420**</span><span class="sxs-lookup"><span data-stu-id="d2d7d-162">**WICJpegYCrCbSubsampling420**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) |
| [<span data-ttu-id="d2d7d-163">SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="d2d7d-163">SuppressApp0</span></span>](/windows)                       | <span data-ttu-id="d2d7d-164">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="d2d7d-164">VT\_BOOL</span></span>          | <span data-ttu-id="d2d7d-165">Valore **true** / **False**</span><span class="sxs-lookup"><span data-stu-id="d2d7d-165">**TRUE**/**FALSE**</span></span>                                                                | <span data-ttu-id="d2d7d-166">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="d2d7d-166">**FALSE**</span></span>                                                                      |



 

<span data-ttu-id="d2d7d-167">Se un'opzione del codificatore è presente nell'elenco di opzioni [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) che il codec non supporta, viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-167">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="imagequality-option"></a><span data-ttu-id="d2d7d-168">ImageQuality-opzione</span><span class="sxs-lookup"><span data-stu-id="d2d7d-168">ImageQuality Option</span></span>

<span data-ttu-id="d2d7d-169">Specifica la fedeltà dell'immagine desiderata.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-169">Specifies the desired image fidelity.</span></span> <span data-ttu-id="d2d7d-170">0,0 indica che la fedeltà più bassa possibile e 1,0 specifica la massima fedeltà.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-170">0.0 indicates the lowest possible fidelity and 1.0 specifies the highest fidelity.</span></span>

<span data-ttu-id="d2d7d-171">Il valore predefinito è 0,9.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-171">The default value is 0.9.</span></span>

### <a name="bitmaptransform-option"></a><span data-ttu-id="d2d7d-172">BitmapTransform-opzione</span><span class="sxs-lookup"><span data-stu-id="d2d7d-172">BitmapTransform Option</span></span>

<span data-ttu-id="d2d7d-173">Specifica la modalità di trasformazione dell'immagine durante la decodifica delle immagini.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-173">Specifies how the image is to be transformed during image decoding.</span></span> <span data-ttu-id="d2d7d-174">Questa opzione deve essere impostata su uno dei valori di enumerazione [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) .</span><span class="sxs-lookup"><span data-stu-id="d2d7d-174">This option must be set to one of the [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) enumeration values.</span></span>

<span data-ttu-id="d2d7d-175">Il valore predefinito è [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).</span><span class="sxs-lookup"><span data-stu-id="d2d7d-175">The default value is [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).</span></span>

### <a name="luminance-option"></a><span data-ttu-id="d2d7d-176">Opzione luminanza</span><span class="sxs-lookup"><span data-stu-id="d2d7d-176">Luminance Option</span></span>

<span data-ttu-id="d2d7d-177">Specifica la tabella del livello di luminosità in scala di grigi da usare per la codifica.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-177">Specifies the grayscale brightness level table to use for encoding.</span></span>

### <a name="chrominance-option"></a><span data-ttu-id="d2d7d-178">Cromatura-opzione</span><span class="sxs-lookup"><span data-stu-id="d2d7d-178">Chrominance Option</span></span>

<span data-ttu-id="d2d7d-179">Specifica la tabella cromatura da utilizzare per la codifica.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-179">Specifies the chrominance table to use for encoding.</span></span>

### <a name="jpegycrcbsubsampling-option"></a><span data-ttu-id="d2d7d-180">JpegYCrCbSubsampling-opzione</span><span class="sxs-lookup"><span data-stu-id="d2d7d-180">JpegYCrCbSubsampling Option</span></span>

<span data-ttu-id="d2d7d-181">Specifica il rapporto di sottocampionamento da utilizzare per la codifica YCrCb.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-181">Specifies the subsampling ratio to use for YCrCb encoding.</span></span>

<span data-ttu-id="d2d7d-182">Il valore predefinito è [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).</span><span class="sxs-lookup"><span data-stu-id="d2d7d-182">The default value is [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).</span></span>

### <a name="suppressapp0-option"></a><span data-ttu-id="d2d7d-183">SuppressApp0-opzione</span><span class="sxs-lookup"><span data-stu-id="d2d7d-183">SuppressApp0 Option</span></span>

<span data-ttu-id="d2d7d-184">Specifica se escludere la scrittura dei metadati APP0 durante la codifica dei dati dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-184">Specifies whether to suppress the write of App0 metadata while encoding the image data.</span></span>

<span data-ttu-id="d2d7d-185">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-185">The default value is **FALSE**.</span></span>

## <a name="decoding"></a><span data-ttu-id="d2d7d-186">Decodifica</span><span class="sxs-lookup"><span data-stu-id="d2d7d-186">Decoding</span></span>

<span data-ttu-id="d2d7d-187">L'API di decodifica WIC è progettata per essere indipendente dal codec e la decodifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-187">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="d2d7d-188">Per ulteriori informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="d2d7d-188">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="d2d7d-189">Per ulteriori informazioni sull'utilizzo di dati di immagine decodificati, vedere [Cenni preliminari sulle origini bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="d2d7d-189">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="d2d7d-190">Il codec JPEG nativo supporta anche [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) sulla decodifica dei frame aggiungendo opzioni avanzato per la decodifica di un flusso di immagini.</span><span class="sxs-lookup"><span data-stu-id="d2d7d-190">The native JPEG codec also supports the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) on frame decoding adding advaced options for decoding an image stream.</span></span> <span data-ttu-id="d2d7d-191">Per ulteriori informazioni su queste opzioni avanzate, vedere [Cenni preliminari sulle origini bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="d2d7d-191">For more information about these advanced options, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
