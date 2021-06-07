---
description: Questo argomento fornisce informazioni sul codec TIFF nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: 021AAF33-A89E-4336-AEB1-1A0D79A14C75
title: Panoramica del formato TIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b28dfcc85dac21e95e6c76118d2db57cb74a08
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444422"
---
# <a name="tiff-format-overview"></a><span data-ttu-id="10e49-103">Panoramica del formato TIFF</span><span class="sxs-lookup"><span data-stu-id="10e49-103">TIFF Format Overview</span></span>

<span data-ttu-id="10e49-104">Questo argomento fornisce informazioni sul codec TIFF nativo disponibile tramite Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="10e49-104">This topic provides information about the native TIFF codec available through Windows Imaging Component (WIC).</span></span>

-   [<span data-ttu-id="10e49-105">Codec Identity</span><span class="sxs-lookup"><span data-stu-id="10e49-105">Codec Identity</span></span>](#codec-identity)
-   [<span data-ttu-id="10e49-106">Encoding</span><span class="sxs-lookup"><span data-stu-id="10e49-106">Encoding</span></span>](#encoding)
    -   [<span data-ttu-id="10e49-107">Opzioni del codificatore</span><span class="sxs-lookup"><span data-stu-id="10e49-107">Encoder Options</span></span>](#encoder-options)
-   [<span data-ttu-id="10e49-108">Decodifica</span><span class="sxs-lookup"><span data-stu-id="10e49-108">Decoding</span></span>](#decoding)

## <a name="codec-identity"></a><span data-ttu-id="10e49-109">Codec Identity</span><span class="sxs-lookup"><span data-stu-id="10e49-109">Codec Identity</span></span>

<span data-ttu-id="10e49-110">Nella tabella seguente vengono fornite informazioni di identificazione del codec.</span><span class="sxs-lookup"><span data-stu-id="10e49-110">The following table provides codec identification information.</span></span>



|   <span data-ttu-id="10e49-111">Componente</span><span class="sxs-lookup"><span data-stu-id="10e49-111">Component</span></span>            |   <span data-ttu-id="10e49-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10e49-112">Description</span></span>                   |
|------------------------|---------------------------------|
| <span data-ttu-id="10e49-113">Nomi formali</span><span class="sxs-lookup"><span data-stu-id="10e49-113">Formal Name(s)</span></span>         | <span data-ttu-id="10e49-114">Tagged Image File Format (TIFF)</span><span class="sxs-lookup"><span data-stu-id="10e49-114">Tagged Image File Format (TIFF)</span></span> |
| <span data-ttu-id="10e49-115">Estensioni di file</span><span class="sxs-lookup"><span data-stu-id="10e49-115">File Name Extension(s)</span></span> | <span data-ttu-id="10e49-116">tiff, tif</span><span class="sxs-lookup"><span data-stu-id="10e49-116">tiff, tif</span></span>                       |
| <span data-ttu-id="10e49-117">Tipi MIME</span><span class="sxs-lookup"><span data-stu-id="10e49-117">MIME type(s)</span></span>           | <span data-ttu-id="10e49-118">image/tiff, image/tif</span><span class="sxs-lookup"><span data-stu-id="10e49-118">image/tiff, image/tif</span></span>           |
| <span data-ttu-id="10e49-119">Supporto delle specifiche</span><span class="sxs-lookup"><span data-stu-id="10e49-119">Specification Support</span></span>  | <span data-ttu-id="10e49-120">Specifica TIFF 6.0</span><span class="sxs-lookup"><span data-stu-id="10e49-120">TIFF Specification 6.0</span></span>          |



 

<span data-ttu-id="10e49-121">Nella tabella seguente sono elencati i GUID utilizzati per identificare i componenti nativi del codec TIFF.</span><span class="sxs-lookup"><span data-stu-id="10e49-121">The following table lists the GUIDs used to identify the native TIFF codec components.</span></span>



| <span data-ttu-id="10e49-122">Componente</span><span class="sxs-lookup"><span data-stu-id="10e49-122">Component</span></span>        | <span data-ttu-id="10e49-123">Nome descrittivo</span><span class="sxs-lookup"><span data-stu-id="10e49-123">Friendly Name</span></span>             | <span data-ttu-id="10e49-124">GUID</span><span class="sxs-lookup"><span data-stu-id="10e49-124">GUID</span></span>                                 |
|------------------|---------------------------|--------------------------------------|
| <span data-ttu-id="10e49-125">Formato contenitore</span><span class="sxs-lookup"><span data-stu-id="10e49-125">Container Format</span></span> | <span data-ttu-id="10e49-126">GUID \_ ContainerFormatTiff</span><span class="sxs-lookup"><span data-stu-id="10e49-126">GUID\_ContainerFormatTiff</span></span> | <span data-ttu-id="10e49-127">163bcc30-e2e9-4f0b-961da3e9fdb788a3</span><span class="sxs-lookup"><span data-stu-id="10e49-127">163bcc30-e2e9-4f0b-961da3e9fdb788a3</span></span>  |
| <span data-ttu-id="10e49-128">Decodificatore</span><span class="sxs-lookup"><span data-stu-id="10e49-128">Decoder</span></span>          | <span data-ttu-id="10e49-129">CLSID \_ WICTiffDecoder</span><span class="sxs-lookup"><span data-stu-id="10e49-129">CLSID\_WICTiffDecoder</span></span>     | <span data-ttu-id="10e49-130">b54e85d9-fe23-499f-8b886acea7137502b</span><span class="sxs-lookup"><span data-stu-id="10e49-130">b54e85d9-fe23-499f-8b886acea7137502b</span></span> |
| <span data-ttu-id="10e49-131">Codificatore</span><span class="sxs-lookup"><span data-stu-id="10e49-131">Encoder</span></span>          | <span data-ttu-id="10e49-132">CLSID \_ WICTiffEncoder</span><span class="sxs-lookup"><span data-stu-id="10e49-132">CLSID\_WICTiffEncoder</span></span>     | <span data-ttu-id="10e49-133">0131be10-2001-4c5f-a9b0cc88fab64ce8</span><span class="sxs-lookup"><span data-stu-id="10e49-133">0131be10-2001-4c5f-a9b0cc88fab64ce8</span></span>  |



 

## <a name="encoding"></a><span data-ttu-id="10e49-134">Codifica</span><span class="sxs-lookup"><span data-stu-id="10e49-134">Encoding</span></span>

<span data-ttu-id="10e49-135">L'API di codifica WIC è progettata per essere indipendente dal codec e la codifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="10e49-135">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="10e49-136">Per altre informazioni sulla codifica delle immagini tramite l'API WIC, vedere Cenni preliminari [sulla codifica.](-wic-creating-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="10e49-136">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="10e49-137">Opzioni del codificatore</span><span class="sxs-lookup"><span data-stu-id="10e49-137">Encoder Options</span></span>

<span data-ttu-id="10e49-138">I codec abilitati per WIC differiscono a livello di opzione di codifica.</span><span class="sxs-lookup"><span data-stu-id="10e49-138">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="10e49-139">Le opzioni del codificatore riflettono le funzionalità di un codificatore di immagini e ogni codec nativo supporta un set di queste opzioni del codificatore.</span><span class="sxs-lookup"><span data-stu-id="10e49-139">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="10e49-140">Le opzioni del codificatore possono essere opzioni di base supportate da WIC disponibili per tutti i codici abilitati per WIC (anche se non necessariamente supportate) o opzioni specifiche del codec progettate dal codec di formato immagine.</span><span class="sxs-lookup"><span data-stu-id="10e49-140">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="10e49-141">Per gestire queste opzioni di codifica durante il processo di codifica, WIC usa [**l'interfaccia IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="10e49-141">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="10e49-142">Per altre informazioni sull'uso **dell'interfaccia IPropertyBag2** per la codifica WIC, vedere Cenni [preliminari sulla codifica.](-wic-creating-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="10e49-142">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="10e49-143">Il codec TIFF usa le opzioni WIC di base.</span><span class="sxs-lookup"><span data-stu-id="10e49-143">The TIFF codec uses basic WIC options.</span></span> <span data-ttu-id="10e49-144">La tabella seguente elenca le opzioni del codificatore WIC supportate dal codec TIFF nativo.</span><span class="sxs-lookup"><span data-stu-id="10e49-144">The following table lists the WIC encoder options supported by the native TIFF codec.</span></span>

| <span data-ttu-id="10e49-145">Nome della proprietà</span><span class="sxs-lookup"><span data-stu-id="10e49-145">Property Name</span></span>         | <span data-ttu-id="10e49-146">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="10e49-146">VARTYPE</span></span> | <span data-ttu-id="10e49-147">Gamma valori</span><span class="sxs-lookup"><span data-stu-id="10e49-147">Value Range</span></span> | <span data-ttu-id="10e49-148">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="10e49-148">Default Value</span></span>    |
|-----------------------|---------|-------------|------------------|
| <span data-ttu-id="10e49-149">CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="10e49-149">CompressionQuality</span></span>    | <span data-ttu-id="10e49-150">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="10e49-150">VT\_R4</span></span>  | <span data-ttu-id="10e49-151">0 - 1.0</span><span class="sxs-lookup"><span data-stu-id="10e49-151">0 - 1.0</span></span>     | <span data-ttu-id="10e49-152">0</span><span class="sxs-lookup"><span data-stu-id="10e49-152">0</span></span>                |
| <span data-ttu-id="10e49-153">TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="10e49-153">TiffCompressionMethod</span></span> | <span data-ttu-id="10e49-154">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="10e49-154">VT\_UI1</span></span> | [<span data-ttu-id="10e49-155">**WICTiffCompressionOption**</span><span class="sxs-lookup"><span data-stu-id="10e49-155">**WICTiffCompressionOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) | [<span data-ttu-id="10e49-156">**WICTiffCompressionDontCare**</span><span class="sxs-lookup"><span data-stu-id="10e49-156">**WICTiffCompressionDontCare**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) |

<span data-ttu-id="10e49-157">Se un'opzione del codificatore è presente [**nell'elenco di opzioni IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) non supportato dal codec, viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="10e49-157">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="compressionquality-option"></a><span data-ttu-id="10e49-158">Opzione CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="10e49-158">CompressionQuality Option</span></span>

<span data-ttu-id="10e49-159">Specifica la qualità di compressione desiderata.</span><span class="sxs-lookup"><span data-stu-id="10e49-159">Specifies the desired compression quality.</span></span> <span data-ttu-id="10e49-160">0,0 indica lo schema di compressione meno efficiente disponibile.</span><span class="sxs-lookup"><span data-stu-id="10e49-160">0.0 indicates the least efficient compression scheme available.</span></span> <span data-ttu-id="10e49-161">In genere, questo schema comporta una codifica più veloce ma un output più grande.</span><span class="sxs-lookup"><span data-stu-id="10e49-161">Typically, this scheme results in a faster encode but larger output.</span></span> <span data-ttu-id="10e49-162">Il valore 1.0 specifica lo schema di compressione più efficiente disponibile.</span><span class="sxs-lookup"><span data-stu-id="10e49-162">A value of 1.0 specifies the most efficient compression scheme available.</span></span> <span data-ttu-id="10e49-163">In genere, questo schema comporta una codifica più lunga, ma produce un output più piccolo.</span><span class="sxs-lookup"><span data-stu-id="10e49-163">Typically, this scheme results in a longer encode but produces smaller output.</span></span>

<span data-ttu-id="10e49-164">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="10e49-164">The default value is 0.</span></span>

### <a name="tiffcompressionmethod-option"></a><span data-ttu-id="10e49-165">Opzione TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="10e49-165">TiffCompressionMethod Option</span></span>

<span data-ttu-id="10e49-166">Specifica il metodo di compressione TIFF.</span><span class="sxs-lookup"><span data-stu-id="10e49-166">Specifies the TIFF compression method.</span></span>

<span data-ttu-id="10e49-167">Il valore predefinito è [**WICTiffCompressionDontCare.**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)</span><span class="sxs-lookup"><span data-stu-id="10e49-167">The default value is [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption).</span></span>

## <a name="decoding"></a><span data-ttu-id="10e49-168">Decodifica</span><span class="sxs-lookup"><span data-stu-id="10e49-168">Decoding</span></span>

<span data-ttu-id="10e49-169">Le API di decodifica WIC sono progettate per essere indipendenti dal codec e la decodifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="10e49-169">The WIC decoding APIs are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="10e49-170">Per altre informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="10e49-170">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="10e49-171">Per altre informazioni sull'uso di dati di immagine decodificati, vedere Cenni [preliminari sulle origini bitmap.](-wic-bitmapsources.md)</span><span class="sxs-lookup"><span data-stu-id="10e49-171">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
