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
# <a name="find-a-filters-peer"></a>Trovare un peer di filtri

Dato un filtro, è possibile attraversare il grafo individuando i filtri a cui è connessa. Per iniziare, è necessario enumerare i pin del filtro. Per ogni pin, controllare se il PIN è connesso a un altro pin. In tal caso, eseguire una query sull'altro pin per il filtro proprietario. È possibile esaminare il grafico nella direzione upstream enumerando i pin di input del filtro o nella direzione downstream enumerando i pin di output.

La funzione seguente cerca un filtro connesso a Monte o a valle. Restituisce il primo filtro corrispondente trovato:


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



La funzione chiama [**IBaseFilter:: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) per enumerare i pin del primo filtro. Per ogni pin, viene chiamato [**Ipin:: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) per verificare se il PIN corrisponde alla direzione specificata (input o output). In tal caso, la funzione determina se il PIN è connesso a un altro pin, chiamando il metodo [**Ipin:: ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) . Infine, viene chiamato [**Ipin:: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) sul pin connesso. Questo metodo restituisce una struttura che contiene, tra le altre cose, un puntatore al filtro proprietario del PIN. Questo puntatore viene restituito al chiamante nel parametro *ppNext* . Il chiamante deve rilasciare il puntatore.

Il codice seguente illustra come chiamare questa funzione:


```C++
IBaseFilter *pF; // Pointer to some filter.
IBaseFilter *pUpstream = NULL;
if (SUCCEEDED(GetNextFilter(pF, PINDIR_INPUT, &pUpstream)))
{
    // Use pUpstream ...
    pUpstream->Release();
}
```



Un filtro può essere connesso a due o più filtri in entrambe le direzioni. Ad esempio, potrebbe trattarsi di un filtro splitter con diversi filtri a valle. Oppure potrebbe trattarsi di un filtro Mux con diversi filtri a Monte. Pertanto, può essere necessario raccoglierli tutti in un elenco.

Il codice seguente illustra un possibile metodo per implementare tale funzione. Usa la classe [**CGenericList**](cgenericlist.md) di DirectShow; è possibile scrivere una funzione equivalente usando un'altra struttura di dati.


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



Per complicare un po' le cose, un filtro può avere più connessioni pin allo stesso filtro. Per evitare di inserire duplicati nell'elenco, eseguire una query su ogni puntatore **IBaseFilter** per **IUnknown** e confrontare i puntatori **IUnknown** . Con le regole di COM, due puntatori di interfaccia fanno riferimento allo stesso oggetto solo se restituiscono puntatori **IUnknown** identici. Nell'esempio precedente, la funzione AddFilterUnique gestisce questo dettaglio.

Nell'esempio seguente viene illustrato come utilizzare la funzione GetPeerFilters:


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tecniche di Graph-Building generali](general-graph-building-techniques.md)
</dt> </dl>

 

 



