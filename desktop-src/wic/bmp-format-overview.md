---
description: In questo argomento vengono fornite informazioni sul codec BMP nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: 85AC5A30-A915-439E-A10F-B2833DDA995C
title: Panoramica del formato BMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3492189f80b43915bab94a7ea8359f2e5950f7c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756911"
---
# <a name="bmp-format-overview"></a><span data-ttu-id="b6e66-103">Panoramica del formato BMP</span><span class="sxs-lookup"><span data-stu-id="b6e66-103">BMP Format Overview</span></span>

<span data-ttu-id="b6e66-104">In questo argomento vengono fornite informazioni sul codec BMP nativo disponibile tramite Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="b6e66-104">This topic provides information about the native BMP codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="b6e66-105">Identità codec</span><span class="sxs-lookup"><span data-stu-id="b6e66-105">Codec Identity</span></span>

<span data-ttu-id="b6e66-106">Nella tabella seguente vengono fornite informazioni di identificazione del codec.</span><span class="sxs-lookup"><span data-stu-id="b6e66-106">The following table provides codec identification information.</span></span>



|                        |                       |
|------------------------|-----------------------|
| <span data-ttu-id="b6e66-107">Nome/i formale/i</span><span class="sxs-lookup"><span data-stu-id="b6e66-107">Formal Name(s)</span></span>         | <span data-ttu-id="b6e66-108">Formato bitmap Windows</span><span class="sxs-lookup"><span data-stu-id="b6e66-108">Windows Bitmap Format</span></span> |
| <span data-ttu-id="b6e66-109">Estensioni del nome di file</span><span class="sxs-lookup"><span data-stu-id="b6e66-109">File Name Extension(s)</span></span> | <span data-ttu-id="b6e66-110">BMP, DIB</span><span class="sxs-lookup"><span data-stu-id="b6e66-110">bmp, dib</span></span>              |
| <span data-ttu-id="b6e66-111">tipo MIME</span><span class="sxs-lookup"><span data-stu-id="b6e66-111">MIME type</span></span>              | <span data-ttu-id="b6e66-112">image/bmp</span><span class="sxs-lookup"><span data-stu-id="b6e66-112">image/bmp</span></span>             |
| <span data-ttu-id="b6e66-113">Supporto delle specifiche</span><span class="sxs-lookup"><span data-stu-id="b6e66-113">Specification Support</span></span>  | <span data-ttu-id="b6e66-114">Specifica BMP V5</span><span class="sxs-lookup"><span data-stu-id="b6e66-114">BMP Specification v5</span></span>  |



 

<span data-ttu-id="b6e66-115">La tabella seguente elenca i GUID usati per identificare i componenti dei codec BMP nativi.</span><span class="sxs-lookup"><span data-stu-id="b6e66-115">The following table lists the GUIDs used to identify the native BMP codec components.</span></span>



| <span data-ttu-id="b6e66-116">Componente</span><span class="sxs-lookup"><span data-stu-id="b6e66-116">Component</span></span>        | <span data-ttu-id="b6e66-117">Nome descrittivo</span><span class="sxs-lookup"><span data-stu-id="b6e66-117">Friendly Name</span></span>            | <span data-ttu-id="b6e66-118">GUID</span><span class="sxs-lookup"><span data-stu-id="b6e66-118">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="b6e66-119">Formato contenitore</span><span class="sxs-lookup"><span data-stu-id="b6e66-119">Container Format</span></span> | <span data-ttu-id="b6e66-120">GUID \_ ContainerFormatBmp</span><span class="sxs-lookup"><span data-stu-id="b6e66-120">GUID\_ContainerFormatBmp</span></span> | <span data-ttu-id="b6e66-121">0af1d87e-fcfe-4188-bdeba7906471cbe3</span><span class="sxs-lookup"><span data-stu-id="b6e66-121">0af1d87e-fcfe-4188-bdeba7906471cbe3</span></span> |
| <span data-ttu-id="b6e66-122">Decodificatore</span><span class="sxs-lookup"><span data-stu-id="b6e66-122">Decoder</span></span>          | <span data-ttu-id="b6e66-123">\_WICBMPDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="b6e66-123">CLSID\_WICBmpDecoder</span></span>     | <span data-ttu-id="b6e66-124">6b462062-7cbf-400D-9fdb813dd10f2778</span><span class="sxs-lookup"><span data-stu-id="b6e66-124">6b462062-7cbf-400d-9fdb813dd10f2778</span></span> |
| <span data-ttu-id="b6e66-125">Codificatore</span><span class="sxs-lookup"><span data-stu-id="b6e66-125">Encoder</span></span>          | <span data-ttu-id="b6e66-126">\_WICBMPENCODER CLSID</span><span class="sxs-lookup"><span data-stu-id="b6e66-126">CLSID\_WICBmpEncoder</span></span>     | <span data-ttu-id="b6e66-127">69be8bb4-d66d-47c8-865aed1589433782</span><span class="sxs-lookup"><span data-stu-id="b6e66-127">69be8bb4-d66d-47c8-865aed1589433782</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="b6e66-128">Codifica</span><span class="sxs-lookup"><span data-stu-id="b6e66-128">Encoding</span></span>

<span data-ttu-id="b6e66-129">L'API di codifica WIC è progettata per essere indipendente dal codec e pertanto la codifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="b6e66-129">The WIC encoding API are designed to be codec-independent and therefore image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="b6e66-130">Per ulteriori informazioni sulla codifica delle immagini tramite l'API WIC, vedere [Cenni preliminari sulla codifica](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="b6e66-130">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="b6e66-131">Opzioni del codificatore</span><span class="sxs-lookup"><span data-stu-id="b6e66-131">Encoder Options</span></span>

<span data-ttu-id="b6e66-132">I codec abilitati per WIC differiscono a livello di opzione di codifica.</span><span class="sxs-lookup"><span data-stu-id="b6e66-132">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="b6e66-133">Le opzioni del codificatore riflettono le funzionalità di un codificatore di immagini e ogni codec nativo supporta un set di queste opzioni del codificatore.</span><span class="sxs-lookup"><span data-stu-id="b6e66-133">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="b6e66-134">Le opzioni del codificatore possono essere opzioni supportate per WIC di base disponibili per tutti i codici abilitati per WIC (anche se non necessariamente supportati) o per le opzioni specifiche del codec progettate dal codec del formato di immagine.</span><span class="sxs-lookup"><span data-stu-id="b6e66-134">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="b6e66-135">Per gestire queste opzioni di codifica durante il processo di codifica, WIC utilizza l'interfaccia [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b6e66-135">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="b6e66-136">Per ulteriori informazioni sull'utilizzo dell'interfaccia **IPropertyBag2** per la codifica WIC, vedere [Cenni preliminari sulla codifica](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="b6e66-136">For more information about using the **IPropertyBag2** interface for WIC encoding see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="b6e66-137">Nella tabella seguente sono elencate le opzioni del codificatore WIC supportate dal codec BMP nativo.</span><span class="sxs-lookup"><span data-stu-id="b6e66-137">The following table lists the WIC encoder options supported by the native BMP codec.</span></span>



| <span data-ttu-id="b6e66-138">Nome della proprietà</span><span class="sxs-lookup"><span data-stu-id="b6e66-138">Property Name</span></span>               | <span data-ttu-id="b6e66-139">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="b6e66-139">VARTYPE</span></span>      | <span data-ttu-id="b6e66-140">Gamma valori</span><span class="sxs-lookup"><span data-stu-id="b6e66-140">Value Range</span></span>                      | <span data-ttu-id="b6e66-141">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="b6e66-141">Default Value</span></span>      |
|-----------------------------|--------------|----------------------------------|--------------------|
| <span data-ttu-id="b6e66-142">**EnableV5Header32bppBGRA**</span><span class="sxs-lookup"><span data-stu-id="b6e66-142">**EnableV5Header32bppBGRA**</span></span> | <span data-ttu-id="b6e66-143">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="b6e66-143">**VT\_BOOL**</span></span> | <span data-ttu-id="b6e66-144">**VARIANT \_ true/Variant \_ false**</span><span class="sxs-lookup"><span data-stu-id="b6e66-144">**VARIANT\_TRUE/VARIANT\_FALSE**</span></span> | <span data-ttu-id="b6e66-145">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="b6e66-145">**VARIANT\_FALSE**</span></span> |



 

### <a name="enablev5header32bppbgra"></a><span data-ttu-id="b6e66-146">EnableV5Header32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="b6e66-146">EnableV5Header32bppBGRA</span></span>

<span data-ttu-id="b6e66-147">Specifica se consentire la codifica dei dati nel \_ formato pixel WICPIXELFORMAT32BPPBGRA GUID.</span><span class="sxs-lookup"><span data-stu-id="b6e66-147">Specifies whether to allow encoding data in the GUID\_WICPixelFormat32bppBGRA pixel format.</span></span> <span data-ttu-id="b6e66-148">Se questa opzione è impostata su **Variant \_ true**, il formato BMP verrà scritto con un'intestazione BITMAPV5HEADER.</span><span class="sxs-lookup"><span data-stu-id="b6e66-148">If this option is set to **VARIANT\_TRUE**, the BMP will be written out with a BITMAPV5HEADER header.</span></span>

<span data-ttu-id="b6e66-149">Il valore predefinito è **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="b6e66-149">The default value is **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="b6e66-150">Se un'opzione del codificatore è presente nell'elenco di opzioni IPropertyBag2 che il codec non supporta, viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="b6e66-150">If an encoder option is present in the IPropertyBag2 option list that the codec does not support, it is ignored.</span></span>

<span data-ttu-id="b6e66-151">Nota per i file BMP Windows a 16 bit e a 32 bit, il codec BMP ignora qualsiasi canale alfa, in quanto molti file di immagine legacy contengono dati non validi in questo canale aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="b6e66-151">Note for 16-bit and 32-bit Windows BMP files, the BMP codec ignores any alpha channel, as many legacy image files contain invalid data in this extra channel.</span></span> <span data-ttu-id="b6e66-152">A partire da Windows 8, i file di Windows BMP a 32 bit scritti usando **BITMAPV5HEADER** con contenuto del canale alfa valido vengono letti come WICPixelFormat32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="b6e66-152">Starting with Windows 8, 32-bit Windows BMP files written using the **BITMAPV5HEADER** with valid alpha channel content are read as WICPixelFormat32bppBGRA</span></span>

## <a name="decoding"></a><span data-ttu-id="b6e66-153">Decodifica</span><span class="sxs-lookup"><span data-stu-id="b6e66-153">Decoding</span></span>

<span data-ttu-id="b6e66-154">L'API di decodifica WIC è progettata per essere indipendente dal codec e la decodifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="b6e66-154">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="b6e66-155">Per ulteriori informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="b6e66-155">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="b6e66-156">Per ulteriori informazioni sull'utilizzo di dati di immagine decodificati, vedere [Cenni preliminari sulle origini bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="b6e66-156">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
