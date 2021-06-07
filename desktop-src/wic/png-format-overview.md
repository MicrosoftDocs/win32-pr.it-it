---
description: In questo argomento vengono fornite informazioni sul codec PNG nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: 703217EA-70C8-4F86-B8DF-95468C78C8DA
title: Panoramica del formato PNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bb00b7530a22fcdbcce112053431ace5e553383
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444442"
---
# <a name="png-format-overview"></a><span data-ttu-id="4386b-103">Panoramica del formato PNG</span><span class="sxs-lookup"><span data-stu-id="4386b-103">PNG Format Overview</span></span>

<span data-ttu-id="4386b-104">In questo argomento vengono fornite informazioni sul codec PNG nativo disponibile tramite Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="4386b-104">This topic provides information about the native PNG codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="4386b-105">Identità codec</span><span class="sxs-lookup"><span data-stu-id="4386b-105">Codec Identity</span></span>

<span data-ttu-id="4386b-106">Nella tabella seguente vengono fornite informazioni di identificazione dei codec.</span><span class="sxs-lookup"><span data-stu-id="4386b-106">The following table provides codec identification information.</span></span>



|     <span data-ttu-id="4386b-107">Componente</span><span class="sxs-lookup"><span data-stu-id="4386b-107">Component</span></span>          | <span data-ttu-id="4386b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4386b-108">Description</span></span>                     |
|------------------------|---------------------------------|
| <span data-ttu-id="4386b-109">Nomi formali</span><span class="sxs-lookup"><span data-stu-id="4386b-109">Formal Name(s)</span></span>         | <span data-ttu-id="4386b-110">Portable Network Graphics (PNG)</span><span class="sxs-lookup"><span data-stu-id="4386b-110">Portable Network Graphics (PNG)</span></span> |
| <span data-ttu-id="4386b-111">Estensioni di file</span><span class="sxs-lookup"><span data-stu-id="4386b-111">File Name Extension(s)</span></span> | <span data-ttu-id="4386b-112">png</span><span class="sxs-lookup"><span data-stu-id="4386b-112">png</span></span>                             |
| <span data-ttu-id="4386b-113">tipo MIME</span><span class="sxs-lookup"><span data-stu-id="4386b-113">MIME type</span></span>              | <span data-ttu-id="4386b-114">image/png</span><span class="sxs-lookup"><span data-stu-id="4386b-114">image/png</span></span>                       |
| <span data-ttu-id="4386b-115">Supporto delle specifiche</span><span class="sxs-lookup"><span data-stu-id="4386b-115">Specification Support</span></span>  | <span data-ttu-id="4386b-116">Specifica PNG 1.2</span><span class="sxs-lookup"><span data-stu-id="4386b-116">PNG Specification 1.2</span></span>           |



 

<span data-ttu-id="4386b-117">Nella tabella seguente sono elencati i GUID usati per identificare i componenti nativi del codec PNG.</span><span class="sxs-lookup"><span data-stu-id="4386b-117">The following table lists the GUIDs used to identify the native PNG codec components.</span></span>



| <span data-ttu-id="4386b-118">Componente</span><span class="sxs-lookup"><span data-stu-id="4386b-118">Component</span></span>        | <span data-ttu-id="4386b-119">Nome descrittivo</span><span class="sxs-lookup"><span data-stu-id="4386b-119">Friendly Name</span></span>            | <span data-ttu-id="4386b-120">GUID</span><span class="sxs-lookup"><span data-stu-id="4386b-120">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="4386b-121">Formato contenitore</span><span class="sxs-lookup"><span data-stu-id="4386b-121">Container Format</span></span> | <span data-ttu-id="4386b-122">GUID \_ ContainerFormatPng</span><span class="sxs-lookup"><span data-stu-id="4386b-122">GUID\_ContainerFormatPng</span></span> | <span data-ttu-id="4386b-123">1b7cfaf4-713f-473c-bbcd6137425faeaf</span><span class="sxs-lookup"><span data-stu-id="4386b-123">1b7cfaf4-713f-473c-bbcd6137425faeaf</span></span> |
| <span data-ttu-id="4386b-124">Decodificatore</span><span class="sxs-lookup"><span data-stu-id="4386b-124">Decoder</span></span>          | <span data-ttu-id="4386b-125">CLSID \_ WICPngDecoder</span><span class="sxs-lookup"><span data-stu-id="4386b-125">CLSID\_WICPngDecoder</span></span>     | <span data-ttu-id="4386b-126">389ea17b-5078-4cde-b6ef25c15175c751</span><span class="sxs-lookup"><span data-stu-id="4386b-126">389ea17b-5078-4cde-b6ef25c15175c751</span></span> |
| <span data-ttu-id="4386b-127">Codificatore</span><span class="sxs-lookup"><span data-stu-id="4386b-127">Encoder</span></span>          | <span data-ttu-id="4386b-128">CLSID \_ WICPngEncoder</span><span class="sxs-lookup"><span data-stu-id="4386b-128">CLSID\_WICPngEncoder</span></span>     | <span data-ttu-id="4386b-129">27949969-876a-41d7-9447568f6a35a4dc</span><span class="sxs-lookup"><span data-stu-id="4386b-129">27949969-876a-41d7-9447568f6a35a4dc</span></span> |



 

### <a name="windows-8-and-later"></a><span data-ttu-id="4386b-130">Windows 8 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="4386b-130">Windows 8 and later</span></span>

<span data-ttu-id="4386b-131">A partire da Windows 8 WIC fornisce un decodificatore PNG aggiuntivo</span><span class="sxs-lookup"><span data-stu-id="4386b-131">Starting with Windows 8 WIC provides an additional PNG decoder</span></span>

## <a name="encoding"></a><span data-ttu-id="4386b-132">Codifica</span><span class="sxs-lookup"><span data-stu-id="4386b-132">Encoding</span></span>

<span data-ttu-id="4386b-133">L'API di codifica WIC è progettata per essere indipendente dal codec e la codifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="4386b-133">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="4386b-134">Per altre informazioni sulla codifica delle immagini tramite l'API WIC, vedere Cenni [preliminari sulla codifica](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="4386b-134">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="4386b-135">Opzioni del codificatore</span><span class="sxs-lookup"><span data-stu-id="4386b-135">Encoder Options</span></span>

<span data-ttu-id="4386b-136">I codec abilitati per WIC differiscono a livello di opzione di codifica.</span><span class="sxs-lookup"><span data-stu-id="4386b-136">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="4386b-137">Le opzioni del codificatore riflettono le funzionalità di un codificatore di immagini e ogni codec nativo supporta un set di queste opzioni del codificatore.</span><span class="sxs-lookup"><span data-stu-id="4386b-137">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="4386b-138">Le opzioni del codificatore possono essere opzioni di base supportate da WIC disponibili per tutti i codici abilitati per WIC (anche se non necessariamente supportate) o opzioni specifiche del codec progettate dal codec del formato immagine.</span><span class="sxs-lookup"><span data-stu-id="4386b-138">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="4386b-139">Per gestire queste opzioni di codifica durante il processo di codifica, WIC usa [**l'interfaccia IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4386b-139">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="4386b-140">Per altre informazioni sull'uso **dell'interfaccia IPropertyBag2** per la codifica WIC, vedere Cenni [preliminari sulla codifica](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="4386b-140">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="4386b-141">Il codec PNG usa le opzioni del codificatore WIC di base.</span><span class="sxs-lookup"><span data-stu-id="4386b-141">The PNG codec uses basic WIC encoder options.</span></span> <span data-ttu-id="4386b-142">Nella tabella seguente sono elencate le opzioni del codificatore WIC supportate dal codec PNG nativo.</span><span class="sxs-lookup"><span data-stu-id="4386b-142">The following table lists the WIC encoder options supported by the native PNG codec.</span></span>



| <span data-ttu-id="4386b-143">Nome della proprietà</span><span class="sxs-lookup"><span data-stu-id="4386b-143">Property Name</span></span>   | <span data-ttu-id="4386b-144">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="4386b-144">VARTYPE</span></span>  | <span data-ttu-id="4386b-145">Gamma valori</span><span class="sxs-lookup"><span data-stu-id="4386b-145">Value Range</span></span>                                                 | <span data-ttu-id="4386b-146">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="4386b-146">Default Value</span></span>                                                    |
|-----------------|----------|-------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="4386b-147">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="4386b-147">InterlaceOption</span></span> | <span data-ttu-id="4386b-148">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="4386b-148">VT\_BOOL</span></span> | <span data-ttu-id="4386b-149">**TRUE** / **FALSE**</span><span class="sxs-lookup"><span data-stu-id="4386b-149">**TRUE**/**FALSE**</span></span>                                          | <span data-ttu-id="4386b-150">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="4386b-150">**FALSE**</span></span>                                                        |
| <span data-ttu-id="4386b-151">FilterOption</span><span class="sxs-lookup"><span data-stu-id="4386b-151">FilterOption</span></span>    | <span data-ttu-id="4386b-152">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="4386b-152">VT\_UI1</span></span>  | [<span data-ttu-id="4386b-153">**WICPngFilterOption**</span><span class="sxs-lookup"><span data-stu-id="4386b-153">**WICPngFilterOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) | [<span data-ttu-id="4386b-154">**WICPngFilterUnspecified**</span><span class="sxs-lookup"><span data-stu-id="4386b-154">**WICPngFilterUnspecified**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) |



 

<span data-ttu-id="4386b-155">Se un'opzione del codificatore è presente nell'elenco di opzioni [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) non supportato dal codec, viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="4386b-155">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="interlaceoption"></a><span data-ttu-id="4386b-156">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="4386b-156">InterlaceOption</span></span>

<span data-ttu-id="4386b-157">Specifica se codificare i dati dell'immagine come interlacciati.</span><span class="sxs-lookup"><span data-stu-id="4386b-157">Specifies whether to encode the image data as interlaced.</span></span>

<span data-ttu-id="4386b-158">Il valore predefinito è **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="4386b-158">The default value is **FALSE**.</span></span>

### <a name="filteroption"></a><span data-ttu-id="4386b-159">FilterOption</span><span class="sxs-lookup"><span data-stu-id="4386b-159">FilterOption</span></span>

<span data-ttu-id="4386b-160">Specifica l'opzione di filtro da utilizzare per la compressione delle immagini.</span><span class="sxs-lookup"><span data-stu-id="4386b-160">Specifies the filter option to use for image compression.</span></span>

<span data-ttu-id="4386b-161">Il valore predefinito è [**WICPngFilterUnspecified.**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)</span><span class="sxs-lookup"><span data-stu-id="4386b-161">The default value is [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption).</span></span>

## <a name="decoding"></a><span data-ttu-id="4386b-162">Decodifica</span><span class="sxs-lookup"><span data-stu-id="4386b-162">Decoding</span></span>

<span data-ttu-id="4386b-163">L'API di decodifica WIC è progettata per essere indipendente dal codec e la decodifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="4386b-163">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="4386b-164">Per altre informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="4386b-164">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="4386b-165">Per altre informazioni sull'uso di dati immagine decodificati, vedere Panoramica [delle origini bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="4386b-165">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="4386b-166">Il codec PNG nativo supporta anche [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) per la decodifica dei fotogrammi aggiungendo opzioni avanzate per la decodifica di un flusso di immagine.</span><span class="sxs-lookup"><span data-stu-id="4386b-166">The native PNG codec also supports the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) on frame decoding adding advanced options for decoding an image stream.</span></span> <span data-ttu-id="4386b-167">Per altre informazioni su queste opzioni avanzate, vedere Panoramica [delle origini bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="4386b-167">For more information about these advanced options, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
