---
description: Gerarchia dell'interfaccia e dell'oggetto streaming multimediale
ms.assetid: dbb6dc3b-b55e-4f6c-918f-068308e2dba9
title: Gerarchia dell'interfaccia e dell'oggetto streaming multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52339644730139af22fd21fa2c24b8448a1afaf3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103886033"
---
# <a name="multimedia-streaming-object-and-interface-hierarchy"></a><span data-ttu-id="0743a-103">Gerarchia dell'interfaccia e dell'oggetto streaming multimediale</span><span class="sxs-lookup"><span data-stu-id="0743a-103">Multimedia Streaming Object and Interface Hierarchy</span></span>

> [!Note]  
> <span data-ttu-id="0743a-104">Queste API sono deprecate.</span><span class="sxs-lookup"><span data-stu-id="0743a-104">These APIs are deprecated.</span></span> <span data-ttu-id="0743a-105">Le applicazioni devono usare il filtro [**grabber di esempio**](sample-grabber-filter.md) o implementare un filtro personalizzato per ottenere i dati da un grafico filtro DirectShow.</span><span class="sxs-lookup"><span data-stu-id="0743a-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="0743a-106">Nel diagramma seguente viene illustrata la gerarchia di oggetti utilizzata nel flusso multimediale.</span><span class="sxs-lookup"><span data-stu-id="0743a-106">The following diagram shows the object hierarchy used in multimedia streaming.</span></span>

![gerarchia di oggetti multimediastreaming](images/mmstream02.png)

<span data-ttu-id="0743a-108">L'architettura di streaming multimediale definisce tre tipi generali di oggetto:</span><span class="sxs-lookup"><span data-stu-id="0743a-108">The multimedia streaming architecture defines three general type of object:</span></span>

-   <span data-ttu-id="0743a-109">L'oggetto **AMMultimediaStream** espone l'interfaccia [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) .</span><span class="sxs-lookup"><span data-stu-id="0743a-109">The **AMMultimediaStream** object exposes the [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) interface.</span></span> <span data-ttu-id="0743a-110">Internamente, questo oggetto esegue il wrapping del grafico del filtro DirectShow.</span><span class="sxs-lookup"><span data-stu-id="0743a-110">Internally, this object wraps the DirectShow filter graph.</span></span>
-   <span data-ttu-id="0743a-111">Gli oggetti del *flusso multimediale* espongono l'interfaccia [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) e sono specifici dei dati.</span><span class="sxs-lookup"><span data-stu-id="0743a-111">*Media stream* objects expose the [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) interface and are data specific.</span></span> <span data-ttu-id="0743a-112">L'oggetto AMMultimediaStream contiene uno o più flussi multimediali.</span><span class="sxs-lookup"><span data-stu-id="0743a-112">The AMMultimediaStream object contains one or more media streams.</span></span>
-   <span data-ttu-id="0743a-113">Gli oggetti di *esempio di flusso* contengono i dati per un flusso specifico.</span><span class="sxs-lookup"><span data-stu-id="0743a-113">*Stream sample* objects contain the data for a particular stream.</span></span>

<span data-ttu-id="0743a-114">Sono supportati gli oggetti del flusso multimediale seguenti:</span><span class="sxs-lookup"><span data-stu-id="0743a-114">The following media stream objects are supported:</span></span>

-   <span data-ttu-id="0743a-115">Flusso audio.</span><span class="sxs-lookup"><span data-stu-id="0743a-115">Audio stream.</span></span> <span data-ttu-id="0743a-116">Espone l'interfaccia [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream) .</span><span class="sxs-lookup"><span data-stu-id="0743a-116">Exposes the [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream) interface.</span></span>
-   <span data-ttu-id="0743a-117">Flusso DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="0743a-117">DirectDraw stream.</span></span> <span data-ttu-id="0743a-118">Rappresenta un flusso video di cui viene eseguito il rendering in una superficie DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="0743a-118">Represents a video stream that is rendered to a DirectDraw surface.</span></span> <span data-ttu-id="0743a-119">Espone l'interfaccia [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) .</span><span class="sxs-lookup"><span data-stu-id="0743a-119">Exposes the [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) interface.</span></span>
-   <span data-ttu-id="0743a-120">Flusso del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="0743a-120">Media type stream.</span></span> <span data-ttu-id="0743a-121">Rappresenta dati arbitrari.</span><span class="sxs-lookup"><span data-stu-id="0743a-121">Represents arbitrary data.</span></span> <span data-ttu-id="0743a-122">Espone l'interfaccia [**IAMMediaTypeStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream) .</span><span class="sxs-lookup"><span data-stu-id="0743a-122">Exposes the [**IAMMediaTypeStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream) interface.</span></span>

<span data-ttu-id="0743a-123">Ogni oggetto flusso multimediale crea il proprio tipo di oggetto di esempio di flusso:</span><span class="sxs-lookup"><span data-stu-id="0743a-123">Each media stream object creates its own kind of stream sample object:</span></span>

-   <span data-ttu-id="0743a-124">I flussi audio creano esempi audio, che espongono l'interfaccia [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) .</span><span class="sxs-lookup"><span data-stu-id="0743a-124">Audio streams create audio samples, which expose the [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) interface.</span></span>
-   <span data-ttu-id="0743a-125">I flussi DirectDraw creano esempi di DirectDraw, che espongono l'interfaccia [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) .</span><span class="sxs-lookup"><span data-stu-id="0743a-125">DirectDraw streams create DirectDraw samples, which expose the [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) interface.</span></span>
-   <span data-ttu-id="0743a-126">Flussi di tipi di supporti creare esempi di tipi di supporto, che espongono l'interfaccia [**IAMMediaTypeSample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample) .</span><span class="sxs-lookup"><span data-stu-id="0743a-126">Media type streams create media type samples, which expose the [**IAMMediaTypeSample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample) interface.</span></span>

<span data-ttu-id="0743a-127">Il diagramma seguente mostra la gerarchia di interfaccia per le interfacce elencate in precedenza:</span><span class="sxs-lookup"><span data-stu-id="0743a-127">The following diagram shows the interface hierarchy for the interfaces listed previously:</span></span>

![gerarchia dell'interfaccia multimediastreaming](images/mmstream01.png)

 

 



