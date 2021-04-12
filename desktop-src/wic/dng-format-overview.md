---
description: Questo argomento fornisce informazioni sul codec DNG nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: 6F87A47D-E54A-42D9-92DC-2411803278AA
title: Panoramica sul formato DNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f766356f7c13d7b2bb25adab5411ae55c2735f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345816"
---
# <a name="dng-format-overview"></a><span data-ttu-id="2dc95-103">Panoramica sul formato DNG</span><span class="sxs-lookup"><span data-stu-id="2dc95-103">DNG Format Overview</span></span>

<span data-ttu-id="2dc95-104">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="2dc95-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2dc95-105">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="2dc95-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2dc95-106">Questo argomento fornisce informazioni sul codec DNG nativo disponibile tramite Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="2dc95-106">This topic provides information about the native DNG codec available through Windows Imaging Component (WIC).</span></span>

-   [<span data-ttu-id="2dc95-107">Identità codec</span><span class="sxs-lookup"><span data-stu-id="2dc95-107">Codec Identity</span></span>](#codec-identity)
-   [<span data-ttu-id="2dc95-108">Decodifica</span><span class="sxs-lookup"><span data-stu-id="2dc95-108">Decoding</span></span>](#decoding)

## <a name="codec-identity"></a><span data-ttu-id="2dc95-109">Identità codec</span><span class="sxs-lookup"><span data-stu-id="2dc95-109">Codec Identity</span></span>

<span data-ttu-id="2dc95-110">Nella tabella seguente vengono fornite informazioni di identificazione del codec.</span><span class="sxs-lookup"><span data-stu-id="2dc95-110">The following table provides codec identification information.</span></span>



|                        |                                                      |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="2dc95-111">Nome/i formale/i</span><span class="sxs-lookup"><span data-stu-id="2dc95-111">Formal Name(s)</span></span>         | <span data-ttu-id="2dc95-112">Negativo digitale (DNG)</span><span class="sxs-lookup"><span data-stu-id="2dc95-112">Digital Negative (DNG)</span></span>                               |
| <span data-ttu-id="2dc95-113">Estensioni del nome di file</span><span class="sxs-lookup"><span data-stu-id="2dc95-113">File Name Extension(s)</span></span> | <span data-ttu-id="2dc95-114">.dng</span><span class="sxs-lookup"><span data-stu-id="2dc95-114">.dng</span></span>                                                 |
| <span data-ttu-id="2dc95-115">Tipi MIME</span><span class="sxs-lookup"><span data-stu-id="2dc95-115">MIME type(s)</span></span>           | <span data-ttu-id="2dc95-116">Image/DNG</span><span class="sxs-lookup"><span data-stu-id="2dc95-116">image/DNG</span></span>                                            |
| <span data-ttu-id="2dc95-117">Supporto delle specifiche</span><span class="sxs-lookup"><span data-stu-id="2dc95-117">Specification Support</span></span>  | <span data-ttu-id="2dc95-118">Versione della specifica digitale negativa (DNG) 1.4.0.0</span><span class="sxs-lookup"><span data-stu-id="2dc95-118">Digital Negative (DNG) Specification Version 1.4.0.0</span></span> |



 

<span data-ttu-id="2dc95-119">La tabella seguente elenca i GUID usati per identificare i componenti dei codec DNG nativi.</span><span class="sxs-lookup"><span data-stu-id="2dc95-119">The following table lists the GUIDs used to identify the native DNG codec components.</span></span>



| <span data-ttu-id="2dc95-120">Componente</span><span class="sxs-lookup"><span data-stu-id="2dc95-120">Component</span></span>        | <span data-ttu-id="2dc95-121">Nome descrittivo</span><span class="sxs-lookup"><span data-stu-id="2dc95-121">Friendly Name</span></span>             | <span data-ttu-id="2dc95-122">GUID</span><span class="sxs-lookup"><span data-stu-id="2dc95-122">GUID</span></span>                                |
|------------------|---------------------------|-------------------------------------|
| <span data-ttu-id="2dc95-123">Formato contenitore</span><span class="sxs-lookup"><span data-stu-id="2dc95-123">Container Format</span></span> | <span data-ttu-id="2dc95-124">GUID \_ ContainerFormatAdng</span><span class="sxs-lookup"><span data-stu-id="2dc95-124">GUID\_ContainerFormatAdng</span></span> | <span data-ttu-id="2dc95-125">f3ff6d0d-38c0-41c4-b1fe1f3824f17b84</span><span class="sxs-lookup"><span data-stu-id="2dc95-125">f3ff6d0d-38c0-41c4-b1fe1f3824f17b84</span></span> |
| <span data-ttu-id="2dc95-126">Decodificatore</span><span class="sxs-lookup"><span data-stu-id="2dc95-126">Decoder</span></span>          | <span data-ttu-id="2dc95-127">\_WICADNGDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="2dc95-127">CLSID\_WICAdngDecoder</span></span>     | <span data-ttu-id="2dc95-128">981d9411-909e-42a7-8f5da747ff052edb</span><span class="sxs-lookup"><span data-stu-id="2dc95-128">981d9411-909e-42a7-8f5da747ff052edb</span></span> |



 

## <a name="decoding"></a><span data-ttu-id="2dc95-129">Decodifica</span><span class="sxs-lookup"><span data-stu-id="2dc95-129">Decoding</span></span>

<span data-ttu-id="2dc95-130">L'API di decodifica WIC è progettata per essere indipendente dal codec e la decodifica delle immagini per i codec compatibili con WIC è sostanzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="2dc95-130">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="2dc95-131">Per ulteriori informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="2dc95-131">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="2dc95-132">Per ulteriori informazioni sull'utilizzo di dati di immagine decodificati, vedere [Cenni preliminari sulle origini bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="2dc95-132">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="2dc95-133">Il decodificatore non supporta la decodifica dei dati dei sensori non elaborati e supporta solo i file con una rappresentazione di immagine non RAW incorporata in un IFD con NewSubFileType uguale a 1.</span><span class="sxs-lookup"><span data-stu-id="2dc95-133">The decoder does not support decoding raw sensor data and only supports files with a non-raw image representation embedded in an IFD with NewSubFileType equal to 1.</span></span>

 

 



