---
description: Filtri driver di classe WDM
ms.assetid: 864fc5ad-5aeb-4dc7-bdd2-2ad2bfb57741
title: Filtri driver di classe WDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338e4ec4d2aaa58bdac737b58571497cad708876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880038"
---
# <a name="wdm-class-driver-filters"></a>Filtri driver di classe WDM

Se un dispositivo di acquisizione usa un driver Windows Driver Model (WDM), il grafico potrebbe richiedere determinati filtri a Monte dal filtro di acquisizione. Questi filtri sono denominati filtri driver di classe di flusso o filtri WDM. Supportano funzionalità aggiuntive fornite dall'hardware. Una scheda Tuner TV, ad esempio, dispone di funzioni per l'impostazione del canale. Il filtro corrispondente è il filtro del [sintonizzatore TV](tv-tuner-filter.md) che espone l'interfaccia [**Impossibile IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) . Per rendere disponibile questa funzionalità per l'applicazione, è necessario connettere il filtro del sintonizzatore TV al filtro di acquisizione.

L'interfaccia [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) fornisce il modo più semplice per aggiungere filtri WDM al grafo. A un certo punto durante la compilazione del grafo, chiamare [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) o [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream). Uno di questi metodi consente di individuare automaticamente i filtri WDM necessari e connetterli al filtro di acquisizione. Nella parte restante di questa sezione viene descritto come aggiungere i filtri WDM manualmente. Tuttavia, tenere presente che l'approccio consigliato è semplicemente chiamare uno di questi metodi **ICaptureGraphBuilder2** .

I pin in un filtro WDM supportano uno o più supporti. Un supporto definisce un metodo di comunicazione, ad esempio un bus. È necessario connettere i pin che supportano lo stesso supporto. La struttura [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) , che è equivalente alla struttura **\_ media KSPIN** usata per i driver di streaming del kernel, definisce un supporto in DirectShow. Il membro **clsMedium** della struttura **REGPINMEDIUM** specifica l'identificatore di classe (CLSID) per il supporto. Per recuperare il supporto di un PIN, chiamare il metodo [**IKsPin:: KsQueryMediums**](ikspin-ksquerymediums.md) . Questo metodo restituisce un puntatore a un blocco di memoria che contiene una struttura di [**\_ elementi KSMULTIPLE**](ksmultiple-item.md) , seguita da zero o più strutture **REGPINMEDIUM** . Ogni struttura **REGPINMEDIUM** identifica un supporto supportato dal pin.

Non connettere un PIN se il supporto presenta un CLSID di GUID \_ null o KSMEDIUMSETID \_ standard. Si tratta di valori predefiniti che indicano che il PIN non supporta supporti.

Inoltre, non connettere un PIN, a meno che il filtro non richieda esattamente un'istanza connessa del PIN. In caso contrario, l'applicazione potrebbe provare a connettere diversi pin che non devono avere connessioni, il che può causare l'interruzione della risposta del programma. Per individuare il numero di istanze necessarie, recuperare il set di \_ \_ Proprietà NECESSARYINSTANCES pin KSPROPERTY, come illustrato nell'esempio di codice seguente. Per brevità, in questo esempio non viene testato alcun codice restituito né viene rilasciata alcuna interfaccia. Naturalmente, l'applicazione deve eseguire entrambe le operazioni.


```C++
// Obtain the pin factory identifier.
IKsPinFactory *pPinFactory;
hr = pPin->QueryInterface(IID_IKsPinFactory, (void **)&pPinFactory);

ULONG ulFactoryId;
hr = pPinFactory->KsPinFactory(&ulFactoryId);

// Get the "instance" property from the filter.
IKsControl *pKsControl;
hr = pFilter->QueryInterface(IID_IKsControl, (void **)&pKsControl);

KSP_PIN ksPin;
ksPin.Property.Set = KSPROPSETID_Pin;
ksPin.Property.Id = KSPROPERTY_PIN_NECESSARYINSTANCES;
ksPin.Property.Flags = KSPROPERTY_TYPE_GET;
ksPin.PinId = ulFactoryId;
ksPin.Reserved = 0; 

KSPROPERTY ksProp;
ULONG ulInstances, bytes;
pKsControl->KsProperty((PKSPROPERTY)&ksPin, sizeof(ksPin), 
    &ulInstances, sizeof(ULONG), &bytes);

if (hr == S_OK && bytes == sizeof(ULONG)) 
{
    if (ulInstances == 1) 
    {
        // Filter requires one instance of this pin.
        // This pin is OK.
    } 
}
```



Lo pseudocodice seguente è una struttura estremamente breve che illustra come trovare e connettere i filtri WDM. Omette molti dettagli e ha lo scopo di illustrare solo i passaggi generali che l'applicazione deve eseguire.


```C++
Add supporting filters:
{
    foreach input pin:
        skip if (pin is connected)
    
        Get pin medium
        skip if (medium is GUID_NULL or KSMEDIUMSETID_Standard)
    
        Query filter for KSPROPERTY_PIN_NECESSARYINSTANCES property
        skip if (necessary instances != 1)

        Match an existing pin || Find a matching filter
}    

Match an existing pin:
{
    foreach filter in the graph
        foreach unconnected pin
            Get pin medium
            if (mediums match)
                connect the pins    
}

Find a matching filter:
{    
    Query the filter graph manager for IFilterMapper2.
    Find a filter with an output pin that matches the medium.
    Add the filter to the graph.
    Connect the pins.
    Add supporting filters. (Recursive call.)
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Argomenti sull'acquisizione avanzata](advanced-capture-topics.md)
</dt> </dl>

 

 



