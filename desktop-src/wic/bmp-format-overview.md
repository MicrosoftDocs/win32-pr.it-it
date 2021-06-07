---
description: In questo argomento vengono fornite informazioni sul codec BMP nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: 85AC5A30-A915-439E-A10F-B2833DDA995C
title: Panoramica del formato BMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1975f27af5b731ed1f62f3571109553848705239
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444962"
---
# <a name="bmp-format-overview"></a><span data-ttu-id="b4569-103">Panoramica del formato BMP</span><span class="sxs-lookup"><span data-stu-id="b4569-103">BMP Format Overview</span></span>

<span data-ttu-id="b4569-104">In questo argomento vengono fornite informazioni sul codec BMP nativo disponibile tramite Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="b4569-104">This topic provides information about the native BMP codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="b4569-105">Identità codec</span><span class="sxs-lookup"><span data-stu-id="b4569-105">Codec Identity</span></span>

<span data-ttu-id="b4569-106">Nella tabella seguente vengono fornite informazioni di identificazione dei codec.</span><span class="sxs-lookup"><span data-stu-id="b4569-106">The following table provides codec identification information.</span></span>



| <span data-ttu-id="b4569-107">Componente</span><span class="sxs-lookup"><span data-stu-id="b4569-107">Component</span></span>              | <span data-ttu-id="b4569-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4569-108">Description</span></span>           |
|------------------------|-----------------------|
| <span data-ttu-id="b4569-109">Nomi formali</span><span class="sxs-lookup"><span data-stu-id="b4569-109">Formal Name(s)</span></span>         | <span data-ttu-id="b4569-110">Formato bitmap di Windows</span><span class="sxs-lookup"><span data-stu-id="b4569-110">Windows Bitmap Format</span></span> |
| <span data-ttu-id="b4569-111">Estensioni di file</span><span class="sxs-lookup"><span data-stu-id="b4569-111">File Name Extension(s)</span></span> | <span data-ttu-id="b4569-112">bmp, dib</span><span class="sxs-lookup"><span data-stu-id="b4569-112">bmp, dib</span></span>              |
| <span data-ttu-id="b4569-113">tipo MIME</span><span class="sxs-lookup"><span data-stu-id="b4569-113">MIME type</span></span>              | <span data-ttu-id="b4569-114">image/bmp</span><span class="sxs-lookup"><span data-stu-id="b4569-114">image/bmp</span></span>             |
| <span data-ttu-id="b4569-115">Supporto delle specifiche</span><span class="sxs-lookup"><span data-stu-id="b4569-115">Specification Support</span></span>  | <span data-ttu-id="b4569-116">Specifica BMP v5</span><span class="sxs-lookup"><span data-stu-id="b4569-116">BMP Specification v5</span></span>  |



 

<span data-ttu-id="b4569-117">Nella tabella seguente sono elencati i GUID usati per identificare i componenti nativi del codec BMP.</span><span class="sxs-lookup"><span data-stu-id="b4569-117">The following table lists the GUIDs used to identify the native BMP codec components.</span></span>



| <span data-ttu-id="b4569-118">Componente</span><span class="sxs-lookup"><span data-stu-id="b4569-118">Component</span></span>        | <span data-ttu-id="b4569-119">Nome descrittivo</span><span class="sxs-lookup"><span data-stu-id="b4569-119">Friendly Name</span></span>            | <span data-ttu-id="b4569-120">GUID</span><span class="sxs-lookup"><span data-stu-id="b4569-120">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="b4569-121">Formato contenitore</span><span class="sxs-lookup"><span data-stu-id="b4569-121">Container Format</span></span> | <span data-ttu-id="b4569-122">GUID \_ ContainerFormatBmp</span><span class="sxs-lookup"><span data-stu-id="b4569-122">GUID\_ContainerFormatBmp</span></span> | <span data-ttu-id="b4569-123">0af1d87e-fcfe-4188-bdeba7906471cbe3</span><span class="sxs-lookup"><span data-stu-id="b4569-123">0af1d87e-fcfe-4188-bdeba7906471cbe3</span></span> |
| <span data-ttu-id="b4569-124">Decodificatore</span><span class="sxs-lookup"><span data-stu-id="b4569-124">Decoder</span></span>          | <span data-ttu-id="b4569-125">CLSID \_ WICBmpDecoder</span><span class="sxs-lookup"><span data-stu-id="b4569-125">CLSID\_WICBmpDecoder</span></span>     | <span data-ttu-id="b4569-126">6b462062-7cbf-400d-9fdb813dd10f2778</span><span class="sxs-lookup"><span data-stu-id="b4569-126">6b462062-7cbf-400d-9fdb813dd10f2778</span></span> |
| <span data-ttu-id="b4569-127">Codificatore</span><span class="sxs-lookup"><span data-stu-id="b4569-127">Encoder</span></span>          | <span data-ttu-id="b4569-128">CLSID \_ WICBmpEncoder</span><span class="sxs-lookup"><span data-stu-id="b4569-128">CLSID\_WICBmpEncoder</span></span>     | <span data-ttu-id="b4569-129">69be8bb4-d66d-47c8-865aed1589433782</span><span class="sxs-lookup"><span data-stu-id="b4569-129">69be8bb4-d66d-47c8-865aed1589433782</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="b4569-130">Codifica</span><span class="sxs-lookup"><span data-stu-id="b4569-130">Encoding</span></span>

<span data-ttu-id="b4569-131">L'API di codifica WIC è progettata per essere indipendente dal codec e pertanto la codifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="b4569-131">The WIC encoding API are designed to be codec-independent and therefore image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="b4569-132">Per altre informazioni sulla codifica delle immagini tramite l'API WIC, vedere Cenni [preliminari sulla codifica](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="b4569-132">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="b4569-133">Opzioni del codificatore</span><span class="sxs-lookup"><span data-stu-id="b4569-133">Encoder Options</span></span>

<span data-ttu-id="b4569-134">I codec abilitati per WIC differiscono a livello di opzione di codifica.</span><span class="sxs-lookup"><span data-stu-id="b4569-134">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="b4569-135">Le opzioni del codificatore riflettono le funzionalità di un codificatore di immagini e ogni codec nativo supporta un set di queste opzioni del codificatore.</span><span class="sxs-lookup"><span data-stu-id="b4569-135">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="b4569-136">Le opzioni del codificatore possono essere opzioni di base supportate da WIC disponibili per tutti i codici abilitati per WIC (anche se non necessariamente supportate) o opzioni specifiche del codec progettate dal codec del formato immagine.</span><span class="sxs-lookup"><span data-stu-id="b4569-136">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="b4569-137">Per gestire queste opzioni di codifica durante il processo di codifica, WIC usa [**l'interfaccia IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b4569-137">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="b4569-138">Per altre informazioni sull'uso **dell'interfaccia IPropertyBag2** per la codifica WIC, vedere Cenni [preliminari sulla codifica](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="b4569-138">For more information about using the **IPropertyBag2** interface for WIC encoding see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="b4569-139">Nella tabella seguente sono elencate le opzioni del codificatore WIC supportate dal codec BMP nativo.</span><span class="sxs-lookup"><span data-stu-id="b4569-139">The following table lists the WIC encoder options supported by the native BMP codec.</span></span>



| <span data-ttu-id="b4569-140">Nome della proprietà</span><span class="sxs-lookup"><span data-stu-id="b4569-140">Property Name</span></span>               | <span data-ttu-id="b4569-141">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="b4569-141">VARTYPE</span></span>      | <span data-ttu-id="b4569-142">Gamma valori</span><span class="sxs-lookup"><span data-stu-id="b4569-142">Value Range</span></span>                      | <span data-ttu-id="b4569-143">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="b4569-143">Default Value</span></span>      |
|-----------------------------|--------------|----------------------------------|--------------------|
| <span data-ttu-id="b4569-144">**EnableV5Header32bppBGRA**</span><span class="sxs-lookup"><span data-stu-id="b4569-144">**EnableV5Header32bppBGRA**</span></span> | <span data-ttu-id="b4569-145">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="b4569-145">**VT\_BOOL**</span></span> | <span data-ttu-id="b4569-146">**VARIANT \_ TRUE/VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="b4569-146">**VARIANT\_TRUE/VARIANT\_FALSE**</span></span> | <span data-ttu-id="b4569-147">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="b4569-147">**VARIANT\_FALSE**</span></span> |



 

### <a name="enablev5header32bppbgra"></a><span data-ttu-id="b4569-148">EnableV5Header32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="b4569-148">EnableV5Header32bppBGRA</span></span>

<span data-ttu-id="b4569-149">Specifica se consentire la codifica dei dati nel formato pixel \_ GUID WICPixelFormat32bppBGRA.</span><span class="sxs-lookup"><span data-stu-id="b4569-149">Specifies whether to allow encoding data in the GUID\_WICPixelFormat32bppBGRA pixel format.</span></span> <span data-ttu-id="b4569-150">Se questa opzione è impostata su **VARIANT \_ TRUE,** il BMP verrà scritto con un'intestazione BITMAPV5HEADER.</span><span class="sxs-lookup"><span data-stu-id="b4569-150">If this option is set to **VARIANT\_TRUE**, the BMP will be written out with a BITMAPV5HEADER header.</span></span>

<span data-ttu-id="b4569-151">Il valore predefinito è **VARIANT \_ FALSE.**</span><span class="sxs-lookup"><span data-stu-id="b4569-151">The default value is **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="b4569-152">Se un'opzione del codificatore è presente nell'elenco di opzioni IPropertyBag2 non supportato dal codec, viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="b4569-152">If an encoder option is present in the IPropertyBag2 option list that the codec does not support, it is ignored.</span></span>

<span data-ttu-id="b4569-153">Nota per i file BMP di Windows a 16 e 32 bit, il codec BMP ignora qualsiasi canale alfa, poiché molti file di immagine legacy contengono dati non validi in questo canale aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="b4569-153">Note for 16-bit and 32-bit Windows BMP files, the BMP codec ignores any alpha channel, as many legacy image files contain invalid data in this extra channel.</span></span> <span data-ttu-id="b4569-154">A partire da Windows 8, i file BMP di Windows a 32 bit scritti usando **BITMAPV5HEADER** con contenuto del canale alfa valido vengono letti come WICPixelFormat32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="b4569-154">Starting with Windows 8, 32-bit Windows BMP files written using the **BITMAPV5HEADER** with valid alpha channel content are read as WICPixelFormat32bppBGRA</span></span>

## <a name="decoding"></a><span data-ttu-id="b4569-155">Decodifica</span><span class="sxs-lookup"><span data-stu-id="b4569-155">Decoding</span></span>

<span data-ttu-id="b4569-156">L'API di decodifica WIC è progettata per essere indipendente dal codec e la decodifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="b4569-156">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="b4569-157">Per altre informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="b4569-157">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="b4569-158">Per altre informazioni sull'uso di dati immagine decodificati, vedere Panoramica [delle origini bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="b4569-158">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
