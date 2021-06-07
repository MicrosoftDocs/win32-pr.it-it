---
description: In questo argomento vengono fornite informazioni sul codec JPEG nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: 9DCBCE9B-965B-4C18-992C-EFFFF32FCE5E
title: Panoramica del formato JPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2acc7fcd71fc962d3321112d342f675b878188
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444192"
---
# <a name="jpeg-format-overview"></a><span data-ttu-id="2a6c2-103">Panoramica del formato JPEG</span><span class="sxs-lookup"><span data-stu-id="2a6c2-103">JPEG Format Overview</span></span>

<span data-ttu-id="2a6c2-104">In questo argomento vengono fornite informazioni sul codec JPEG nativo disponibile tramite Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="2a6c2-104">This topic provides information about the native JPEG codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="2a6c2-105">Codec Identity</span><span class="sxs-lookup"><span data-stu-id="2a6c2-105">Codec Identity</span></span>

<span data-ttu-id="2a6c2-106">Nella tabella seguente vengono fornite informazioni di identificazione del codec.</span><span class="sxs-lookup"><span data-stu-id="2a6c2-106">The following table provides codec identification information.</span></span>



|   <span data-ttu-id="2a6c2-107">Componente</span><span class="sxs-lookup"><span data-stu-id="2a6c2-107">Component</span></span>            | <span data-ttu-id="2a6c2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a6c2-108">Description</span></span>                             |
|------------------------|-----------------------------------------|
| <span data-ttu-id="2a6c2-109">Nomi formali</span><span class="sxs-lookup"><span data-stu-id="2a6c2-109">Formal Name(s)</span></span>         | <span data-ttu-id="2a6c2-110">Joint Photographic Experts Group (JPEG)</span><span class="sxs-lookup"><span data-stu-id="2a6c2-110">Joint Photographic Experts Group (JPEG)</span></span> |
| <span data-ttu-id="2a6c2-111">Estensioni di file</span><span class="sxs-lookup"><span data-stu-id="2a6c2-111">File Name Extension(s)</span></span> | <span data-ttu-id="2a6c2-112">jpe, jpeg, jpg</span><span class="sxs-lookup"><span data-stu-id="2a6c2-112">jpe, jpeg, jpg</span></span>                          |
| <span data-ttu-id="2a6c2-113">tipo MIME</span><span class="sxs-lookup"><span data-stu-id="2a6c2-113">MIME type</span></span>              | <span data-ttu-id="2a6c2-114">image/jpeg, image/jpe, image/jpg</span><span class="sxs-lookup"><span data-stu-id="2a6c2-114">image/jpeg, image/jpe, image/jpg</span></span>        |
| <span data-ttu-id="2a6c2-115">Supporto delle specifiche</span><span class="sxs-lookup"><span data-stu-id="2a6c2-115">Specification Support</span></span>  | <span data-ttu-id="2a6c2-116">Specifica JFIF 1.02</span><span class="sxs-lookup"><span data-stu-id="2a6c2-116">JFIF Specification 1.02</span></span>                 |



 

<span data-ttu-id="2a6c2-117">Nella tabella seguente sono elencati i GUID utilizzati per identificare i componenti nativi del codec JPEG.</span><span class="sxs-lookup"><span data-stu-id="2a6c2-117">The following table lists the GUIDs used to identify the native JPEG codec components.</span></span>



| <span data-ttu-id="2a6c2-118">Componente</span><span class="sxs-lookup"><span data-stu-id="2a6c2-118">Component</span></span>        | <span data-ttu-id="2a6c2-119">Nome descrittivo</span><span class="sxs-lookup"><span data-stu-id="2a6c2-119">Friendly Name</span></span>             | <span data-ttu-id="2a6c2-120">GUID</span><span class="sxs-lookup"><span data-stu-id="2a6c2-120">GUID</span></span>                                |
|------------------|---------------------------|-------------------------------------|
| <span data-ttu-id="2a6c2-121">Formato contenitore</span><span class="sxs-lookup"><span data-stu-id="2a6c2-121">Container Format</span></span> | <span data-ttu-id="2a6c2-122">GUID \_ ContainerFormatJpeg</span><span class="sxs-lookup"><span data-stu-id="2a6c2-122">GUID\_ContainerFormatJpeg</span></span> | <span data-ttu-id="2a6c2-123">19e4a5aa-5662-4fc5-a0c01758028e1057</span><span class="sxs-lookup"><span data-stu-id="2a6c2-123">19e4a5aa-5662-4fc5-a0c01758028e1057</span></span> |
| <span data-ttu-id="2a6c2-124">Decodificatore</span><span class="sxs-lookup"><span data-stu-id="2a6c2-124">Decoder</span></span>          | <span data-ttu-id="2a6c2-125">CLSID \_ WICJpegDecoder</span><span class="sxs-lookup"><span data-stu-id="2a6c2-125">CLSID\_WICJpegDecoder</span></span>     | <span data-ttu-id="2a6c2-126">9456a480-e88b-43ea-9e730b2d9b71b1ca</span><span class="sxs-lookup"><span data-stu-id="2a6c2-126">9456a480-e88b-43ea-9e730b2d9b71b1ca</span></span> |
| <span data-ttu-id="2a6c2-127">Codificatore</span><span class="sxs-lookup"><span data-stu-id="2a6c2-127">Encoder</span></span>          | <span data-ttu-id="2a6c2-128">CLSID \_ WICJpegEncoder</span><span class="sxs-lookup"><span data-stu-id="2a6c2-128">CLSID\_WICJpegEncoder</span></span>     | <span data-ttu-id="2a6c2-129">1a34f5c1-4a5a-46dc-b6441f4567e7a676</span><span class="sxs-lookup"><span data-stu-id="2a6c2-129">1a34f5c1-4a5a-46dc-b6441f4567e7a676</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="2a6c2-130">Codifica</span><span class="sxs-lookup"><span data-stu-id="2a6c2-130">Encoding</span></span>

<span data-ttu-id="2a6c2-131">L'API di codifica WIC è progettata per essere indipendente dal codec e la codifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="2a6c2-131">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="2a6c2-132">Per altre informazioni sulla codifica delle immagini tramite l'API WIC, vedere Cenni preliminari [sulla codifica.](-wic-creating-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="2a6c2-132">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="2a6c2-133">Opzioni del codificatore</span><span class="sxs-lookup"><span data-stu-id="2a6c2-133">Encoder Options</span></span>

<span data-ttu-id="2a6c2-134">I codec abilitati per WIC differiscono a livello di opzione di codifica.</span><span class="sxs-lookup"><span data-stu-id="2a6c2-134">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="2a6c2-135">Le opzioni del codificatore riflettono le funzionalità di un codificatore di immagini e ogni codec nativo supporta un set di queste opzioni del codificatore.</span><span class="sxs-lookup"><span data-stu-id="2a6c2-135">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="2a6c2-136">Le opzioni del codificatore possono essere opzioni di base supportate da WIC disponibili per tutti i codici abilitati per WIC (anche se non necessariamente supportate) o opzioni specifiche del codec progettate dal codec di formato immagine.</span><span class="sxs-lookup"><span data-stu-id="2a6c2-136">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="2a6c2-137">Per gestire queste opzioni di codifica durante il processo di codifica, WIC usa [**l'interfaccia IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2a6c2-137">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="2a6c2-138">Per altre informazioni sull'uso **dell'interfaccia IPropertyBag2** per la codifica WIC, vedere Cenni [preliminari sulla codifica.](-wic-creating-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="2a6c2-138">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="2a6c2-139">Il codec JPEG usa le opzioni WIC di base.</span><span class="sxs-lookup"><span data-stu-id="2a6c2-139">The JPEG codec uses basic WIC options.</span></span> <span data-ttu-id="2a6c2-140">La tabella seguente elenca le opzioni del codificatore WIC supportate dal codec JPEG nativo.</span><span class="sxs-lookup"><span data-stu-id="2a6c2-140">The following table lists the WIC encoder options supported by the native JPEG codec.</span></span>



| <span data-ttu-id="2a6c2-141">Nome della proprietà</span><span class="sxs-lookup"><span data-stu-id="2a6c2-141">Property Name</span></span>                                        | <span data-ttu-id="2a6c2-142">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="2a6c2-142">VARTYPE</span></span>           | <span data-ttu-id="2a6c2-143">Gamma valori</span><span class="sxs-lookup"><span data-stu-id="2a6c2-143">Value Range</span></span>                                                                       | <span data-ttu-id="2a6c2-144">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="2a6c2-144">Default Value</span></span>                                                                  |
|------------------------------------------------------|-------------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="2a6c2-145">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="2a6c2-145">ImageQuality</span></span>](#imagequality-option)                 | <span data-ttu-id="2a6c2-146">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="2a6c2-146">VT\_R4</span></span>            | <span data-ttu-id="2a6c2-147">0 - 1.0</span><span class="sxs-lookup"><span data-stu-id="2a6c2-147">0 - 1.0</span></span>                                                                           | <span data-ttu-id="2a6c2-148">0.9</span><span class="sxs-lookup"><span data-stu-id="2a6c2-148">0.9</span></span>                                                                            |
| [<span data-ttu-id="2a6c2-149">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="2a6c2-149">BitmapTransform</span></span>](#bitmaptransform-option)           | <span data-ttu-id="2a6c2-150">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="2a6c2-150">VT\_UI1</span></span>           | [<span data-ttu-id="2a6c2-151">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="2a6c2-151">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)         | [<span data-ttu-id="2a6c2-152">**WICBitmapTransformRotate0**</span><span class="sxs-lookup"><span data-stu-id="2a6c2-152">**WICBitmapTransformRotate0**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)      |
| [<span data-ttu-id="2a6c2-153">Luminanza</span><span class="sxs-lookup"><span data-stu-id="2a6c2-153">Luminance</span></span>](#luminance-option)                       | <span data-ttu-id="2a6c2-154">VT \_ UI4/VT \_ ARRAY</span><span class="sxs-lookup"><span data-stu-id="2a6c2-154">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="2a6c2-155">64 voci (DCT)</span><span class="sxs-lookup"><span data-stu-id="2a6c2-155">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="2a6c2-156">Tabella di luminance predefinita.</span><span class="sxs-lookup"><span data-stu-id="2a6c2-156">Default luminance table.</span></span>                                                       |
| [<span data-ttu-id="2a6c2-157">Chrominance</span><span class="sxs-lookup"><span data-stu-id="2a6c2-157">Chrominance</span></span>](#chrominance-option)                   | <span data-ttu-id="2a6c2-158">VT \_ UI4/VT \_ ARRAY</span><span class="sxs-lookup"><span data-stu-id="2a6c2-158">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="2a6c2-159">64 voci (DCT)</span><span class="sxs-lookup"><span data-stu-id="2a6c2-159">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="2a6c2-160">Tabella di cronologia predefinita.</span><span class="sxs-lookup"><span data-stu-id="2a6c2-160">Default chrominance table.</span></span>                                                     |
| [<span data-ttu-id="2a6c2-161">JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="2a6c2-161">JpegYCrCbSubsampling</span></span>](#jpegycrcbsubsampling-option) | <span data-ttu-id="2a6c2-162">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="2a6c2-162">VT\_UI1</span></span>           | [<span data-ttu-id="2a6c2-163">**WICJpegYCrCbSubsamplingOption**</span><span class="sxs-lookup"><span data-stu-id="2a6c2-163">**WICJpegYCrCbSubsamplingOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | [<span data-ttu-id="2a6c2-164">**WICJpegYCrCbSubsampling420**</span><span class="sxs-lookup"><span data-stu-id="2a6c2-164">**WICJpegYCrCbSubsampling420**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) |
| [<span data-ttu-id="2a6c2-165">SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="2a6c2-165">SuppressApp0</span></span>](/windows)                       | <span data-ttu-id="2a6c2-166">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="2a6c2-166">VT\_BOOL</span></span>          | <span data-ttu-id="2a6c2-167">**TRUE** / **FALSE**</span><span class="sxs-lookup"><span data-stu-id="2a6c2-167">**TRUE**/**FALSE**</span></span>                                                                | <span data-ttu-id="2a6c2-168">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="2a6c2-168">**FALSE**</span></span>                                                                      |



 

<span data-ttu-id="2a6c2-169">Se un'opzione del codificatore è presente [**nell'elenco di opzioni IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) non supportato dal codec, viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="2a6c2-169">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="imagequality-option"></a><span data-ttu-id="2a6c2-170">Opzione ImageQuality</span><span class="sxs-lookup"><span data-stu-id="2a6c2-170">ImageQuality Option</span></span>

<span data-ttu-id="2a6c2-171">Specifica la fedeltà dell'immagine desiderata.</span><span class="sxs-lookup"><span data-stu-id="2a6c2-171">Specifies the desired image fidelity.</span></span> <span data-ttu-id="2a6c2-172">0,0 indica la fedeltà più bassa possibile e 1.0 specifica la massima fedeltà.</span><span class="sxs-lookup"><span data-stu-id="2a6c2-172">0.0 indicates the lowest possible fidelity and 1.0 specifies the highest fidelity.</span></span>

<span data-ttu-id="2a6c2-173">Il valore predefinito è 0,9.</span><span class="sxs-lookup"><span data-stu-id="2a6c2-173">The default value is 0.9.</span></span>

### <a name="bitmaptransform-option"></a><span data-ttu-id="2a6c2-174">Opzione BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="2a6c2-174">BitmapTransform Option</span></span>

<span data-ttu-id="2a6c2-175">Specifica come l'immagine deve essere trasformata durante la decodifica dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2a6c2-175">Specifies how the image is to be transformed during image decoding.</span></span> <span data-ttu-id="2a6c2-176">Questa opzione deve essere impostata su uno dei valori di [**enumerazione WICBitmapTransformOptions.**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)</span><span class="sxs-lookup"><span data-stu-id="2a6c2-176">This option must be set to one of the [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) enumeration values.</span></span>

<span data-ttu-id="2a6c2-177">Il valore predefinito è [**WICBitmapTransformRotate0.**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)</span><span class="sxs-lookup"><span data-stu-id="2a6c2-177">The default value is [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).</span></span>

### <a name="luminance-option"></a><span data-ttu-id="2a6c2-178">Opzione Luminance</span><span class="sxs-lookup"><span data-stu-id="2a6c2-178">Luminance Option</span></span>

<span data-ttu-id="2a6c2-179">Specifica la tabella del livello di luminosità in scala di grigi da utilizzare per la codifica.</span><span class="sxs-lookup"><span data-stu-id="2a6c2-179">Specifies the grayscale brightness level table to use for encoding.</span></span>

### <a name="chrominance-option"></a><span data-ttu-id="2a6c2-180">Opzione Chrominance</span><span class="sxs-lookup"><span data-stu-id="2a6c2-180">Chrominance Option</span></span>

<span data-ttu-id="2a6c2-181">Specifica la tabella chrominance da usare per la codifica.</span><span class="sxs-lookup"><span data-stu-id="2a6c2-181">Specifies the chrominance table to use for encoding.</span></span>

### <a name="jpegycrcbsubsampling-option"></a><span data-ttu-id="2a6c2-182">Opzione JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="2a6c2-182">JpegYCrCbSubsampling Option</span></span>

<span data-ttu-id="2a6c2-183">Specifica il rapporto di sottocampionamento da usare per la codifica YCrCb.</span><span class="sxs-lookup"><span data-stu-id="2a6c2-183">Specifies the subsampling ratio to use for YCrCb encoding.</span></span>

<span data-ttu-id="2a6c2-184">Il valore predefinito [**è WICJpegYCrCbSubsampling420.**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption)</span><span class="sxs-lookup"><span data-stu-id="2a6c2-184">The default value is [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).</span></span>

### <a name="suppressapp0-option"></a><span data-ttu-id="2a6c2-185">Opzione SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="2a6c2-185">SuppressApp0 Option</span></span>

<span data-ttu-id="2a6c2-186">Specifica se eliminare la scrittura dei metadati App0 durante la codifica dei dati dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2a6c2-186">Specifies whether to suppress the write of App0 metadata while encoding the image data.</span></span>

<span data-ttu-id="2a6c2-187">Il valore predefinito è **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="2a6c2-187">The default value is **FALSE**.</span></span>

## <a name="decoding"></a><span data-ttu-id="2a6c2-188">Decodifica</span><span class="sxs-lookup"><span data-stu-id="2a6c2-188">Decoding</span></span>

<span data-ttu-id="2a6c2-189">L'API di decodifica WIC è progettata per essere indipendente dal codec e la decodifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="2a6c2-189">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="2a6c2-190">Per altre informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="2a6c2-190">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="2a6c2-191">Per altre informazioni sull'uso di dati di immagine decodificati, vedere Cenni [preliminari sulle origini bitmap.](-wic-bitmapsources.md)</span><span class="sxs-lookup"><span data-stu-id="2a6c2-191">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="2a6c2-192">Il codec JPEG nativo supporta anche [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) nella decodifica dei fotogrammi aggiungendo opzioni avanzate per la decodifica di un flusso di immagine.</span><span class="sxs-lookup"><span data-stu-id="2a6c2-192">The native JPEG codec also supports the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) on frame decoding adding advaced options for decoding an image stream.</span></span> <span data-ttu-id="2a6c2-193">Per altre informazioni su queste opzioni avanzate, vedere Cenni preliminari [sulle origini bitmap.](-wic-bitmapsources.md)</span><span class="sxs-lookup"><span data-stu-id="2a6c2-193">For more information about these advanced options, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
