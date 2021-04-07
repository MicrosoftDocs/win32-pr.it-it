---
description: Trovare un peer di filtri
ms.assetid: 74d9fe65-f7f4-4971-9550-27884ac4146b
title: Trovare un peer di filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1717f6ad61ad7310fdaa11ea5baaab4dcb7f8011
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048874"
---
# <a name="find-a-filters-peer"></a><span data-ttu-id="e5eb1-103">Trovare un peer di filtri</span><span class="sxs-lookup"><span data-stu-id="e5eb1-103">Find a Filters Peer</span></span>

<span data-ttu-id="e5eb1-104">Dato un filtro, è possibile attraversare il grafo individuando i filtri a cui è connessa.</span><span class="sxs-lookup"><span data-stu-id="e5eb1-104">Given a filter, you can traverse the graph by finding the filters to which it is connected.</span></span> <span data-ttu-id="e5eb1-105">Per iniziare, è necessario enumerare i pin del filtro.</span><span class="sxs-lookup"><span data-stu-id="e5eb1-105">Start by enumerating the filter's pins.</span></span> <span data-ttu-id="e5eb1-106">Per ogni pin, controllare se il PIN è connesso a un altro pin.</span><span class="sxs-lookup"><span data-stu-id="e5eb1-106">For each pin, check whether that pin is connected to another pin.</span></span> <span data-ttu-id="e5eb1-107">In tal caso, eseguire una query sull'altro pin per il filtro proprietario.</span><span class="sxs-lookup"><span data-stu-id="e5eb1-107">If so, query the other pin for it's owning filter.</span></span> <span data-ttu-id="e5eb1-108">È possibile esaminare il grafico nella direzione upstream enumerando i pin di input del filtro o nella direzione downstream enumerando i pin di output.</span><span class="sxs-lookup"><span data-stu-id="e5eb1-108">You can walk the graph in the upstream direction by enumerating the filter's input pins, or in the downstream direction by enumerating the output pins.</span></span>

<span data-ttu-id="e5eb1-109">La funzione seguente cerca un filtro connesso a Monte o a valle.</span><span class="sxs-lookup"><span data-stu-id="e5eb1-109">The following function searches upstream or downstream for a connected filter.</span></span> <span data-ttu-id="e5eb1-110">Restituisce il primo filtro corrispondente trovato:</span><span class="sxs-lookup"><span data-stu-id="e5eb1-110">It returns the first matching filter that it finds:</span></span>


```C++
// Get the first upstream or downstream filter
HRESULT GetNextFilter(
    IBaseFilter *pFilter, // Pointer to the starting filter
    PIN_DIRECTION Dir,    // Direction to search (upstream or downstream)
    IBaseFilter **ppNext) // Receives a pointer to the next filter.
{
    if (!pFilter || !ppNext) return E_POINTER;

    IEnumPins *pEnum = 0;
    IPin *pPin = 0;
    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr)) return hr;
    while (S_OK == pEnum->Next(1, &pPin, 0))
    {
        // See if this pin matches the specified direction.
        PIN_DIRECTION ThisPinDir;
        hr = pPin->QueryDirection(&ThisPinDir);
        if (FAILED(hr))
        {
            // Something strange happened.
            hr = E_UNEXPECTED;
            pPin->Release();
            break;
        }
        if (ThisPinDir == Dir)
        {
            // Check if the pin is connected to another pin.
            IPin *pPinNext = 0;
            hr = pPin->ConnectedTo(&pPinNext);
            if (SUCCEEDED(hr))
            {
                // Get the filter that owns that pin.
                PIN_INFO PinInfo;
                hr = pPinNext->QueryPinInfo(&PinInfo);
                pPinNext->Release();
                pPin->Release();
                pEnum->Release();
                if (FAILED(hr) || (PinInfo.pFilter == NULL))
                {
                    // Something strange happened.
                    return E_UNEXPECTED;
                }
                // This is the filter we're looking for.
                *ppNext = PinInfo.pFilter; // Client must release.
                return S_OK;
            }
        }
        pPin->Release();
    }
    pEnum->Release();
    // Did not find a matching filter.
    return E_FAIL;
}
```



<span data-ttu-id="e5eb1-111">La funzione chiama [**IBaseFilter:: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) per enumerare i pin del primo filtro.</span><span class="sxs-lookup"><span data-stu-id="e5eb1-111">The function calls [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) to enumerate the first filter's pins.</span></span> <span data-ttu-id="e5eb1-112">Per ogni pin, viene chiamato [**Ipin:: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) per verificare se il PIN corrisponde alla direzione specificata (input o output).</span><span class="sxs-lookup"><span data-stu-id="e5eb1-112">For each pin, it calls [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) to check whether the pin matches the specified direction (input or output).</span></span> <span data-ttu-id="e5eb1-113">In tal caso, la funzione determina se il PIN è connesso a un altro pin, chiamando il metodo [**Ipin:: ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) .</span><span class="sxs-lookup"><span data-stu-id="e5eb1-113">If so, the function determines whether that pin is connected to another pin, by calling the [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) method.</span></span> <span data-ttu-id="e5eb1-114">Infine, viene chiamato [**Ipin:: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) sul pin connesso.</span><span class="sxs-lookup"><span data-stu-id="e5eb1-114">Finally, it calls [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) on the connected pin.</span></span> <span data-ttu-id="e5eb1-115">Questo metodo restituisce una struttura che contiene, tra le altre cose, un puntatore al filtro proprietario del PIN.</span><span class="sxs-lookup"><span data-stu-id="e5eb1-115">This method returns a structure that contains, among other things, a pointer to that pin's owning filter.</span></span> <span data-ttu-id="e5eb1-116">Questo puntatore viene restituito al chiamante nel parametro *ppNext* .</span><span class="sxs-lookup"><span data-stu-id="e5eb1-116">This pointer is returned to the caller in the *ppNext* parameter.</span></span> <span data-ttu-id="e5eb1-117">Il chiamante deve rilasciare il puntatore.</span><span class="sxs-lookup"><span data-stu-id="e5eb1-117">The caller must release the pointer.</span></span>

<span data-ttu-id="e5eb1-118">Il codice seguente illustra come chiamare questa funzione:</span><span class="sxs-lookup"><span data-stu-id="e5eb1-118">The following code shows how to call this function:</span></span>


```C++
IBaseFilter *pF; // Pointer to some filter.
IBaseFilter *pUpstream = NULL;
if (SUCCEEDED(GetNextFilter(pF, PINDIR_INPUT, &pUpstream)))
{
    // Use pUpstream ...
    pUpstream->Release();
}
```



<span data-ttu-id="e5eb1-119">Un filtro può essere connesso a due o più filtri in entrambe le direzioni.</span><span class="sxs-lookup"><span data-stu-id="e5eb1-119">A filter might be connected to two or more filters in either direction.</span></span> <span data-ttu-id="e5eb1-120">Ad esempio, potrebbe trattarsi di un filtro splitter con diversi filtri a valle.</span><span class="sxs-lookup"><span data-stu-id="e5eb1-120">For example, it might be a splitter filter, with several filters downstream from it.</span></span> <span data-ttu-id="e5eb1-121">Oppure potrebbe trattarsi di un filtro Mux con diversi filtri a Monte.</span><span class="sxs-lookup"><span data-stu-id="e5eb1-121">Or it might be a mux filter, with several filters upstream from it.</span></span> <span data-ttu-id="e5eb1-122">Pertanto, può essere necessario raccoglierli tutti in un elenco.</span><span class="sxs-lookup"><span data-stu-id="e5eb1-122">Therefore, you might want to collect all of them into a list.</span></span>

<span data-ttu-id="e5eb1-123">Il codice seguente illustra un possibile metodo per implementare tale funzione.</span><span class="sxs-lookup"><span data-stu-id="e5eb1-123">The following code shows one possible way to implement such a function.</span></span> <span data-ttu-id="e5eb1-124">Usa la classe [**CGenericList**](cgenericlist.md) di DirectShow; è possibile scrivere una funzione equivalente usando un'altra struttura di dati.</span><span class="sxs-lookup"><span data-stu-id="e5eb1-124">It uses the DirectShow [**CGenericList**](cgenericlist.md) class; you could write an equivalent function using some other data structure.</span></span>


```C++
#include <streams.h>  // Link to the DirectShow base class library
// Define a typedef for a list of filters.
typedef CGenericList<IBaseFilter> CFilterList;

// Forward declaration. Adds a filter to the list unless it's a duplicate.
void AddFilterUnique(CFilterList &FilterList, IBaseFilter *pNew);

// Find all the immediate upstream or downstream peers of a filter.
HRESULT GetPeerFilters(
    IBaseFilter *pFilter, // Pointer to the starting filter
    PIN_DIRECTION Dir,    // Direction to search (upstream or downstream)
    CFilterList &FilterList)  // Collect the results in this list.
{
    if (!pFilter) return E_POINTER;

    IEnumPins *pEnum = 0;
    IPin *pPin = 0;
    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr)) return hr;
    while (S_OK == pEnum->Next(1, &pPin, 0))
    {
        // See if this pin matches the specified direction.
        PIN_DIRECTION ThisPinDir;
        hr = pPin->QueryDirection(&ThisPinDir);
        if (FAILED(hr))
        {
            // Something strange happened.
            hr = E_UNEXPECTED;
            pPin->Release();
            break;
        }
        if (ThisPinDir == Dir)
        {
            // Check if the pin is connected to another pin.
            IPin *pPinNext = 0;
            hr = pPin->ConnectedTo(&pPinNext);
            if (SUCCEEDED(hr))
            {
                // Get the filter that owns that pin.
                PIN_INFO PinInfo;
                hr = pPinNext->QueryPinInfo(&PinInfo);
                pPinNext->Release();
                if (FAILED(hr) || (PinInfo.pFilter == NULL))
                {
                    // Something strange happened.
                    pPin->Release();
                    pEnum->Release();
                    return E_UNEXPECTED;
                }
                // Insert the filter into the list.
                AddFilterUnique(FilterList, PinInfo.pFilter);
                PinInfo.pFilter->Release();
            }
        }
        pPin->Release();
    }
    pEnum->Release();
    return S_OK;
}
void AddFilterUnique(CFilterList &FilterList, IBaseFilter *pNew)
{
    if (pNew == NULL) return;

    POSITION pos = FilterList.GetHeadPosition();
    while (pos)
    {
        IBaseFilter *pF = FilterList.GetNext(pos);
        if (IsEqualObject(pF, pNew))
        {
            return;
        }
    }
    pNew->AddRef();  // The caller must release everything in the list.
    FilterList.AddTail(pNew);
}
```



<span data-ttu-id="e5eb1-125">Per complicare un po' le cose, un filtro può avere più connessioni pin allo stesso filtro.</span><span class="sxs-lookup"><span data-stu-id="e5eb1-125">To complicate matters somewhat, a filter can have multiple pin connections to the same filter.</span></span> <span data-ttu-id="e5eb1-126">Per evitare di inserire duplicati nell'elenco, eseguire una query su ogni puntatore **IBaseFilter** per **IUnknown** e confrontare i puntatori **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="e5eb1-126">To avoid putting duplicates into the list, query each **IBaseFilter** pointer for **IUnknown** and compare the **IUnknown** pointers.</span></span> <span data-ttu-id="e5eb1-127">Con le regole di COM, due puntatori di interfaccia fanno riferimento allo stesso oggetto solo se restituiscono puntatori **IUnknown** identici.</span><span class="sxs-lookup"><span data-stu-id="e5eb1-127">By the rules of COM, two interface pointers refer to the same object if and only if they return identical **IUnknown** pointers.</span></span> <span data-ttu-id="e5eb1-128">Nell'esempio precedente, la funzione AddFilterUnique gestisce questo dettaglio.</span><span class="sxs-lookup"><span data-stu-id="e5eb1-128">In the previous example, the AddFilterUnique function handles this detail.</span></span>

<span data-ttu-id="e5eb1-129">Nell'esempio seguente viene illustrato come utilizzare la funzione GetPeerFilters:</span><span class="sxs-lookup"><span data-stu-id="e5eb1-129">The following example shows how to use the GetPeerFilters function:</span></span>


```C++
IBaseFilter *pF; // Pointer to some filter.
CFilterList FList(NAME("MyList"));  // List to hold the downstream peers.
hr = GetPeerFilters(pF, PINDIR_OUTPUT, FList);
if (SUCCEEDED(hr))
{
    POSITION pos = FList.GetHeadPosition();
    while (pos)
    {
        IBaseFilter *pDownstream = FList.GetNext(pos);
        pDownstream->Release();
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="e5eb1-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e5eb1-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5eb1-131">Tecniche di Graph-Building generali</span><span class="sxs-lookup"><span data-stu-id="e5eb1-131">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> </dl>

 

 



