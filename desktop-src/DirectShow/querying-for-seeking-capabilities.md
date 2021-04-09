---
description: Esecuzione di query per la ricerca di funzionalità
ms.assetid: d1d8c708-75f2-4dc7-a33a-8dd2cea0ee00
title: Esecuzione di query per la ricerca di funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa763ab11267da0a9a13a920285491d83273a8d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876798"
---
# <a name="querying-for-seeking-capabilities"></a><span data-ttu-id="b5cee-103">Esecuzione di query per la ricerca di funzionalità</span><span class="sxs-lookup"><span data-stu-id="b5cee-103">Querying for Seeking Capabilities</span></span>

<span data-ttu-id="b5cee-104">Microsoft® DirectShow® supporta la ricerca tramite l'interfaccia [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .</span><span class="sxs-lookup"><span data-stu-id="b5cee-104">Microsoft® DirectShow® supports seeking through the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="b5cee-105">Il gestore del grafo del filtro espone questa interfaccia, ma la funzionalità di ricerca viene sempre implementata dai filtri nel grafico.</span><span class="sxs-lookup"><span data-stu-id="b5cee-105">The Filter Graph Manager exposes this interface, but the seeking functionality is always implemented by filters in the graph.</span></span>

<span data-ttu-id="b5cee-106">Non è possibile cercare alcuni dati.</span><span class="sxs-lookup"><span data-stu-id="b5cee-106">Some data cannot be seeked.</span></span> <span data-ttu-id="b5cee-107">Ad esempio, non è possibile cercare un flusso video live da una fotocamera.</span><span class="sxs-lookup"><span data-stu-id="b5cee-107">For example, you cannot seek a live video stream from a camera.</span></span> <span data-ttu-id="b5cee-108">Se un flusso è ricercabile, tuttavia, esistono diversi tipi di ricerca che potrebbero supportare.</span><span class="sxs-lookup"><span data-stu-id="b5cee-108">If a stream is seekable, however, there are various types of seeking it might support.</span></span> <span data-ttu-id="b5cee-109">Tra queste sono incluse:</span><span class="sxs-lookup"><span data-stu-id="b5cee-109">These include:</span></span>

-   <span data-ttu-id="b5cee-110">Ricerca in una posizione arbitraria nel flusso.</span><span class="sxs-lookup"><span data-stu-id="b5cee-110">Seeking to an arbitrary position in the stream.</span></span>
-   <span data-ttu-id="b5cee-111">Recupero della durata del flusso.</span><span class="sxs-lookup"><span data-stu-id="b5cee-111">Retrieving the duration of the stream.</span></span>
-   <span data-ttu-id="b5cee-112">Recupero della posizione corrente all'interno del flusso.</span><span class="sxs-lookup"><span data-stu-id="b5cee-112">Retrieving the current position within the stream.</span></span>
-   <span data-ttu-id="b5cee-113">Riproduzione in ordine inverso.</span><span class="sxs-lookup"><span data-stu-id="b5cee-113">Playing in reverse.</span></span>

<span data-ttu-id="b5cee-114">L'interfaccia **IMediaSeeking** definisce un set di flag, [**che \_ cercano \_ \_ funzionalità di ricerca**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities), che descrivono le possibili funzionalità di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b5cee-114">The **IMediaSeeking** interface defines a set of flags, [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities), that describe the possible seeking capabilities.</span></span> <span data-ttu-id="b5cee-115">Per recuperare le funzionalità del flusso, chiamare il metodo [**IMediaSeeking:: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="b5cee-115">To retrieve the stream's capabilities, call the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span> <span data-ttu-id="b5cee-116">Il metodo restituisce una combinazione bit per bit di flag.</span><span class="sxs-lookup"><span data-stu-id="b5cee-116">The method returns a bitwise combination of flags.</span></span> <span data-ttu-id="b5cee-117">L'applicazione può testarli usando l'operatore & ( **and** bit per bit).</span><span class="sxs-lookup"><span data-stu-id="b5cee-117">The application can test them using the & (bitwise **AND**) operator.</span></span> <span data-ttu-id="b5cee-118">Il codice seguente, ad esempio, controlla se il grafo può cercare in una posizione arbitraria:</span><span class="sxs-lookup"><span data-stu-id="b5cee-118">For example, the following code checks whether the graph can seek to an arbitrary position:</span></span>


```C++
DWORD dwCap = 0;
HRESULT hr = pSeek->GetCapabilities(&dwCap);
if (AM_SEEKING_CanSeekAbsolute & dwCap)
{
    // Graph can seek to absolute positions.
}
```



 

 



