---
description: Interfacce del decodificatore
ms.assetid: b88517cc-06fe-4d83-a6a9-76e1f34293f4
title: Interfacce del decodificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef90ca2dd521c15460295505a6d5b7ea451c4dba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233541"
---
# <a name="decoder-interfaces"></a><span data-ttu-id="0d045-103">Interfacce del decodificatore</span><span class="sxs-lookup"><span data-stu-id="0d045-103">Decoder Interfaces</span></span>

<span data-ttu-id="0d045-104">Nelle tabelle seguenti sono illustrate le interfacce implementate dai decodificatori di Windows Imaging Component (WIC) e il diagramma classi Mostra la gerarchia di ereditarietà.</span><span class="sxs-lookup"><span data-stu-id="0d045-104">The following tables show the interfaces implemented by Windows Imaging Component (WIC) decoders, and the class diagram shows the inheritance hierarchy.</span></span>

<span data-ttu-id="0d045-105">Interfacce del decodificatore Container-Level</span><span class="sxs-lookup"><span data-stu-id="0d045-105">Container-Level Decoder Interfaces</span></span>



| <span data-ttu-id="0d045-106">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="0d045-106">Interface</span></span>                                                                                       | <span data-ttu-id="0d045-107">Responsabilità</span><span class="sxs-lookup"><span data-stu-id="0d045-107">Responsibilities</span></span>                             | <span data-ttu-id="0d045-108">Implementazione</span><span class="sxs-lookup"><span data-stu-id="0d045-108">Implementation</span></span>                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="0d045-109">IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="0d045-109">IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)                                             | <span data-ttu-id="0d045-110">Servizi a livello di contenitore</span><span class="sxs-lookup"><span data-stu-id="0d045-110">Container-level services</span></span>                     | <span data-ttu-id="0d045-111">Necessario</span><span class="sxs-lookup"><span data-stu-id="0d045-111">Required</span></span>                                                                   |
| [<span data-ttu-id="0d045-112">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="0d045-112">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) | <span data-ttu-id="0d045-113">Avviso di stato & supporto per l'annullamento</span><span class="sxs-lookup"><span data-stu-id="0d045-113">Progress notification & cancellation support</span></span> | <span data-ttu-id="0d045-114">Consigliato</span><span class="sxs-lookup"><span data-stu-id="0d045-114">Recommended</span></span>                                                                |
| [<span data-ttu-id="0d045-115">IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="0d045-115">IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)                                 | <span data-ttu-id="0d045-116">Enumerazione dei metadati</span><span class="sxs-lookup"><span data-stu-id="0d045-116">Metadata enumeration</span></span>                         | <span data-ttu-id="0d045-117">Facoltativo (obbligatorio solo per i formati che supportano i metadati a livello di contenitore)</span><span class="sxs-lookup"><span data-stu-id="0d045-117">Optional (Required only for formats that support container-level metadata)</span></span> |



 

<span data-ttu-id="0d045-118">Interfacce del decodificatore Frame-Level</span><span class="sxs-lookup"><span data-stu-id="0d045-118">Frame-Level Decoder Interfaces</span></span>



| <span data-ttu-id="0d045-119">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="0d045-119">Interface</span></span>                                                           | <span data-ttu-id="0d045-120">Responsabilità</span><span class="sxs-lookup"><span data-stu-id="0d045-120">Responsibilities</span></span>          | <span data-ttu-id="0d045-121">Implementazione</span><span class="sxs-lookup"><span data-stu-id="0d045-121">Implementation</span></span>                |
|---------------------------------------------------------------------|---------------------------|-------------------------------|
| [<span data-ttu-id="0d045-122">IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="0d045-122">IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)         | <span data-ttu-id="0d045-123">Servizi a livello di frame</span><span class="sxs-lookup"><span data-stu-id="0d045-123">Frame-level services</span></span>      | <span data-ttu-id="0d045-124">Necessario</span><span class="sxs-lookup"><span data-stu-id="0d045-124">Required</span></span>                      |
| [<span data-ttu-id="0d045-125">IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="0d045-125">IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)     | <span data-ttu-id="0d045-126">Enumerazione dei metadati</span><span class="sxs-lookup"><span data-stu-id="0d045-126">Metadata enumeration</span></span>      | <span data-ttu-id="0d045-127">Necessario</span><span class="sxs-lookup"><span data-stu-id="0d045-127">Required</span></span>                      |
| [<span data-ttu-id="0d045-128">IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="0d045-128">IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md) | <span data-ttu-id="0d045-129">Trasformazioni del decodificatore Native</span><span class="sxs-lookup"><span data-stu-id="0d045-129">Native decoder transforms</span></span> | <span data-ttu-id="0d045-130">Consigliato</span><span class="sxs-lookup"><span data-stu-id="0d045-130">Recommended</span></span>                   |
| [<span data-ttu-id="0d045-131">IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="0d045-131">IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)                       | <span data-ttu-id="0d045-132">Servizi di elaborazione non elaborati</span><span class="sxs-lookup"><span data-stu-id="0d045-132">Raw processing services</span></span>   | <span data-ttu-id="0d045-133">Obbligatorio solo per formati RAW</span><span class="sxs-lookup"><span data-stu-id="0d045-133">Required for Raw formats only</span></span> |



 

![gerarchia di ereditarietà dell'interfaccia WIC](graphics/wicinterfaces.png)

## <a name="related-topics"></a><span data-ttu-id="0d045-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0d045-135">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0d045-136">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="0d045-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0d045-137">Implementazione di un decodificatore WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="0d045-137">Implementing a WIC-Enabled Decoder</span></span>](-wic-implementingwicdecoder.md)
</dt> <dt>

[<span data-ttu-id="0d045-138">Implementazione di IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="0d045-138">Implementing IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[<span data-ttu-id="0d045-139">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="0d045-139">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="0d045-140">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="0d045-140">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



