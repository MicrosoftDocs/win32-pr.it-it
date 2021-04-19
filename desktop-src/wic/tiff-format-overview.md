---
description: In questo argomento vengono fornite informazioni sul codec TIFF nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: 021AAF33-A89E-4336-AEB1-1A0D79A14C75
title: Cenni preliminari sul formato TIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db603857da892d4b699bb7df7d8b3e2ee5566326
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317243"
---
# <a name="tiff-format-overview"></a><span data-ttu-id="c96cd-103">Cenni preliminari sul formato TIFF</span><span class="sxs-lookup"><span data-stu-id="c96cd-103">TIFF Format Overview</span></span>

<span data-ttu-id="c96cd-104">In questo argomento vengono fornite informazioni sul codec TIFF nativo disponibile tramite Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="c96cd-104">This topic provides information about the native TIFF codec available through Windows Imaging Component (WIC).</span></span>

-   [<span data-ttu-id="c96cd-105">Identità codec</span><span class="sxs-lookup"><span data-stu-id="c96cd-105">Codec Identity</span></span>](#codec-identity)
-   [<span data-ttu-id="c96cd-106">Encoding</span><span class="sxs-lookup"><span data-stu-id="c96cd-106">Encoding</span></span>](#encoding)
    -   [<span data-ttu-id="c96cd-107">Opzioni del codificatore</span><span class="sxs-lookup"><span data-stu-id="c96cd-107">Encoder Options</span></span>](#encoder-options)
-   [<span data-ttu-id="c96cd-108">Decodifica</span><span class="sxs-lookup"><span data-stu-id="c96cd-108">Decoding</span></span>](#decoding)

## <a name="codec-identity"></a><span data-ttu-id="c96cd-109">Identità codec</span><span class="sxs-lookup"><span data-stu-id="c96cd-109">Codec Identity</span></span>

<span data-ttu-id="c96cd-110">Nella tabella seguente vengono fornite informazioni di identificazione del codec.</span><span class="sxs-lookup"><span data-stu-id="c96cd-110">The following table provides codec identification information.</span></span>



|                        |                                 |
|------------------------|---------------------------------|
| <span data-ttu-id="c96cd-111">Nome/i formale/i</span><span class="sxs-lookup"><span data-stu-id="c96cd-111">Formal Name(s)</span></span>         | <span data-ttu-id="c96cd-112">Tagged Image File Format (TIFF)</span><span class="sxs-lookup"><span data-stu-id="c96cd-112">Tagged Image File Format (TIFF)</span></span> |
| <span data-ttu-id="c96cd-113">Estensioni del nome di file</span><span class="sxs-lookup"><span data-stu-id="c96cd-113">File Name Extension(s)</span></span> | <span data-ttu-id="c96cd-114">TIFF, TIF</span><span class="sxs-lookup"><span data-stu-id="c96cd-114">tiff, tif</span></span>                       |
| <span data-ttu-id="c96cd-115">Tipi MIME</span><span class="sxs-lookup"><span data-stu-id="c96cd-115">MIME type(s)</span></span>           | <span data-ttu-id="c96cd-116">image/TIFF, image/TIF</span><span class="sxs-lookup"><span data-stu-id="c96cd-116">image/tiff, image/tif</span></span>           |
| <span data-ttu-id="c96cd-117">Supporto delle specifiche</span><span class="sxs-lookup"><span data-stu-id="c96cd-117">Specification Support</span></span>  | <span data-ttu-id="c96cd-118">Specifica TIFF 6,0</span><span class="sxs-lookup"><span data-stu-id="c96cd-118">TIFF Specification 6.0</span></span>          |



 

<span data-ttu-id="c96cd-119">Nella tabella seguente sono elencati i GUID utilizzati per identificare i componenti codec TIFF nativi.</span><span class="sxs-lookup"><span data-stu-id="c96cd-119">The following table lists the GUIDs used to identify the native TIFF codec components.</span></span>



| <span data-ttu-id="c96cd-120">Componente</span><span class="sxs-lookup"><span data-stu-id="c96cd-120">Component</span></span>        | <span data-ttu-id="c96cd-121">Nome descrittivo</span><span class="sxs-lookup"><span data-stu-id="c96cd-121">Friendly Name</span></span>             | <span data-ttu-id="c96cd-122">GUID</span><span class="sxs-lookup"><span data-stu-id="c96cd-122">GUID</span></span>                                 |
|------------------|---------------------------|--------------------------------------|
| <span data-ttu-id="c96cd-123">Formato contenitore</span><span class="sxs-lookup"><span data-stu-id="c96cd-123">Container Format</span></span> | <span data-ttu-id="c96cd-124">GUID \_ ContainerFormatTiff</span><span class="sxs-lookup"><span data-stu-id="c96cd-124">GUID\_ContainerFormatTiff</span></span> | <span data-ttu-id="c96cd-125">163bcc30-e2e9-4f0b-961da3e9fdb788a3</span><span class="sxs-lookup"><span data-stu-id="c96cd-125">163bcc30-e2e9-4f0b-961da3e9fdb788a3</span></span>  |
| <span data-ttu-id="c96cd-126">Decodificatore</span><span class="sxs-lookup"><span data-stu-id="c96cd-126">Decoder</span></span>          | <span data-ttu-id="c96cd-127">\_WICTIFFDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="c96cd-127">CLSID\_WICTiffDecoder</span></span>     | <span data-ttu-id="c96cd-128">b54e85d9-FE23-499f-8b886acea7137502b</span><span class="sxs-lookup"><span data-stu-id="c96cd-128">b54e85d9-fe23-499f-8b886acea7137502b</span></span> |
| <span data-ttu-id="c96cd-129">Codificatore</span><span class="sxs-lookup"><span data-stu-id="c96cd-129">Encoder</span></span>          | <span data-ttu-id="c96cd-130">\_WICTIFFENCODER CLSID</span><span class="sxs-lookup"><span data-stu-id="c96cd-130">CLSID\_WICTiffEncoder</span></span>     | <span data-ttu-id="c96cd-131">0131be10-2001-4c5f-a9b0cc88fab64ce8</span><span class="sxs-lookup"><span data-stu-id="c96cd-131">0131be10-2001-4c5f-a9b0cc88fab64ce8</span></span>  |



 

## <a name="encoding"></a><span data-ttu-id="c96cd-132">Codifica</span><span class="sxs-lookup"><span data-stu-id="c96cd-132">Encoding</span></span>

<span data-ttu-id="c96cd-133">L'API di codifica WIC è progettata per essere indipendente dal codec e la codifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="c96cd-133">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="c96cd-134">Per ulteriori informazioni sulla codifica delle immagini tramite l'API WIC, vedere [Cenni preliminari sulla codifica](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="c96cd-134">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="c96cd-135">Opzioni del codificatore</span><span class="sxs-lookup"><span data-stu-id="c96cd-135">Encoder Options</span></span>

<span data-ttu-id="c96cd-136">I codec abilitati per WIC differiscono a livello di opzione di codifica.</span><span class="sxs-lookup"><span data-stu-id="c96cd-136">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="c96cd-137">Le opzioni del codificatore riflettono le funzionalità di un codificatore di immagini e ogni codec nativo supporta un set di queste opzioni del codificatore.</span><span class="sxs-lookup"><span data-stu-id="c96cd-137">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="c96cd-138">Le opzioni del codificatore possono essere opzioni supportate per WIC di base disponibili per tutti i codici abilitati per WIC (anche se non necessariamente supportati) o per le opzioni specifiche del codec progettate dal codec del formato di immagine.</span><span class="sxs-lookup"><span data-stu-id="c96cd-138">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="c96cd-139">Per gestire queste opzioni di codifica durante il processo di codifica, WIC utilizza l'interfaccia [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c96cd-139">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="c96cd-140">Per ulteriori informazioni sull'utilizzo dell'interfaccia **IPropertyBag2** per la codifica WIC, vedere [Cenni preliminari sulla codifica](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="c96cd-140">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="c96cd-141">Il codec TIFF usa le opzioni WIC di base.</span><span class="sxs-lookup"><span data-stu-id="c96cd-141">The TIFF codec uses basic WIC options.</span></span> <span data-ttu-id="c96cd-142">Nella tabella seguente sono elencate le opzioni del codificatore WIC supportate dal codec TIFF nativo.</span><span class="sxs-lookup"><span data-stu-id="c96cd-142">The following table lists the WIC encoder options supported by the native TIFF codec.</span></span>

| <span data-ttu-id="c96cd-143">Nome della proprietà</span><span class="sxs-lookup"><span data-stu-id="c96cd-143">Property Name</span></span>         | <span data-ttu-id="c96cd-144">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c96cd-144">VARTYPE</span></span> | <span data-ttu-id="c96cd-145">Gamma valori</span><span class="sxs-lookup"><span data-stu-id="c96cd-145">Value Range</span></span> | <span data-ttu-id="c96cd-146">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="c96cd-146">Default Value</span></span>    |
|-----------------------|---------|-------------|------------------|
| <span data-ttu-id="c96cd-147">CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="c96cd-147">CompressionQuality</span></span>    | <span data-ttu-id="c96cd-148">\_R4 VT</span><span class="sxs-lookup"><span data-stu-id="c96cd-148">VT\_R4</span></span>  | <span data-ttu-id="c96cd-149">0-1,0</span><span class="sxs-lookup"><span data-stu-id="c96cd-149">0 - 1.0</span></span>     | <span data-ttu-id="c96cd-150">0</span><span class="sxs-lookup"><span data-stu-id="c96cd-150">0</span></span>                |
| <span data-ttu-id="c96cd-151">TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="c96cd-151">TiffCompressionMethod</span></span> | <span data-ttu-id="c96cd-152">\_Ui1 VT</span><span class="sxs-lookup"><span data-stu-id="c96cd-152">VT\_UI1</span></span> | [<span data-ttu-id="c96cd-153">**WICTiffCompressionOption**</span><span class="sxs-lookup"><span data-stu-id="c96cd-153">**WICTiffCompressionOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) | [<span data-ttu-id="c96cd-154">**WICTiffCompressionDontCare**</span><span class="sxs-lookup"><span data-stu-id="c96cd-154">**WICTiffCompressionDontCare**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) |

<span data-ttu-id="c96cd-155">Se un'opzione del codificatore è presente nell'elenco di opzioni [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) che il codec non supporta, viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="c96cd-155">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="compressionquality-option"></a><span data-ttu-id="c96cd-156">CompressionQuality-opzione</span><span class="sxs-lookup"><span data-stu-id="c96cd-156">CompressionQuality Option</span></span>

<span data-ttu-id="c96cd-157">Specifica la qualità di compressione desiderata.</span><span class="sxs-lookup"><span data-stu-id="c96cd-157">Specifies the desired compression quality.</span></span> <span data-ttu-id="c96cd-158">0,0 indica lo schema di compressione meno efficiente disponibile.</span><span class="sxs-lookup"><span data-stu-id="c96cd-158">0.0 indicates the least efficient compression scheme available.</span></span> <span data-ttu-id="c96cd-159">In genere, questo schema genera una codifica più veloce ma un output più grande.</span><span class="sxs-lookup"><span data-stu-id="c96cd-159">Typically, this scheme results in a faster encode but larger output.</span></span> <span data-ttu-id="c96cd-160">Il valore 1,0 specifica lo schema di compressione più efficiente disponibile.</span><span class="sxs-lookup"><span data-stu-id="c96cd-160">A value of 1.0 specifies the most efficient compression scheme available.</span></span> <span data-ttu-id="c96cd-161">In genere, questo schema comporta una codifica più lunga, ma produce un output di dimensioni inferiori.</span><span class="sxs-lookup"><span data-stu-id="c96cd-161">Typically, this scheme results in a longer encode but produces smaller output.</span></span>

<span data-ttu-id="c96cd-162">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="c96cd-162">The default value is 0.</span></span>

### <a name="tiffcompressionmethod-option"></a><span data-ttu-id="c96cd-163">TiffCompressionMethod-opzione</span><span class="sxs-lookup"><span data-stu-id="c96cd-163">TiffCompressionMethod Option</span></span>

<span data-ttu-id="c96cd-164">Specifica il metodo di compressione TIFF.</span><span class="sxs-lookup"><span data-stu-id="c96cd-164">Specifies the TIFF compression method.</span></span>

<span data-ttu-id="c96cd-165">Il valore predefinito è [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption).</span><span class="sxs-lookup"><span data-stu-id="c96cd-165">The default value is [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption).</span></span>

## <a name="decoding"></a><span data-ttu-id="c96cd-166">Decodifica</span><span class="sxs-lookup"><span data-stu-id="c96cd-166">Decoding</span></span>

<span data-ttu-id="c96cd-167">Le API di decodifica WIC sono progettate per essere indipendenti dal codec e la decodifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="c96cd-167">The WIC decoding APIs are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="c96cd-168">Per ulteriori informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="c96cd-168">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="c96cd-169">Per ulteriori informazioni sull'utilizzo di dati di immagine decodificati, vedere [Cenni preliminari sulle origini bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="c96cd-169">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
