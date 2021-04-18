---
description: In questo argomento vengono fornite informazioni sul codec PNG nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: 703217EA-70C8-4F86-B8DF-95468C78C8DA
title: Panoramica del formato PNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 118d6af831c8fb6f8cacc8407e90f610c0fc426d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316380"
---
# <a name="png-format-overview"></a><span data-ttu-id="99e56-103">Panoramica del formato PNG</span><span class="sxs-lookup"><span data-stu-id="99e56-103">PNG Format Overview</span></span>

<span data-ttu-id="99e56-104">In questo argomento vengono fornite informazioni sul codec PNG nativo disponibile tramite Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="99e56-104">This topic provides information about the native PNG codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="99e56-105">Identità codec</span><span class="sxs-lookup"><span data-stu-id="99e56-105">Codec Identity</span></span>

<span data-ttu-id="99e56-106">Nella tabella seguente vengono fornite informazioni di identificazione del codec.</span><span class="sxs-lookup"><span data-stu-id="99e56-106">The following table provides codec identification information.</span></span>



|                        |                                 |
|------------------------|---------------------------------|
| <span data-ttu-id="99e56-107">Nome/i formale/i</span><span class="sxs-lookup"><span data-stu-id="99e56-107">Formal Name(s)</span></span>         | <span data-ttu-id="99e56-108">Portable Network Graphics (PNG)</span><span class="sxs-lookup"><span data-stu-id="99e56-108">Portable Network Graphics (PNG)</span></span> |
| <span data-ttu-id="99e56-109">Estensioni del nome di file</span><span class="sxs-lookup"><span data-stu-id="99e56-109">File Name Extension(s)</span></span> | <span data-ttu-id="99e56-110">png</span><span class="sxs-lookup"><span data-stu-id="99e56-110">png</span></span>                             |
| <span data-ttu-id="99e56-111">tipo MIME</span><span class="sxs-lookup"><span data-stu-id="99e56-111">MIME type</span></span>              | <span data-ttu-id="99e56-112">image/png</span><span class="sxs-lookup"><span data-stu-id="99e56-112">image/png</span></span>                       |
| <span data-ttu-id="99e56-113">Supporto delle specifiche</span><span class="sxs-lookup"><span data-stu-id="99e56-113">Specification Support</span></span>  | <span data-ttu-id="99e56-114">Specifica PNG 1,2</span><span class="sxs-lookup"><span data-stu-id="99e56-114">PNG Specification 1.2</span></span>           |



 

<span data-ttu-id="99e56-115">La tabella seguente elenca i GUID usati per identificare i componenti dei codec PNG nativi.</span><span class="sxs-lookup"><span data-stu-id="99e56-115">The following table lists the GUIDs used to identify the native PNG codec components.</span></span>



| <span data-ttu-id="99e56-116">Componente</span><span class="sxs-lookup"><span data-stu-id="99e56-116">Component</span></span>        | <span data-ttu-id="99e56-117">Nome descrittivo</span><span class="sxs-lookup"><span data-stu-id="99e56-117">Friendly Name</span></span>            | <span data-ttu-id="99e56-118">GUID</span><span class="sxs-lookup"><span data-stu-id="99e56-118">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="99e56-119">Formato contenitore</span><span class="sxs-lookup"><span data-stu-id="99e56-119">Container Format</span></span> | <span data-ttu-id="99e56-120">GUID \_ ContainerFormatPng</span><span class="sxs-lookup"><span data-stu-id="99e56-120">GUID\_ContainerFormatPng</span></span> | <span data-ttu-id="99e56-121">1b7cfaf4-713f-473c-bbcd6137425faeaf</span><span class="sxs-lookup"><span data-stu-id="99e56-121">1b7cfaf4-713f-473c-bbcd6137425faeaf</span></span> |
| <span data-ttu-id="99e56-122">Decodificatore</span><span class="sxs-lookup"><span data-stu-id="99e56-122">Decoder</span></span>          | <span data-ttu-id="99e56-123">\_WICPNGDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="99e56-123">CLSID\_WICPngDecoder</span></span>     | <span data-ttu-id="99e56-124">389ea17b-5078-4cde-b6ef25c15175c751</span><span class="sxs-lookup"><span data-stu-id="99e56-124">389ea17b-5078-4cde-b6ef25c15175c751</span></span> |
| <span data-ttu-id="99e56-125">Codificatore</span><span class="sxs-lookup"><span data-stu-id="99e56-125">Encoder</span></span>          | <span data-ttu-id="99e56-126">\_WICPNGENCODER CLSID</span><span class="sxs-lookup"><span data-stu-id="99e56-126">CLSID\_WICPngEncoder</span></span>     | <span data-ttu-id="99e56-127">27949969-876a-41d7-9447568f6a35a4dc</span><span class="sxs-lookup"><span data-stu-id="99e56-127">27949969-876a-41d7-9447568f6a35a4dc</span></span> |



 

### <a name="windows-8-and-later"></a><span data-ttu-id="99e56-128">Windows 8 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="99e56-128">Windows 8 and later</span></span>

<span data-ttu-id="99e56-129">A partire da Windows 8 WIC fornisce un decoder PNG aggiuntivo</span><span class="sxs-lookup"><span data-stu-id="99e56-129">Starting with Windows 8 WIC provides an additional PNG decoder</span></span>

## <a name="encoding"></a><span data-ttu-id="99e56-130">Codifica</span><span class="sxs-lookup"><span data-stu-id="99e56-130">Encoding</span></span>

<span data-ttu-id="99e56-131">L'API di codifica WIC è progettata per essere indipendente dal codec e la codifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="99e56-131">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="99e56-132">Per ulteriori informazioni sulla codifica delle immagini tramite l'API WIC, vedere [Cenni preliminari sulla codifica](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="99e56-132">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="99e56-133">Opzioni del codificatore</span><span class="sxs-lookup"><span data-stu-id="99e56-133">Encoder Options</span></span>

<span data-ttu-id="99e56-134">I codec abilitati per WIC differiscono a livello di opzione di codifica.</span><span class="sxs-lookup"><span data-stu-id="99e56-134">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="99e56-135">Le opzioni del codificatore riflettono le funzionalità di un codificatore di immagini e ogni codec nativo supporta un set di queste opzioni del codificatore.</span><span class="sxs-lookup"><span data-stu-id="99e56-135">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="99e56-136">Le opzioni del codificatore possono essere opzioni supportate per WIC di base disponibili per tutti i codici abilitati per WIC (anche se non necessariamente supportati) o per le opzioni specifiche del codec progettate dal codec del formato di immagine.</span><span class="sxs-lookup"><span data-stu-id="99e56-136">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="99e56-137">Per gestire queste opzioni di codifica durante il processo di codifica, WIC utilizza l'interfaccia [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="99e56-137">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="99e56-138">Per ulteriori informazioni sull'utilizzo dell'interfaccia **IPropertyBag2** per la codifica WIC, vedere [Cenni preliminari sulla codifica](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="99e56-138">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="99e56-139">Il codec PNG usa le opzioni di base del codificatore WIC.</span><span class="sxs-lookup"><span data-stu-id="99e56-139">The PNG codec uses basic WIC encoder options.</span></span> <span data-ttu-id="99e56-140">Nella tabella seguente sono elencate le opzioni del codificatore WIC supportate dal codec PNG nativo.</span><span class="sxs-lookup"><span data-stu-id="99e56-140">The following table lists the WIC encoder options supported by the native PNG codec.</span></span>



| <span data-ttu-id="99e56-141">Nome della proprietà</span><span class="sxs-lookup"><span data-stu-id="99e56-141">Property Name</span></span>   | <span data-ttu-id="99e56-142">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="99e56-142">VARTYPE</span></span>  | <span data-ttu-id="99e56-143">Gamma valori</span><span class="sxs-lookup"><span data-stu-id="99e56-143">Value Range</span></span>                                                 | <span data-ttu-id="99e56-144">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="99e56-144">Default Value</span></span>                                                    |
|-----------------|----------|-------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="99e56-145">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="99e56-145">InterlaceOption</span></span> | <span data-ttu-id="99e56-146">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="99e56-146">VT\_BOOL</span></span> | <span data-ttu-id="99e56-147">Valore **true** / **False**</span><span class="sxs-lookup"><span data-stu-id="99e56-147">**TRUE**/**FALSE**</span></span>                                          | <span data-ttu-id="99e56-148">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="99e56-148">**FALSE**</span></span>                                                        |
| <span data-ttu-id="99e56-149">FilterOption</span><span class="sxs-lookup"><span data-stu-id="99e56-149">FilterOption</span></span>    | <span data-ttu-id="99e56-150">\_Ui1 VT</span><span class="sxs-lookup"><span data-stu-id="99e56-150">VT\_UI1</span></span>  | [<span data-ttu-id="99e56-151">**WICPngFilterOption**</span><span class="sxs-lookup"><span data-stu-id="99e56-151">**WICPngFilterOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) | [<span data-ttu-id="99e56-152">**WICPngFilterUnspecified**</span><span class="sxs-lookup"><span data-stu-id="99e56-152">**WICPngFilterUnspecified**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) |



 

<span data-ttu-id="99e56-153">Se un'opzione del codificatore è presente nell'elenco di opzioni [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) che il codec non supporta, viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="99e56-153">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="interlaceoption"></a><span data-ttu-id="99e56-154">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="99e56-154">InterlaceOption</span></span>

<span data-ttu-id="99e56-155">Specifica se codificare i dati dell'immagine come interlacciato.</span><span class="sxs-lookup"><span data-stu-id="99e56-155">Specifies whether to encode the image data as interlaced.</span></span>

<span data-ttu-id="99e56-156">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="99e56-156">The default value is **FALSE**.</span></span>

### <a name="filteroption"></a><span data-ttu-id="99e56-157">FilterOption</span><span class="sxs-lookup"><span data-stu-id="99e56-157">FilterOption</span></span>

<span data-ttu-id="99e56-158">Specifica l'opzione di filtro da utilizzare per la compressione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="99e56-158">Specifies the filter option to use for image compression.</span></span>

<span data-ttu-id="99e56-159">Il valore predefinito è [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption).</span><span class="sxs-lookup"><span data-stu-id="99e56-159">The default value is [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption).</span></span>

## <a name="decoding"></a><span data-ttu-id="99e56-160">Decodifica</span><span class="sxs-lookup"><span data-stu-id="99e56-160">Decoding</span></span>

<span data-ttu-id="99e56-161">L'API di decodifica WIC è progettata per essere indipendente dal codec e la decodifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="99e56-161">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="99e56-162">Per ulteriori informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="99e56-162">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="99e56-163">Per ulteriori informazioni sull'utilizzo di dati di immagine decodificati, vedere [Cenni preliminari sulle origini bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="99e56-163">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="99e56-164">Il codec PNG nativo supporta anche [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) sulla decodifica dei frame aggiungendo opzioni avanzate per la decodifica di un flusso di immagini.</span><span class="sxs-lookup"><span data-stu-id="99e56-164">The native PNG codec also supports the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) on frame decoding adding advanced options for decoding an image stream.</span></span> <span data-ttu-id="99e56-165">Per ulteriori informazioni su queste opzioni avanzate, vedere [Cenni preliminari sulle origini bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="99e56-165">For more information about these advanced options, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
