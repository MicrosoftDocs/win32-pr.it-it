---
description: Processori di segnale digitale
ms.assetid: cd3952ca-3958-4944-8fde-f0163a47bff9
title: Processori di segnale digitale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0961554d9c9902e68f74c6b2b57662b23846614f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320514"
---
# <a name="digital-signal-processors"></a><span data-ttu-id="a3de2-103">Processori di segnale digitale</span><span class="sxs-lookup"><span data-stu-id="a3de2-103">Digital Signal Processors</span></span>

<span data-ttu-id="a3de2-104">In questa sezione vengono descritti gli oggetti DSP (Digital Signal Processor) forniti da Windows.</span><span class="sxs-lookup"><span data-stu-id="a3de2-104">This section describes the digital signal processor (DSP) objects provided by Windows.</span></span>

<span data-ttu-id="a3de2-105">Microsoft usa il termine *elaboratore di segnali digitali* per definire un set di oggetti com che eseguono trasformazioni su dati audio e video non compressi.</span><span class="sxs-lookup"><span data-stu-id="a3de2-105">Microsoft uses the term *digital signal processor* to designate a set of COM objects that perform transformations on uncompressed audio and video data.</span></span> <span data-ttu-id="a3de2-106">Il DSP descritto in questo SDK trasforma audio e video in un'ampia gamma di formati non compressi.</span><span class="sxs-lookup"><span data-stu-id="a3de2-106">The DSPs described in this SDK transform audio and video in a variety of uncompressed formats.</span></span>

<span data-ttu-id="a3de2-107">Il DSP può essere usato autonomamente o in combinazione con codec audio e video.</span><span class="sxs-lookup"><span data-stu-id="a3de2-107">The DSPs can be used by themselves, or in combination with audio and video codecs.</span></span> <span data-ttu-id="a3de2-108">Ad eccezione del DSP di acquisizione vocale, ogni DSP elencato qui implementa due interfacce separate ma simili.</span><span class="sxs-lookup"><span data-stu-id="a3de2-108">With the exception of the Voice Capture DSP, each DSP listed here implements two separate but similar interfaces.</span></span>



| <span data-ttu-id="a3de2-109">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="a3de2-109">Interface</span></span>                              | <span data-ttu-id="a3de2-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3de2-110">Description</span></span>                                 |
|----------------------------------------|---------------------------------------------|
| [<span data-ttu-id="a3de2-111">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="a3de2-111">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | <span data-ttu-id="a3de2-112">Compatibile con Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a3de2-112">Compatible with Microsoft Media Foundation.</span></span> |
| [<span data-ttu-id="a3de2-113">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="a3de2-113">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | <span data-ttu-id="a3de2-114">Compatibile con DirectShow.</span><span class="sxs-lookup"><span data-stu-id="a3de2-114">Compatible with DirectShow.</span></span>                 |



 

<span data-ttu-id="a3de2-115">È possibile configurare DSP usando l'interfaccia [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) per impostare le proprietà.</span><span class="sxs-lookup"><span data-stu-id="a3de2-115">You can configure the DSPs by using the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface to set properties.</span></span> <span data-ttu-id="a3de2-116">Alcuni DSP hanno interfacce aggiuntive che impostano le proprietà.</span><span class="sxs-lookup"><span data-stu-id="a3de2-116">Some of the DSPs have additional interfaces that set properties.</span></span> <span data-ttu-id="a3de2-117">Per usare queste interfacce, chiamare il metodo [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) di qualsiasi altra interfaccia del DSP.</span><span class="sxs-lookup"><span data-stu-id="a3de2-117">To use these interfaces, call the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method of any other interface of the DSP.</span></span> <span data-ttu-id="a3de2-118">L'argomento di riferimento per ogni DSP elenca le proprietà, le interfacce e altre funzionalità supportate.</span><span class="sxs-lookup"><span data-stu-id="a3de2-118">The reference topic for each DSP lists the supported properties, interfaces, and other features.</span></span>

<span data-ttu-id="a3de2-119">In questa sezione vengono trattati gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="a3de2-119">This section contains the following topics.</span></span>



| <span data-ttu-id="a3de2-120">DSP</span><span class="sxs-lookup"><span data-stu-id="a3de2-120">DSP</span></span>                                                      | <span data-ttu-id="a3de2-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3de2-121">Description</span></span>                                          |
|----------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="a3de2-122">DSP ricampionatore audio</span><span class="sxs-lookup"><span data-stu-id="a3de2-122">Audio Resampler DSP</span></span>](audioresampler.md)                | <span data-ttu-id="a3de2-123">Converte la frequenza di campionamento di un flusso audio.</span><span class="sxs-lookup"><span data-stu-id="a3de2-123">Converts the sampling rate of an audio stream.</span></span>       |
| [<span data-ttu-id="a3de2-124">Trasformazione controllo colori DSP</span><span class="sxs-lookup"><span data-stu-id="a3de2-124">Color Control Transform DSP</span></span>](colorcontroltransform.md) | <span data-ttu-id="a3de2-125">Regola le caratteristiche dei colori di un flusso video.</span><span class="sxs-lookup"><span data-stu-id="a3de2-125">Adjusts the color characteristics of a video stream.</span></span> |
| [<span data-ttu-id="a3de2-126">Convertitore di colori DSP</span><span class="sxs-lookup"><span data-stu-id="a3de2-126">Color Converter DSP</span></span>](colorconverter.md)                | <span data-ttu-id="a3de2-127">Converte un flusso video tra i formati di colore.</span><span class="sxs-lookup"><span data-stu-id="a3de2-127">Converts a video stream between color formats.</span></span>       |
| [<span data-ttu-id="a3de2-128">Convertitore frequenza frame DSP</span><span class="sxs-lookup"><span data-stu-id="a3de2-128">Frame Rate Converter DSP</span></span>](framerateconverter.md)       | <span data-ttu-id="a3de2-129">Modifica la frequenza dei fotogrammi di un flusso video.</span><span class="sxs-lookup"><span data-stu-id="a3de2-129">Changes the frame rate of a video stream.</span></span>            |
| [<span data-ttu-id="a3de2-130">Ridimensionamento video DSP</span><span class="sxs-lookup"><span data-stu-id="a3de2-130">Video Resizer DSP</span></span>](videoresizer.md)                    | <span data-ttu-id="a3de2-131">Ridimensiona un flusso video.</span><span class="sxs-lookup"><span data-stu-id="a3de2-131">Resizes a video stream.</span></span>                              |
| [<span data-ttu-id="a3de2-132">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="a3de2-132">Voice Capture DSP</span></span>](voicecapturedmo.md)                 | <span data-ttu-id="a3de2-133">Incapsula diversi DSP correlati all'acquisizione vocale.</span><span class="sxs-lookup"><span data-stu-id="a3de2-133">Encapsulates several DSPs related to voice capture.</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="a3de2-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a3de2-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3de2-135">Guida di riferimento alla programmazione di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a3de2-135">Media Foundation Programming Reference</span></span>](media-foundation-programming-reference.md)
</dt> </dl>

 

 
