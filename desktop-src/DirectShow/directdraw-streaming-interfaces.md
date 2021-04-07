---
description: Interfacce di streaming di DirectDraw
ms.assetid: 8f91d90d-0b9f-4d04-bc10-4b82c1b0e062
title: Interfacce di streaming di DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc922bfed03fd2fac3581168bda35f072871a52
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048973"
---
# <a name="directdraw-streaming-interfaces"></a><span data-ttu-id="d0f9d-103">Interfacce di streaming di DirectDraw</span><span class="sxs-lookup"><span data-stu-id="d0f9d-103">DirectDraw Streaming Interfaces</span></span>

> [!Note]  
> <span data-ttu-id="d0f9d-104">Queste API sono deprecate.</span><span class="sxs-lookup"><span data-stu-id="d0f9d-104">These APIs are deprecated.</span></span> <span data-ttu-id="d0f9d-105">Le applicazioni devono usare il filtro [**grabber di esempio**](sample-grabber-filter.md) o implementare un filtro personalizzato per ottenere i dati da un grafico filtro DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d0f9d-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="d0f9d-106">Se nei flussi si utilizzano formati video supportati da DirectDraw, le interfacce seguenti consentono un controllo più efficace sui dati rispetto alle interfacce di base più generiche.</span><span class="sxs-lookup"><span data-stu-id="d0f9d-106">If you use DirectDraw-supported video formats in your streams, the following interfaces give you more powerful control over the data than the more generic base interfaces.</span></span>



| <span data-ttu-id="d0f9d-107">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="d0f9d-107">Interface</span></span>                                                  | <span data-ttu-id="d0f9d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0f9d-108">Description</span></span>                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d0f9d-109">**IDirectDrawMediaStream**</span><span class="sxs-lookup"><span data-stu-id="d0f9d-109">**IDirectDrawMediaStream**</span></span>](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | <span data-ttu-id="d0f9d-110">Imposta e recupera il formato del flusso e l'oggetto DirectDraw associato al flusso multimediale; Questa interfaccia deriva da [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream).</span><span class="sxs-lookup"><span data-stu-id="d0f9d-110">Sets and retrieves the stream format and the DirectDraw object associated with the media stream; this interface derives from [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream).</span></span> <span data-ttu-id="d0f9d-111">È anche possibile usare questa interfaccia per creare esempi video.</span><span class="sxs-lookup"><span data-stu-id="d0f9d-111">You can also use this interface to create video samples.</span></span> |
| [<span data-ttu-id="d0f9d-112">**IDirectDrawStreamSample**</span><span class="sxs-lookup"><span data-stu-id="d0f9d-112">**IDirectDrawStreamSample**</span></span>](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | <span data-ttu-id="d0f9d-113">Consente di alleghi gli esempi video alle superfici DirectDraw; Questa interfaccia deriva dall'interfaccia [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) .</span><span class="sxs-lookup"><span data-stu-id="d0f9d-113">Enables you to attach video samples to DirectDraw surfaces; this interface derives from the [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) interface.</span></span> <span data-ttu-id="d0f9d-114">Ogni superficie collegata include un rettangolo di ridimensionamento per semplificare il rendering.</span><span class="sxs-lookup"><span data-stu-id="d0f9d-114">Each attached surface includes a clipping rectangle to make rendering easier.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d0f9d-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d0f9d-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0f9d-116">Elenco di interfacce di streaming multimediali</span><span class="sxs-lookup"><span data-stu-id="d0f9d-116">List of Multimedia Streaming Interfaces</span></span>](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



