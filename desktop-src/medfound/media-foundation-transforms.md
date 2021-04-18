---
description: Trasformazioni Media Foundation
ms.assetid: cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0
title: Trasformazioni Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0518ced06169f6d998bdad1747878d109e0676
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320707"
---
# <a name="media-foundation-transforms"></a><span data-ttu-id="e8937-103">Trasformazioni Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e8937-103">Media Foundation Transforms</span></span>

<span data-ttu-id="e8937-104">Le trasformazioni Media Foundation (MFTs) forniscono un modello generico per l'elaborazione dei dati multimediali.</span><span class="sxs-lookup"><span data-stu-id="e8937-104">Media Foundation transforms (MFTs) provide a generic model for processing media data.</span></span> <span data-ttu-id="e8937-105">MFTs vengono usati per i decodificatori, i codificatori e i processori di segnale digitale (DSP).</span><span class="sxs-lookup"><span data-stu-id="e8937-105">MFTs are used for decoders, encoders, and digital signal processors (DSPs).</span></span> <span data-ttu-id="e8937-106">In breve, tutto ciò che si trova nella pipeline multimediale tra l'origine multimediale e il sink multimediale è un MFT.</span><span class="sxs-lookup"><span data-stu-id="e8937-106">In short, anything that sits in the media pipeline between the media source and the media sink is an MFT.</span></span>

<span data-ttu-id="e8937-107">In questa sezione viene descritto il modello di programmazione MFT e viene illustrato come implementare un MFT, con consigli per tipi specifici di MFTs, ad esempio i decodificatori.</span><span class="sxs-lookup"><span data-stu-id="e8937-107">This section describes the MFT programming model and how to implement an MFT, with recommendations for specific types of MFTs, such as decoders.</span></span>



| <span data-ttu-id="e8937-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="e8937-108">Topic</span></span>                                                                    | <span data-ttu-id="e8937-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8937-109">Description</span></span>                                                                                                                                                                                         |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e8937-110">Informazioni su MFTs</span><span class="sxs-lookup"><span data-stu-id="e8937-110">About MFTs</span></span>](about-mfts.md)                                             | <span data-ttu-id="e8937-111">Viene fornita una breve panoramica di MFTs</span><span class="sxs-lookup"><span data-stu-id="e8937-111">Provides a brief overview of MFTs</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="e8937-112">Modello di elaborazione MFT di base</span><span class="sxs-lookup"><span data-stu-id="e8937-112">Basic MFT Processing Model</span></span>](basic-mft-processing-model.md)             | <span data-ttu-id="e8937-113">Viene descritto in dettaglio il modello di base per l'elaborazione dei dati con un MFT.</span><span class="sxs-lookup"><span data-stu-id="e8937-113">Describes in more detail the basic model for processing data with an MFT.</span></span>                                                                                                                           |
| [<span data-ttu-id="e8937-114">MFTs asincrono</span><span class="sxs-lookup"><span data-stu-id="e8937-114">Asynchronous MFTs</span></span>](asynchronous-mfts.md)                               | <span data-ttu-id="e8937-115">Descrive un modello di elaborazione asincrona che rappresenta un'alternativa al modello di base.</span><span class="sxs-lookup"><span data-stu-id="e8937-115">Describes an asynchronous processing model that is an alternative to the basic model.</span></span><br/> <span data-ttu-id="e8937-116">L'elaborazione asincrona è stata introdotta in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e8937-116">Asynchronous processing was introduced in Windows 7.</span></span> <span data-ttu-id="e8937-117">Non tutte le MFT supportano questo modello.</span><span class="sxs-lookup"><span data-stu-id="e8937-117">Not every MFT supports this model.</span></span><br/> |
| [<span data-ttu-id="e8937-118">Registrazione ed enumerazione di MFTs</span><span class="sxs-lookup"><span data-stu-id="e8937-118">Registering and Enumerating MFTs</span></span>](registering-and-enumerating-mfts.md) | <span data-ttu-id="e8937-119">Come registrare un MFT e come enumerare MFTs nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e8937-119">How to register an MFT and how to enumerate MFTs in the registry.</span></span>                                                                                                                                   |
| [<span data-ttu-id="e8937-120">Limitazioni per l'utilizzo dei campi</span><span class="sxs-lookup"><span data-stu-id="e8937-120">Field of Use Restrictions</span></span>](field-of-use-restrictions.md)               | <span data-ttu-id="e8937-121">Viene descritto il meccanismo per sbloccare un MFT con restrizioni di campo per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="e8937-121">Describes the mechanism for unlocking an MFT that has field-of-use restrictions.</span></span>                                                                                                                    |
| [<span data-ttu-id="e8937-122">Confronto tra MFT e DMO</span><span class="sxs-lookup"><span data-stu-id="e8937-122">Comparison of MFTs and DMOs</span></span>](comparison-of-mfts-and-dmos.md)           | <span data-ttu-id="e8937-123">Riepiloga le differenze tra MFTs e DMOs.</span><span class="sxs-lookup"><span data-stu-id="e8937-123">Summarizes the differences between MFTs and DMOs.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="e8937-124">Scrittura di un MFT personalizzato</span><span class="sxs-lookup"><span data-stu-id="e8937-124">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)                         | <span data-ttu-id="e8937-125">Linee guida per la scrittura di un MFT personalizzato.</span><span class="sxs-lookup"><span data-stu-id="e8937-125">Guidelines for writing a custom MFT.</span></span>                                                                                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="e8937-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e8937-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8937-127">Pipeline Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e8937-127">Media Foundation Pipeline</span></span>](media-foundation-pipeline.md)
</dt> <dt>

[<span data-ttu-id="e8937-128">Architettura di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e8937-128">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="e8937-129">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="e8937-129">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




