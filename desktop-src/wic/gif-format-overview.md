---
description: In questo argomento vengono fornite informazioni sul codec GIF nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: CAEC8F92-8971-42B4-BED8-A6A93522D11E
title: Panoramica del formato GIF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddf7e9924c921b7944de114f5fe667cb2aa33cae
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444452"
---
# <a name="gif-format-overview"></a><span data-ttu-id="e53ab-103">Panoramica del formato GIF</span><span class="sxs-lookup"><span data-stu-id="e53ab-103">GIF Format Overview</span></span>

<span data-ttu-id="e53ab-104">In questo argomento vengono fornite informazioni sul codec GIF nativo disponibile tramite Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="e53ab-104">This topic provides information about the native GIF codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="e53ab-105">Identità codec</span><span class="sxs-lookup"><span data-stu-id="e53ab-105">Codec Identity</span></span>

<span data-ttu-id="e53ab-106">Nella tabella seguente vengono fornite informazioni di identificazione dei codec.</span><span class="sxs-lookup"><span data-stu-id="e53ab-106">The following table provides codec identification information.</span></span>



|  <span data-ttu-id="e53ab-107">Componente</span><span class="sxs-lookup"><span data-stu-id="e53ab-107">Component</span></span>             | <span data-ttu-id="e53ab-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e53ab-108">Description</span></span>                           |
|------------------------|---------------------------------------|
| <span data-ttu-id="e53ab-109">Nomi formali</span><span class="sxs-lookup"><span data-stu-id="e53ab-109">Formal Name(s)</span></span>         | <span data-ttu-id="e53ab-110">Graphics Interchange Format 89a (GIF)</span><span class="sxs-lookup"><span data-stu-id="e53ab-110">Graphics Interchange Format 89a (GIF)</span></span> |
| <span data-ttu-id="e53ab-111">Estensioni di file</span><span class="sxs-lookup"><span data-stu-id="e53ab-111">File Name Extension(s)</span></span> | <span data-ttu-id="e53ab-112">GIF</span><span class="sxs-lookup"><span data-stu-id="e53ab-112">gif</span></span>                                   |
| <span data-ttu-id="e53ab-113">tipo MIME</span><span class="sxs-lookup"><span data-stu-id="e53ab-113">MIME type</span></span>              | <span data-ttu-id="e53ab-114">image/gif</span><span class="sxs-lookup"><span data-stu-id="e53ab-114">image/gif</span></span>                             |
| <span data-ttu-id="e53ab-115">Supporto delle specifiche</span><span class="sxs-lookup"><span data-stu-id="e53ab-115">Specification Support</span></span>  | <span data-ttu-id="e53ab-116">Specifica GIF 89a/89m</span><span class="sxs-lookup"><span data-stu-id="e53ab-116">GIF Specification 89a/89m</span></span>             |



 

<span data-ttu-id="e53ab-117">Nella tabella seguente sono elencati i GUID usati per identificare i componenti del codec GIF nativo.</span><span class="sxs-lookup"><span data-stu-id="e53ab-117">The following table lists the GUIDs used to identify the native GIF codec components.</span></span>



| <span data-ttu-id="e53ab-118">Componente</span><span class="sxs-lookup"><span data-stu-id="e53ab-118">Component</span></span>        | <span data-ttu-id="e53ab-119">Nome descrittivo</span><span class="sxs-lookup"><span data-stu-id="e53ab-119">Friendly Name</span></span>            | <span data-ttu-id="e53ab-120">GUID</span><span class="sxs-lookup"><span data-stu-id="e53ab-120">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="e53ab-121">Formato contenitore</span><span class="sxs-lookup"><span data-stu-id="e53ab-121">Container Format</span></span> | <span data-ttu-id="e53ab-122">GUID \_ ContainerFormatGif</span><span class="sxs-lookup"><span data-stu-id="e53ab-122">GUID\_ContainerFormatGif</span></span> | <span data-ttu-id="e53ab-123">1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5</span><span class="sxs-lookup"><span data-stu-id="e53ab-123">1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5</span></span> |
| <span data-ttu-id="e53ab-124">Decodificatore</span><span class="sxs-lookup"><span data-stu-id="e53ab-124">Decoder</span></span>          | <span data-ttu-id="e53ab-125">CLSID \_ WICGifDecoder</span><span class="sxs-lookup"><span data-stu-id="e53ab-125">CLSID\_WICGifDecoder</span></span>     | <span data-ttu-id="e53ab-126">381dda3c-9ce9-4834-a23e1f98f8fc52be</span><span class="sxs-lookup"><span data-stu-id="e53ab-126">381dda3c-9ce9-4834-a23e1f98f8fc52be</span></span> |
| <span data-ttu-id="e53ab-127">Codificatore</span><span class="sxs-lookup"><span data-stu-id="e53ab-127">Encoder</span></span>          | <span data-ttu-id="e53ab-128">CLSID \_ WICGifEncoder</span><span class="sxs-lookup"><span data-stu-id="e53ab-128">CLSID\_WICGifEncoder</span></span>     | <span data-ttu-id="e53ab-129">114f5598-0b22-40a0-86a1c83ea495adbd</span><span class="sxs-lookup"><span data-stu-id="e53ab-129">114f5598-0b22-40a0-86a1c83ea495adbd</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="e53ab-130">Codifica</span><span class="sxs-lookup"><span data-stu-id="e53ab-130">Encoding</span></span>

<span data-ttu-id="e53ab-131">L'API di codifica WIC è progettata per essere indipendente dai codec e la codifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="e53ab-131">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="e53ab-132">Per altre informazioni sulla codifica delle immagini tramite l'API WIC, vedere Cenni [preliminari sulla codifica](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="e53ab-132">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="e53ab-133">Opzioni del codificatore</span><span class="sxs-lookup"><span data-stu-id="e53ab-133">Encoder Options</span></span>

<span data-ttu-id="e53ab-134">I codec abilitati per WIC differiscono a livello di opzione di codifica.</span><span class="sxs-lookup"><span data-stu-id="e53ab-134">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="e53ab-135">Le opzioni del codificatore riflettono le funzionalità di un codificatore di immagini e ogni codec nativo supporta un set di queste opzioni del codificatore.</span><span class="sxs-lookup"><span data-stu-id="e53ab-135">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="e53ab-136">Le opzioni del codificatore possono essere opzioni di base supportate da WIC disponibili per tutti i codici abilitati per WIC (anche se non necessariamente supportate) o opzioni specifiche del codec progettate dal codec del formato immagine.</span><span class="sxs-lookup"><span data-stu-id="e53ab-136">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="e53ab-137">Per gestire queste opzioni di codifica durante il processo di codifica, WIC usa [**l'interfaccia IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e53ab-137">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="e53ab-138">Per altre informazioni sull'uso **dell'interfaccia IPropertyBag2** per la codifica WIC, vedere Cenni [preliminari sulla codifica](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="e53ab-138">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="e53ab-139">Il codificatore GIF non supporta opzioni WIC di base e non fornisce opzioni personalizzate per il codificatore.</span><span class="sxs-lookup"><span data-stu-id="e53ab-139">The GIF encoder does not support any basic WIC options and does not provide custom encoder options.</span></span> <span data-ttu-id="e53ab-140">Se un'opzione del codificatore si trova nell'elenco di opzioni [**IPropertyBag2,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="e53ab-140">If an encoder option is in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list, it is ignored.</span></span>

## <a name="decoding"></a><span data-ttu-id="e53ab-141">Decodifica</span><span class="sxs-lookup"><span data-stu-id="e53ab-141">Decoding</span></span>

<span data-ttu-id="e53ab-142">L'API di decodifica WIC è progettata per essere indipendente dal codec e la decodifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="e53ab-142">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="e53ab-143">Per altre informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="e53ab-143">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="e53ab-144">Per altre informazioni sull'uso di dati immagine decodificati, vedere Panoramica [delle origini bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="e53ab-144">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
