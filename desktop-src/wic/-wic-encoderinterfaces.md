---
description: Interfacce del codificatore
ms.assetid: 02365401-8648-4be1-a447-fabd2cb77355
title: Interfacce del codificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5367a25f1a2a4caf486711f7569312a436f8f474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232322"
---
# <a name="encoder-interfaces"></a><span data-ttu-id="ca716-103">Interfacce del codificatore</span><span class="sxs-lookup"><span data-stu-id="ca716-103">Encoder Interfaces</span></span>


<span data-ttu-id="ca716-104">Nelle tabelle seguenti sono illustrate le interfacce implementate dai codificatori Windows Imaging Component (WIC) e il diagramma classi Mostra la gerarchia di ereditarietà.</span><span class="sxs-lookup"><span data-stu-id="ca716-104">The following tables show the interfaces implemented by Windows Imaging Component (WIC) encoders, and the class diagram shows the inheritance hierarchy.</span></span>

<span data-ttu-id="ca716-105">Interfacce del codificatore Container-Level</span><span class="sxs-lookup"><span data-stu-id="ca716-105">Container-Level Encoder Interfaces</span></span>



| <span data-ttu-id="ca716-106">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="ca716-106">Interface</span></span>                                                                                       | <span data-ttu-id="ca716-107">Responsabilità</span><span class="sxs-lookup"><span data-stu-id="ca716-107">Responsibilities</span></span>                             | <span data-ttu-id="ca716-108">Implementazione</span><span class="sxs-lookup"><span data-stu-id="ca716-108">Implementation</span></span>                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="ca716-109">IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="ca716-109">IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)                                             | <span data-ttu-id="ca716-110">Servizi a livello di contenitore</span><span class="sxs-lookup"><span data-stu-id="ca716-110">Container-level services</span></span>                     | <span data-ttu-id="ca716-111">Necessario</span><span class="sxs-lookup"><span data-stu-id="ca716-111">Required</span></span>                                                                   |
| [<span data-ttu-id="ca716-112">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="ca716-112">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md) | <span data-ttu-id="ca716-113">Avviso di stato & supporto per l'annullamento</span><span class="sxs-lookup"><span data-stu-id="ca716-113">Progress notification & cancellation support</span></span> | <span data-ttu-id="ca716-114">Consigliato</span><span class="sxs-lookup"><span data-stu-id="ca716-114">Recommended</span></span>                                                                |
| [<span data-ttu-id="ca716-115">IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="ca716-115">IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)                                 | <span data-ttu-id="ca716-116">Servizi di serializzazione dei metadati</span><span class="sxs-lookup"><span data-stu-id="ca716-116">Metadata serialization services</span></span>              | <span data-ttu-id="ca716-117">Facoltativo (obbligatorio solo per i formati che supportano i metadati a livello di contenitore)</span><span class="sxs-lookup"><span data-stu-id="ca716-117">Optional (Required only for formats that support container-level metadata)</span></span> |



 

<span data-ttu-id="ca716-118">Interfacce del codificatore Frame-Level</span><span class="sxs-lookup"><span data-stu-id="ca716-118">Frame-Level Encoder Interfaces</span></span>



| <span data-ttu-id="ca716-119">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="ca716-119">Interface</span></span>                                                       | <span data-ttu-id="ca716-120">Responsabilità</span><span class="sxs-lookup"><span data-stu-id="ca716-120">Responsibilities</span></span>                | <span data-ttu-id="ca716-121">Implementazione</span><span class="sxs-lookup"><span data-stu-id="ca716-121">Implementation</span></span> |
|-----------------------------------------------------------------|---------------------------------|----------------|
| [<span data-ttu-id="ca716-122">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="ca716-122">IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)     | <span data-ttu-id="ca716-123">Servizi a livello di frame</span><span class="sxs-lookup"><span data-stu-id="ca716-123">Frame-level services</span></span>            | <span data-ttu-id="ca716-124">Necessario</span><span class="sxs-lookup"><span data-stu-id="ca716-124">Required</span></span>       |
| [<span data-ttu-id="ca716-125">IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="ca716-125">IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md) | <span data-ttu-id="ca716-126">Servizi di serializzazione dei metadati</span><span class="sxs-lookup"><span data-stu-id="ca716-126">Metadata serialization services</span></span> | <span data-ttu-id="ca716-127">Necessario</span><span class="sxs-lookup"><span data-stu-id="ca716-127">Required</span></span>       |



 

![gerarchia di ereditarietà dell'interfaccia del codificatore WIC](graphics/wicencoderinterfaces.png)

<span data-ttu-id="ca716-129">Si noterà che le interfacce del codificatore sono immagini quasi speculari delle interfacce del decodificatore e che la maggior parte dei metodi su queste interfacce corrispondono ai metodi nelle interfacce del decodificatore correlate.</span><span class="sxs-lookup"><span data-stu-id="ca716-129">You'll notice that the encoder interfaces are almost mirror images of the decoder interfaces, and that most of the methods on these interfaces correspond to methods on the related decoder interfaces.</span></span> <span data-ttu-id="ca716-130">Ora che si ha familiarità con l'implementazione di un decodificatore abilitato per WIC, l'implementazione di un codificatore abilitato per WIC può sembrare familiare.</span><span class="sxs-lookup"><span data-stu-id="ca716-130">Now that you're familiar with the implementation of a WIC-enabled decoder, the implementation of a WIC-enabled encoder will seem familiar as well.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca716-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ca716-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ca716-132">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="ca716-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ca716-133">Implementazione di un codificatore di WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="ca716-133">Implementing a WIC-Enabled Encoder</span></span>](-wic-implementingwicencoder.md)
</dt> <dt>

[<span data-ttu-id="ca716-134">Implementazione di IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="ca716-134">Implementing IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[<span data-ttu-id="ca716-135">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="ca716-135">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="ca716-136">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="ca716-136">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



