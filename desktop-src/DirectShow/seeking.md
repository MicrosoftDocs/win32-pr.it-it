---
description: La ricerca
ms.assetid: ceccb657-f1e1-4d59-920a-477a95b8a1a4
title: La ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ef7e82009198a790d5c0f7818599aa13905ce82
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104552430"
---
# <a name="seeking"></a><span data-ttu-id="a35bd-103">La ricerca</span><span class="sxs-lookup"><span data-stu-id="a35bd-103">Seeking</span></span>

<span data-ttu-id="a35bd-104">I filtri supportano la ricerca tramite l'interfaccia [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .</span><span class="sxs-lookup"><span data-stu-id="a35bd-104">Filters support seeking through the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="a35bd-105">L'applicazione esegue una query su Filter Graph Manager per **IMediaSeeking** e la usa per emettere comandi Seek.</span><span class="sxs-lookup"><span data-stu-id="a35bd-105">The application queries the Filter Graph Manager for **IMediaSeeking** and uses it to issue seek commands.</span></span> <span data-ttu-id="a35bd-106">Filter Graph Manager distribuisce ogni comando seek a tutti i filtri renderer presenti nel grafico.</span><span class="sxs-lookup"><span data-stu-id="a35bd-106">The Filter Graph Manager distributes each seek command to all of the renderer filters in the graph.</span></span> <span data-ttu-id="a35bd-107">Ogni renderer passa il comando upstream, tramite i pin di output dei filtri upstream, fino a raggiungere un filtro in grado di eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="a35bd-107">Each renderer passes the command upstream, through the output pins of the upstream filters, until it reaches a filter that can execute the seek.</span></span> <span data-ttu-id="a35bd-108">In genere un filtro di origine o un filtro del parser, ad esempio il [separatore AVI](avi-splitter-filter.md), esegue l'operazione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="a35bd-108">Typically a source filter or parser filter, such as the [AVI Splitter](avi-splitter-filter.md), carries out the seek operation.</span></span>

<span data-ttu-id="a35bd-109">Quando un filtro esegue un'operazione di ricerca, Scarica tutti i dati in sospeso.</span><span class="sxs-lookup"><span data-stu-id="a35bd-109">When a filter performs a seek operation, it flushes any pending data.</span></span> <span data-ttu-id="a35bd-110">Il risultato è ridurre al minimo la latenza dei comandi Seek, perché i dati esistenti vengono scaricati dal grafico.</span><span class="sxs-lookup"><span data-stu-id="a35bd-110">The result is to minimize the latency of seek commands, because existing data is flushed from the graph.</span></span> <span data-ttu-id="a35bd-111">Dopo un comando seek, il flusso dell'ora viene reimpostato su zero.</span><span class="sxs-lookup"><span data-stu-id="a35bd-111">After a seek command, stream time resets to zero.</span></span>

<span data-ttu-id="a35bd-112">Nel diagramma seguente viene illustrata la sequenza di eventi.</span><span class="sxs-lookup"><span data-stu-id="a35bd-112">The following diagram illustrates the sequence of events.</span></span>

![sequenza di eventi](images/seeking.png)

<span data-ttu-id="a35bd-114">Se un filtro del parser ha più di un pin di output, in genere designa uno di essi per accettare i comandi Seek.</span><span class="sxs-lookup"><span data-stu-id="a35bd-114">If a parser filter has more than one output pin, it typically designates one of them to accept seek commands.</span></span> <span data-ttu-id="a35bd-115">Gli altri pin rifiutano o ignorano i comandi di ricerca ricevuti.</span><span class="sxs-lookup"><span data-stu-id="a35bd-115">The other pins reject or ignore any seek commands they receive.</span></span> <span data-ttu-id="a35bd-116">In questo modo, il parser mantiene tutti i flussi sincronizzati.</span><span class="sxs-lookup"><span data-stu-id="a35bd-116">In this way, the parser keeps all of its streams synchronized.</span></span> <span data-ttu-id="a35bd-117">Tuttavia, tutti i pin di output devono implementare [**IMediaSeeking:: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) e [**IMediaSeeking:: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) per restituire le funzionalità di ricerca del filtro.</span><span class="sxs-lookup"><span data-stu-id="a35bd-117">However, all output pins should implement [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) and [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) to return the filter's seeking capabilities.</span></span> <span data-ttu-id="a35bd-118">In questo modo, il gestore del grafico del filtro restituisce il valore corretto per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a35bd-118">This ensures that the Filter Graph Manager returns the correct value to the application.</span></span>

<span data-ttu-id="a35bd-119">L'interfaccia [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) è stata deprecata per i filtri.</span><span class="sxs-lookup"><span data-stu-id="a35bd-119">The [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interface has been deprecated for filters.</span></span> <span data-ttu-id="a35bd-120">I client di automazione devono ancora usare questa interfaccia nel gestore del grafo dei filtri, perché **IMediaSeeking** non è compatibile con l'automazione, ma il gestore del grafo del filtro converte tutte le chiamate **IMediaPosition** in chiamate **IMediaSeeking** .</span><span class="sxs-lookup"><span data-stu-id="a35bd-120">Automation clients still need to use this interface on the Filter Graph Manager, because **IMediaSeeking** is not Automation-compatible, but the Filter Graph Manager translates all **IMediaPosition** calls into **IMediaSeeking** calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a35bd-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a35bd-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a35bd-122">Flushing</span><span class="sxs-lookup"><span data-stu-id="a35bd-122">Flushing</span></span>](flushing.md)
</dt> <dt>

[<span data-ttu-id="a35bd-123">Time and Clocks in DirectShow</span><span class="sxs-lookup"><span data-stu-id="a35bd-123">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



