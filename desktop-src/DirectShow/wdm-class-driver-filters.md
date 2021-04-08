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
# <a name="wdm-class-driver-filters"></a><span data-ttu-id="d1631-103">Filtri driver di classe WDM</span><span class="sxs-lookup"><span data-stu-id="d1631-103">WDM Class Driver Filters</span></span>

<span data-ttu-id="d1631-104">Se un dispositivo di acquisizione usa un driver Windows Driver Model (WDM), il grafico potrebbe richiedere determinati filtri a Monte dal filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d1631-104">If a capture device uses a Windows Driver Model (WDM) driver, the graph might require certain filters upstream from the capture filter.</span></span> <span data-ttu-id="d1631-105">Questi filtri sono denominati filtri driver di classe di flusso o filtri WDM.</span><span class="sxs-lookup"><span data-stu-id="d1631-105">These filters are called stream-class driver filters or WDM filters.</span></span> <span data-ttu-id="d1631-106">Supportano funzionalità aggiuntive fornite dall'hardware.</span><span class="sxs-lookup"><span data-stu-id="d1631-106">They support additional functionality provided by the hardware.</span></span> <span data-ttu-id="d1631-107">Una scheda Tuner TV, ad esempio, dispone di funzioni per l'impostazione del canale.</span><span class="sxs-lookup"><span data-stu-id="d1631-107">For example, a TV tuner card has functions for setting the channel.</span></span> <span data-ttu-id="d1631-108">Il filtro corrispondente è il filtro del [sintonizzatore TV](tv-tuner-filter.md) che espone l'interfaccia [**Impossibile IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) .</span><span class="sxs-lookup"><span data-stu-id="d1631-108">The corresponding filter is the [TV Tuner](tv-tuner-filter.md) filter, which exposes the [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) interface.</span></span> <span data-ttu-id="d1631-109">Per rendere disponibile questa funzionalità per l'applicazione, è necessario connettere il filtro del sintonizzatore TV al filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d1631-109">To make this functionality available to the application, you must connect the TV Tuner filter to the capture filter.</span></span>

<span data-ttu-id="d1631-110">L'interfaccia [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) fornisce il modo più semplice per aggiungere filtri WDM al grafo.</span><span class="sxs-lookup"><span data-stu-id="d1631-110">The [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface provides the easiest way to add WDM filters to the graph.</span></span> <span data-ttu-id="d1631-111">A un certo punto durante la compilazione del grafo, chiamare [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) o [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).</span><span class="sxs-lookup"><span data-stu-id="d1631-111">At some point while building the graph, call [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) or [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).</span></span> <span data-ttu-id="d1631-112">Uno di questi metodi consente di individuare automaticamente i filtri WDM necessari e connetterli al filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d1631-112">Either one of these methods will automatically locate the necessary WDM filters and connect them to the capture filter.</span></span> <span data-ttu-id="d1631-113">Nella parte restante di questa sezione viene descritto come aggiungere i filtri WDM manualmente.</span><span class="sxs-lookup"><span data-stu-id="d1631-113">The rest of this section describes how to add WDM filters manually.</span></span> <span data-ttu-id="d1631-114">Tuttavia, tenere presente che l'approccio consigliato è semplicemente chiamare uno di questi metodi **ICaptureGraphBuilder2** .</span><span class="sxs-lookup"><span data-stu-id="d1631-114">However, be aware that the recommend approach is simply to call one of these **ICaptureGraphBuilder2** methods.</span></span>

<span data-ttu-id="d1631-115">I pin in un filtro WDM supportano uno o più supporti.</span><span class="sxs-lookup"><span data-stu-id="d1631-115">The pins on a WDM filter support one or more mediums.</span></span> <span data-ttu-id="d1631-116">Un supporto definisce un metodo di comunicazione, ad esempio un bus.</span><span class="sxs-lookup"><span data-stu-id="d1631-116">A medium defines a method of communication, such as a bus.</span></span> <span data-ttu-id="d1631-117">È necessario connettere i pin che supportano lo stesso supporto.</span><span class="sxs-lookup"><span data-stu-id="d1631-117">You must connect pins that support the same medium.</span></span> <span data-ttu-id="d1631-118">La struttura [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) , che è equivalente alla struttura **\_ media KSPIN** usata per i driver di streaming del kernel, definisce un supporto in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d1631-118">The [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) structure, which is equivalent to the **KSPIN\_MEDIUM** structure used for kernel streaming drivers, defines a medium in DirectShow.</span></span> <span data-ttu-id="d1631-119">Il membro **clsMedium** della struttura **REGPINMEDIUM** specifica l'identificatore di classe (CLSID) per il supporto.</span><span class="sxs-lookup"><span data-stu-id="d1631-119">The **clsMedium** member of the **REGPINMEDIUM** structure specifies the class identifier (CLSID) for the medium.</span></span> <span data-ttu-id="d1631-120">Per recuperare il supporto di un PIN, chiamare il metodo [**IKsPin:: KsQueryMediums**](ikspin-ksquerymediums.md) .</span><span class="sxs-lookup"><span data-stu-id="d1631-120">To retrieve a pin's medium, call the [**IKsPin::KsQueryMediums**](ikspin-ksquerymediums.md) method.</span></span> <span data-ttu-id="d1631-121">Questo metodo restituisce un puntatore a un blocco di memoria che contiene una struttura di [**\_ elementi KSMULTIPLE**](ksmultiple-item.md) , seguita da zero o più strutture **REGPINMEDIUM** .</span><span class="sxs-lookup"><span data-stu-id="d1631-121">This method returns a pointer to a block of memory that contains a [**KSMULTIPLE\_ITEM**](ksmultiple-item.md) structure, followed by zero or more **REGPINMEDIUM** structures.</span></span> <span data-ttu-id="d1631-122">Ogni struttura **REGPINMEDIUM** identifica un supporto supportato dal pin.</span><span class="sxs-lookup"><span data-stu-id="d1631-122">Each **REGPINMEDIUM** structure identifies a medium the pin supports.</span></span>

<span data-ttu-id="d1631-123">Non connettere un PIN se il supporto presenta un CLSID di GUID \_ null o KSMEDIUMSETID \_ standard.</span><span class="sxs-lookup"><span data-stu-id="d1631-123">Do not connect a pin if the medium has a CLSID of GUID\_NULL or KSMEDIUMSETID\_Standard.</span></span> <span data-ttu-id="d1631-124">Si tratta di valori predefiniti che indicano che il PIN non supporta supporti.</span><span class="sxs-lookup"><span data-stu-id="d1631-124">These are default values indicating that the pin does not support mediums.</span></span>

<span data-ttu-id="d1631-125">Inoltre, non connettere un PIN, a meno che il filtro non richieda esattamente un'istanza connessa del PIN.</span><span class="sxs-lookup"><span data-stu-id="d1631-125">Also, do not connect a pin unless the filter requires exactly one connected instance of that pin.</span></span> <span data-ttu-id="d1631-126">In caso contrario, l'applicazione potrebbe provare a connettere diversi pin che non devono avere connessioni, il che può causare l'interruzione della risposta del programma.</span><span class="sxs-lookup"><span data-stu-id="d1631-126">Otherwise, your application might try to connect various pins that shouldn't have connections, which can cause the program to stop responding.</span></span> <span data-ttu-id="d1631-127">Per individuare il numero di istanze necessarie, recuperare il set di \_ \_ Proprietà NECESSARYINSTANCES pin KSPROPERTY, come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="d1631-127">To find out the number of required instances, retrieve the KSPROPERTY\_PIN\_NECESSARYINSTANCES property set, as shown in the following code example.</span></span> <span data-ttu-id="d1631-128">Per brevità, in questo esempio non viene testato alcun codice restituito né viene rilasciata alcuna interfaccia.</span><span class="sxs-lookup"><span data-stu-id="d1631-128">(For brevity, this example does not test any return codes or release any interfaces.</span></span> <span data-ttu-id="d1631-129">Naturalmente, l'applicazione deve eseguire entrambe le operazioni.</span><span class="sxs-lookup"><span data-stu-id="d1631-129">Your application should do both, of course.)</span></span>


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



<span data-ttu-id="d1631-130">Lo pseudocodice seguente è una struttura estremamente breve che illustra come trovare e connettere i filtri WDM.</span><span class="sxs-lookup"><span data-stu-id="d1631-130">The following pseudocode is an extremely brief outline showing how to find and connect the WDM filters.</span></span> <span data-ttu-id="d1631-131">Omette molti dettagli e ha lo scopo di illustrare solo i passaggi generali che l'applicazione deve eseguire.</span><span class="sxs-lookup"><span data-stu-id="d1631-131">It omits many details, and is only meant to show the general steps your application would need to take.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d1631-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d1631-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1631-133">Argomenti sull'acquisizione avanzata</span><span class="sxs-lookup"><span data-stu-id="d1631-133">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> </dl>

 

 



