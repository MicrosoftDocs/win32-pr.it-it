---
description: Trovare un peer di filtri
ms.assetid: 74d9fe65-f7f4-4971-9550-27884ac4146b
title: Trovare un peer di filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d2f20a7145d2365e7ee1ec261ea861ddc5fa1eb01d0c3b2503f6f53fa25815
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401765"
---
# <a name="find-a-filters-peer"></a>Trovare un peer di filtri

Dato un filtro, è possibile attraversare il grafico individuando i filtri a cui è connesso. Per iniziare, enumerare i pin del filtro. Per ogni pin, controllare se tale pin è connesso a un altro pin. In tal caso, eseguire una query sull'altro segnaposto per individuare il filtro proprietario. È possibile eseguire il grafico nella direzione a monte enumerando i pin di input del filtro o nella direzione downstream enumerando i pin di output.

La funzione seguente cerca un filtro connesso a monte o a valle. Restituisce il primo filtro corrispondente trovato:


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



La funzione chiama [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) per enumerare i pin del primo filtro. Per ogni pin, chiama [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) per verificare se il pin corrisponde alla direzione specificata (input o output). In tal caso, la funzione determina se il pin è connesso a un altro pin, chiamando il [**metodo IPin::ConnectedTo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) Infine, chiama [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) sul pin connesso. Questo metodo restituisce una struttura che contiene, tra le altre cose, un puntatore al filtro proprietario del pin. Questo puntatore viene restituito al chiamante nel *parametro ppNext.* Il chiamante deve rilasciare il puntatore .

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



Un filtro potrebbe essere connesso a due o più filtri in entrambe le direzioni. Ad esempio, potrebbe trattarsi di un filtro con separatore, con diversi filtri a valle. Oppure potrebbe trattarsi di un filtro mux, con diversi filtri a monte. Di conseguenza, è possibile raccogliere tutti i dati in un elenco.

Il codice seguente illustra un modo possibile per implementare una funzione di questo tipo. Usa la classe DirectShow [**CGenericList.**](cgenericlist.md) è possibile scrivere una funzione equivalente usando un'altra struttura di dati.


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



Per complicare le cose, un filtro può avere più connessioni pin allo stesso filtro. Per evitare di inserire duplicati nell'elenco, eseguire una query su ogni puntatore **IBaseFilter** per **IUnknown** e confrontare i puntatori **IUnknown.** In base alle regole di COM, due puntatori a interfaccia fanno riferimento allo stesso oggetto se e solo se restituiscono **puntatori IUnknown** identici. Nell'esempio precedente la funzione AddFilterUnique gestisce questo dettaglio.

L'esempio seguente illustra come usare la funzione GetPeerFilters:


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

[Tecniche Graph-Building generale](general-graph-building-techniques.md)
</dt> </dl>

 

 



