---
description: Interfacce di streaming audio
ms.assetid: eaf510ef-a6a3-45e0-8f0a-281a44b0ff6f
title: Interfacce di streaming audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68210beef0b05fcfc89ae5005c485fbc4b74d40f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522482"
---
# <a name="audio-streaming-interfaces"></a><span data-ttu-id="251ec-103">Interfacce di streaming audio</span><span class="sxs-lookup"><span data-stu-id="251ec-103">Audio Streaming Interfaces</span></span>

> [!Note]  
> <span data-ttu-id="251ec-104">Queste API sono deprecate.</span><span class="sxs-lookup"><span data-stu-id="251ec-104">These APIs are deprecated.</span></span> <span data-ttu-id="251ec-105">Le applicazioni devono usare il filtro [**grabber di esempio**](sample-grabber-filter.md) o implementare un filtro personalizzato per ottenere i dati da un grafico filtro DirectShow.</span><span class="sxs-lookup"><span data-stu-id="251ec-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 



| <span data-ttu-id="251ec-106">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="251ec-106">Interface</span></span>                                        | <span data-ttu-id="251ec-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="251ec-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="251ec-108">**IAudioMediaStream**</span><span class="sxs-lookup"><span data-stu-id="251ec-108">**IAudioMediaStream**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)   | <span data-ttu-id="251ec-109">Controlla i flussi multimediali audio.</span><span class="sxs-lookup"><span data-stu-id="251ec-109">Controls audio media streams.</span></span> <span data-ttu-id="251ec-110">Questa interfaccia eredita dall'interfaccia [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) e viene usata per creare uno o più oggetti [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) .</span><span class="sxs-lookup"><span data-stu-id="251ec-110">This interface inherits from the [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) interface and is used to create one or more [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) objects.</span></span> <span data-ttu-id="251ec-111">Viene inoltre utilizzato per impostare e recuperare il formato corrente dei dati del flusso.</span><span class="sxs-lookup"><span data-stu-id="251ec-111">It is also used to set and retrieve the current format of the stream data.</span></span>                                                                                                            |
| [<span data-ttu-id="251ec-112">**IAudioStreamSample**</span><span class="sxs-lookup"><span data-stu-id="251ec-112">**IAudioStreamSample**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) | <span data-ttu-id="251ec-113">Recupera le informazioni dagli oggetti dati [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) sottostanti.</span><span class="sxs-lookup"><span data-stu-id="251ec-113">Retrieves information from the underlying [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) data objects.</span></span>                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="251ec-114">**IMemoryData**</span><span class="sxs-lookup"><span data-stu-id="251ec-114">**IMemoryData**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)               | <span data-ttu-id="251ec-115">Contiene metodi che impostano e recuperano i dati di memoria sugli oggetti dati audio.</span><span class="sxs-lookup"><span data-stu-id="251ec-115">Contains methods that set and retrieve memory data on audio data objects.</span></span> <span data-ttu-id="251ec-116">Gli oggetti dati audio forniscono i dati sottostanti ai quali viene eseguito il flusso degli esempi.</span><span class="sxs-lookup"><span data-stu-id="251ec-116">Audio data objects provide the underlying data that stream samples access.</span></span> <span data-ttu-id="251ec-117">Questa interfaccia fornisce un modo per inizializzare i buffer di memoria e impostare quantità effettive di dati audio negli oggetti.</span><span class="sxs-lookup"><span data-stu-id="251ec-117">This interface provides a way to initialize memory buffers and to set actual amounts of audio data in the objects.</span></span> <span data-ttu-id="251ec-118">Inoltre, è possibile usare il metodo [**IMemoryData:: GetInfo**](/previous-versions/windows/desktop/api/austream/nf-austream-imemorydata-getinfo) per recuperare i dati di memoria audio.</span><span class="sxs-lookup"><span data-stu-id="251ec-118">Additionally, the [**IMemoryData::GetInfo**](/previous-versions/windows/desktop/api/austream/nf-austream-imemorydata-getinfo) method can be used to retrieve audio memory data.</span></span> |
| [<span data-ttu-id="251ec-119">**IAudioData**</span><span class="sxs-lookup"><span data-stu-id="251ec-119">**IAudioData**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                 | <span data-ttu-id="251ec-120">Fornisce metodi che consentono alle applicazioni di impostare e ottenere i dati audio sottostanti a cui faranno riferimento i flussi audio.</span><span class="sxs-lookup"><span data-stu-id="251ec-120">Provides methods that enable applications to set and get the underlying audio data that audio streams will reference.</span></span> <span data-ttu-id="251ec-121">Il formato dei dati audio è impostato nella struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="251ec-121">The audio data format is set in the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>                                                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="251ec-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="251ec-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="251ec-123">Elenco di interfacce di streaming multimediali</span><span class="sxs-lookup"><span data-stu-id="251ec-123">List of Multimedia Streaming Interfaces</span></span>](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 
