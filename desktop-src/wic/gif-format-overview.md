---
description: In questo argomento vengono fornite informazioni sul codec GIF nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: CAEC8F92-8971-42B4-BED8-A6A93522D11E
title: Panoramica del formato GIF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f592b50300edf79c71ff4050a2c0d5aeba8b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232468"
---
# <a name="gif-format-overview"></a><span data-ttu-id="1fd7b-103">Panoramica del formato GIF</span><span class="sxs-lookup"><span data-stu-id="1fd7b-103">GIF Format Overview</span></span>

<span data-ttu-id="1fd7b-104">In questo argomento vengono fornite informazioni sul codec GIF nativo disponibile tramite Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="1fd7b-104">This topic provides information about the native GIF codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="1fd7b-105">Identità codec</span><span class="sxs-lookup"><span data-stu-id="1fd7b-105">Codec Identity</span></span>

<span data-ttu-id="1fd7b-106">Nella tabella seguente vengono fornite informazioni di identificazione del codec.</span><span class="sxs-lookup"><span data-stu-id="1fd7b-106">The following table provides codec identification information.</span></span>



|                        |                                       |
|------------------------|---------------------------------------|
| <span data-ttu-id="1fd7b-107">Nome/i formale/i</span><span class="sxs-lookup"><span data-stu-id="1fd7b-107">Formal Name(s)</span></span>         | <span data-ttu-id="1fd7b-108">Graphics Interchange Format 89a (GIF)</span><span class="sxs-lookup"><span data-stu-id="1fd7b-108">Graphics Interchange Format 89a (GIF)</span></span> |
| <span data-ttu-id="1fd7b-109">Estensioni del nome di file</span><span class="sxs-lookup"><span data-stu-id="1fd7b-109">File Name Extension(s)</span></span> | <span data-ttu-id="1fd7b-110">GIF</span><span class="sxs-lookup"><span data-stu-id="1fd7b-110">gif</span></span>                                   |
| <span data-ttu-id="1fd7b-111">tipo MIME</span><span class="sxs-lookup"><span data-stu-id="1fd7b-111">MIME type</span></span>              | <span data-ttu-id="1fd7b-112">image/gif</span><span class="sxs-lookup"><span data-stu-id="1fd7b-112">image/gif</span></span>                             |
| <span data-ttu-id="1fd7b-113">Supporto delle specifiche</span><span class="sxs-lookup"><span data-stu-id="1fd7b-113">Specification Support</span></span>  | <span data-ttu-id="1fd7b-114">Specifica GIF 89a/89m</span><span class="sxs-lookup"><span data-stu-id="1fd7b-114">GIF Specification 89a/89m</span></span>             |



 

<span data-ttu-id="1fd7b-115">La tabella seguente elenca i GUID usati per identificare i componenti dei codec GIF nativi.</span><span class="sxs-lookup"><span data-stu-id="1fd7b-115">The following table lists the GUIDs used to identify the native GIF codec components.</span></span>



| <span data-ttu-id="1fd7b-116">Componente</span><span class="sxs-lookup"><span data-stu-id="1fd7b-116">Component</span></span>        | <span data-ttu-id="1fd7b-117">Nome descrittivo</span><span class="sxs-lookup"><span data-stu-id="1fd7b-117">Friendly Name</span></span>            | <span data-ttu-id="1fd7b-118">GUID</span><span class="sxs-lookup"><span data-stu-id="1fd7b-118">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="1fd7b-119">Formato contenitore</span><span class="sxs-lookup"><span data-stu-id="1fd7b-119">Container Format</span></span> | <span data-ttu-id="1fd7b-120">GUID \_ ContainerFormatGif</span><span class="sxs-lookup"><span data-stu-id="1fd7b-120">GUID\_ContainerFormatGif</span></span> | <span data-ttu-id="1fd7b-121">1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5</span><span class="sxs-lookup"><span data-stu-id="1fd7b-121">1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5</span></span> |
| <span data-ttu-id="1fd7b-122">Decodificatore</span><span class="sxs-lookup"><span data-stu-id="1fd7b-122">Decoder</span></span>          | <span data-ttu-id="1fd7b-123">\_WICGIFDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="1fd7b-123">CLSID\_WICGifDecoder</span></span>     | <span data-ttu-id="1fd7b-124">381dda3c-9ce9-4834-a23e1f98f8fc52be</span><span class="sxs-lookup"><span data-stu-id="1fd7b-124">381dda3c-9ce9-4834-a23e1f98f8fc52be</span></span> |
| <span data-ttu-id="1fd7b-125">Codificatore</span><span class="sxs-lookup"><span data-stu-id="1fd7b-125">Encoder</span></span>          | <span data-ttu-id="1fd7b-126">\_WICGIFENCODER CLSID</span><span class="sxs-lookup"><span data-stu-id="1fd7b-126">CLSID\_WICGifEncoder</span></span>     | <span data-ttu-id="1fd7b-127">114f5598-0b22-40a0-86a1c83ea495adbd</span><span class="sxs-lookup"><span data-stu-id="1fd7b-127">114f5598-0b22-40a0-86a1c83ea495adbd</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="1fd7b-128">Codifica</span><span class="sxs-lookup"><span data-stu-id="1fd7b-128">Encoding</span></span>

<span data-ttu-id="1fd7b-129">L'API di codifica WIC è progettata per essere indipendente dal codec e la codifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="1fd7b-129">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="1fd7b-130">Per ulteriori informazioni sulla codifica delle immagini tramite l'API WIC, vedere [Cenni preliminari sulla codifica](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="1fd7b-130">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="1fd7b-131">Opzioni del codificatore</span><span class="sxs-lookup"><span data-stu-id="1fd7b-131">Encoder Options</span></span>

<span data-ttu-id="1fd7b-132">I codec abilitati per WIC differiscono a livello di opzione di codifica.</span><span class="sxs-lookup"><span data-stu-id="1fd7b-132">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="1fd7b-133">Le opzioni del codificatore riflettono le funzionalità di un codificatore di immagini e ogni codec nativo supporta un set di queste opzioni del codificatore.</span><span class="sxs-lookup"><span data-stu-id="1fd7b-133">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="1fd7b-134">Le opzioni del codificatore possono essere opzioni supportate per WIC di base disponibili per tutti i codici abilitati per WIC (anche se non necessariamente supportati) o per le opzioni specifiche del codec progettate dal codec del formato di immagine.</span><span class="sxs-lookup"><span data-stu-id="1fd7b-134">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="1fd7b-135">Per gestire queste opzioni di codifica durante il processo di codifica, WIC utilizza l'interfaccia [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1fd7b-135">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="1fd7b-136">Per ulteriori informazioni sull'utilizzo dell'interfaccia **IPropertyBag2** per la codifica WIC, vedere [Cenni preliminari sulla codifica](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="1fd7b-136">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="1fd7b-137">Il codificatore GIF non supporta le opzioni WIC di base e non fornisce opzioni del codificatore personalizzate.</span><span class="sxs-lookup"><span data-stu-id="1fd7b-137">The GIF encoder does not support any basic WIC options and does not provide custom encoder options.</span></span> <span data-ttu-id="1fd7b-138">Se un'opzione del codificatore è presente nell'elenco di opzioni [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) , viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="1fd7b-138">If an encoder option is in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list, it is ignored.</span></span>

## <a name="decoding"></a><span data-ttu-id="1fd7b-139">Decodifica</span><span class="sxs-lookup"><span data-stu-id="1fd7b-139">Decoding</span></span>

<span data-ttu-id="1fd7b-140">L'API di decodifica WIC è progettata per essere indipendente dal codec e la decodifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="1fd7b-140">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="1fd7b-141">Per ulteriori informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="1fd7b-141">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="1fd7b-142">Per ulteriori informazioni sull'utilizzo di dati di immagine decodificati, vedere [Cenni preliminari sulle origini bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="1fd7b-142">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
