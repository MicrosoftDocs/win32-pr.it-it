---
description: In questo argomento vengono fornite informazioni sul codec DNG nativo disponibile tramite Windows Imaging Component (WIC).
ms.assetid: 6F87A47D-E54A-42D9-92DC-2411803278AA
title: Panoramica del formato DNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0815d6a24bb8e57e6c64b90f9e9068765838e148
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444932"
---
# <a name="dng-format-overview"></a><span data-ttu-id="d33f7-103">Panoramica del formato DNG</span><span class="sxs-lookup"><span data-stu-id="d33f7-103">DNG Format Overview</span></span>

<span data-ttu-id="d33f7-104">\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio.</span><span class="sxs-lookup"><span data-stu-id="d33f7-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d33f7-105">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="d33f7-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d33f7-106">In questo argomento vengono fornite informazioni sul codec DNG nativo disponibile tramite Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="d33f7-106">This topic provides information about the native DNG codec available through Windows Imaging Component (WIC).</span></span>

-   [<span data-ttu-id="d33f7-107">Codec Identity</span><span class="sxs-lookup"><span data-stu-id="d33f7-107">Codec Identity</span></span>](#codec-identity)
-   [<span data-ttu-id="d33f7-108">Decodifica</span><span class="sxs-lookup"><span data-stu-id="d33f7-108">Decoding</span></span>](#decoding)

## <a name="codec-identity"></a><span data-ttu-id="d33f7-109">Codec Identity</span><span class="sxs-lookup"><span data-stu-id="d33f7-109">Codec Identity</span></span>

<span data-ttu-id="d33f7-110">Nella tabella seguente vengono fornite informazioni di identificazione del codec.</span><span class="sxs-lookup"><span data-stu-id="d33f7-110">The following table provides codec identification information.</span></span>



|     <span data-ttu-id="d33f7-111">Componente</span><span class="sxs-lookup"><span data-stu-id="d33f7-111">Component</span></span>          |  <span data-ttu-id="d33f7-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d33f7-112">Description</span></span>                                         |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="d33f7-113">Nomi formali</span><span class="sxs-lookup"><span data-stu-id="d33f7-113">Formal Name(s)</span></span>         | <span data-ttu-id="d33f7-114">Digital Negative (DNG)</span><span class="sxs-lookup"><span data-stu-id="d33f7-114">Digital Negative (DNG)</span></span>                               |
| <span data-ttu-id="d33f7-115">Estensioni di file</span><span class="sxs-lookup"><span data-stu-id="d33f7-115">File Name Extension(s)</span></span> | <span data-ttu-id="d33f7-116">.dng</span><span class="sxs-lookup"><span data-stu-id="d33f7-116">.dng</span></span>                                                 |
| <span data-ttu-id="d33f7-117">Tipi MIME</span><span class="sxs-lookup"><span data-stu-id="d33f7-117">MIME type(s)</span></span>           | <span data-ttu-id="d33f7-118">image/DNG</span><span class="sxs-lookup"><span data-stu-id="d33f7-118">image/DNG</span></span>                                            |
| <span data-ttu-id="d33f7-119">Supporto delle specifiche</span><span class="sxs-lookup"><span data-stu-id="d33f7-119">Specification Support</span></span>  | <span data-ttu-id="d33f7-120">Digital Negative (DNG) Specification Version 1.4.0.0</span><span class="sxs-lookup"><span data-stu-id="d33f7-120">Digital Negative (DNG) Specification Version 1.4.0.0</span></span> |



 

<span data-ttu-id="d33f7-121">Nella tabella seguente sono elencati i GUID utilizzati per identificare i componenti nativi del codec DNG.</span><span class="sxs-lookup"><span data-stu-id="d33f7-121">The following table lists the GUIDs used to identify the native DNG codec components.</span></span>



| <span data-ttu-id="d33f7-122">Componente</span><span class="sxs-lookup"><span data-stu-id="d33f7-122">Component</span></span>        | <span data-ttu-id="d33f7-123">Nome descrittivo</span><span class="sxs-lookup"><span data-stu-id="d33f7-123">Friendly Name</span></span>             | <span data-ttu-id="d33f7-124">GUID</span><span class="sxs-lookup"><span data-stu-id="d33f7-124">GUID</span></span>                                |
|------------------|---------------------------|-------------------------------------|
| <span data-ttu-id="d33f7-125">Formato contenitore</span><span class="sxs-lookup"><span data-stu-id="d33f7-125">Container Format</span></span> | <span data-ttu-id="d33f7-126">GUID \_ ContainerFormatAdng</span><span class="sxs-lookup"><span data-stu-id="d33f7-126">GUID\_ContainerFormatAdng</span></span> | <span data-ttu-id="d33f7-127">f3ff6d0d-38c0-41c4-b1fe1f3824f17b84</span><span class="sxs-lookup"><span data-stu-id="d33f7-127">f3ff6d0d-38c0-41c4-b1fe1f3824f17b84</span></span> |
| <span data-ttu-id="d33f7-128">Decodificatore</span><span class="sxs-lookup"><span data-stu-id="d33f7-128">Decoder</span></span>          | <span data-ttu-id="d33f7-129">CLSID \_ WICAdngDecoder</span><span class="sxs-lookup"><span data-stu-id="d33f7-129">CLSID\_WICAdngDecoder</span></span>     | <span data-ttu-id="d33f7-130">981d9411-909e-42a7-8f5da747ff052edb</span><span class="sxs-lookup"><span data-stu-id="d33f7-130">981d9411-909e-42a7-8f5da747ff052edb</span></span> |



 

## <a name="decoding"></a><span data-ttu-id="d33f7-131">Decodifica</span><span class="sxs-lookup"><span data-stu-id="d33f7-131">Decoding</span></span>

<span data-ttu-id="d33f7-132">L'API di decodifica WIC è progettata per essere indipendente dal codec e la decodifica delle immagini per i codec abilitati per WIC è essenzialmente la stessa.</span><span class="sxs-lookup"><span data-stu-id="d33f7-132">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="d33f7-133">Per altre informazioni sulla decodifica delle immagini, vedere [Cenni preliminari sulla decodifica.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="d33f7-133">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="d33f7-134">Per altre informazioni sull'uso di dati di immagine decodificati, vedere Cenni [preliminari sulle origini bitmap.](-wic-bitmapsources.md)</span><span class="sxs-lookup"><span data-stu-id="d33f7-134">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="d33f7-135">Il decodificatore non supporta la decodifica dei dati dei sensori non elaborati e supporta solo i file con una rappresentazione di immagine non non elaborata incorporata in un IFD con NewSubFileType uguale a 1.</span><span class="sxs-lookup"><span data-stu-id="d33f7-135">The decoder does not support decoding raw sensor data and only supports files with a non-raw image representation embedded in an IFD with NewSubFileType equal to 1.</span></span>

 

 



