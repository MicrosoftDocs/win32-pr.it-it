---
description: Un filtro eventi è una classe WMI che descrive gli eventi che WMI recapita a un consumer fisico.
ms.assetid: c0ce26a4-5ff2-44b4-8550-c7d8ad0ba0f0
ms.tgt_platform: multiple
title: Creazione di un filtro eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 693e4ef2eee5de14550b8efbf25a9b6720d6a8b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319300"
---
# <a name="creating-an-event-filter"></a><span data-ttu-id="ae8da-103">Creazione di un filtro eventi</span><span class="sxs-lookup"><span data-stu-id="ae8da-103">Creating an Event Filter</span></span>

<span data-ttu-id="ae8da-104">Un filtro eventi è una classe WMI che descrive gli eventi che WMI recapita a un consumer fisico.</span><span class="sxs-lookup"><span data-stu-id="ae8da-104">An event filter is a WMI class that describes which events WMI delivers to a physical consumer.</span></span> <span data-ttu-id="ae8da-105">Ad esempio, un filtro eventi può indicare a WMI di recapitare a un consumer tutti gli eventi di risparmio energia o tutti gli eventi di riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="ae8da-105">For example, an event filter can instruct WMI to deliver to a consumer all power management events, or all system reboot events.</span></span> <span data-ttu-id="ae8da-106">Un filtro eventi descrive inoltre le condizioni in base alle quali WMI recapita gli eventi.</span><span class="sxs-lookup"><span data-stu-id="ae8da-106">An event filter also describes the conditions under which WMI delivers the events.</span></span> <span data-ttu-id="ae8da-107">Un filtro eventi può specificare un evento intrinseco o estrinseco; e il filtro può fare riferimento a eventi che hanno origine nello spazio dei nomi, ovvero diversi dallo spazio dei nomi del filtro.</span><span class="sxs-lookup"><span data-stu-id="ae8da-107">An event filter can specify an intrinsic or extrinsic event; and the filter can refer to events that originate in the namespace—that is, other than the namespace of the filter.</span></span> <span data-ttu-id="ae8da-108">Il consumer permanente deve avere lo stesso [**CreatorSID**](--eventconsumer.md) nelle istanze consumer, Filter e binding.</span><span class="sxs-lookup"><span data-stu-id="ae8da-108">The permanent consumer must have the same [**CreatorSID**](--eventconsumer.md) in the consumer, filter, and binding instances.</span></span> <span data-ttu-id="ae8da-109">Per altre informazioni, vedere [ricezione di eventi](receiving-events-securely.md)in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="ae8da-109">For more information, see [Receiving Events Securely](receiving-events-securely.md).</span></span>

<span data-ttu-id="ae8da-110">Nella procedura seguente viene descritto come creare un filtro evento.</span><span class="sxs-lookup"><span data-stu-id="ae8da-110">The following procedure describes how to create an event filter.</span></span>

<span data-ttu-id="ae8da-111">**Per creare un filtro eventi**</span><span class="sxs-lookup"><span data-stu-id="ae8da-111">**To create an event filter**</span></span>

1.  <span data-ttu-id="ae8da-112">Creare un'istanza della classe di sistema WMI [**\_ \_ EventFilter**](--eventfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="ae8da-112">Create an instance of the WMI [**\_\_EventFilter**](--eventfilter.md) system class.</span></span>
2.  <span data-ttu-id="ae8da-113">Creare un identificatore univoco per il filtro con la proprietà **Name** , in uno dei due modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="ae8da-113">Create a unique identifier for your filter with the **Name** property, in one of two ways:</span></span>

    -   <span data-ttu-id="ae8da-114">Usare uno schema privato.</span><span class="sxs-lookup"><span data-stu-id="ae8da-114">Use a private scheme.</span></span>

        <span data-ttu-id="ae8da-115">Il nome arbitrario dei filtri eventi funziona a condizione che non si verifichino conflitti con altri schemi di denominazione dei filtri.</span><span class="sxs-lookup"><span data-stu-id="ae8da-115">Arbitrarily naming your event filters works as long as you do not conflict with other filter naming schemes.</span></span> <span data-ttu-id="ae8da-116">È necessario evitare conflitti di denominazione perché l'aggiunta di un'istanza con un valore di **nome** duplicato sovrascrive l'istanza precedente.</span><span class="sxs-lookup"><span data-stu-id="ae8da-116">You must avoid naming conflicts because adding an instance with a duplicate **Name** value overwrites the old instance.</span></span>

    -   <span data-ttu-id="ae8da-117">Usare un identificatore univoco globale (GUID).</span><span class="sxs-lookup"><span data-stu-id="ae8da-117">Use a globally unique identifier (GUID).</span></span>

        <span data-ttu-id="ae8da-118">Se si lascia il **nome** vuoto, WMI riempie il **nome** con un GUID.</span><span class="sxs-lookup"><span data-stu-id="ae8da-118">If you leave **Name** empty, WMI fills **Name** with a GUID.</span></span>

3.  <span data-ttu-id="ae8da-119">Descrivere il tipo di evento che si desidera filtrare con la proprietà di **query** .</span><span class="sxs-lookup"><span data-stu-id="ae8da-119">Describe the type of event you want filtered with the **Query** property.</span></span>

    <span data-ttu-id="ae8da-120">La proprietà **query** contiene la query WMI Query Language (WQL) che descrive il tipo di evento che si desidera filtrare.</span><span class="sxs-lookup"><span data-stu-id="ae8da-120">The **Query** property contains the WMI Query Language (WQL) query that describes the type of event you want filtered.</span></span> <span data-ttu-id="ae8da-121">È possibile ottenere un filtro preciso utilizzando diversi operatori ed estensioni di WQL.</span><span class="sxs-lookup"><span data-stu-id="ae8da-121">You can achieve precise filtering using a variety of operators and extensions to WQL.</span></span>

    <span data-ttu-id="ae8da-122">Un evento di registro NT viene generato quando si verifica un errore in una query di un consumer di eventi permanenti.</span><span class="sxs-lookup"><span data-stu-id="ae8da-122">An NT Log event is generated when a query from a permanent event consumer fails.</span></span> <span data-ttu-id="ae8da-123">L'origine dell'evento è WinMgmt, l'ID evento è 10 e il tipo di evento è Error.</span><span class="sxs-lookup"><span data-stu-id="ae8da-123">The event's source is WinMgmt, the event ID is 10, and the event type is Error.</span></span>

    <span data-ttu-id="ae8da-124">WMI è più efficiente in fase di elaborazione di query restrittive e specifiche rispetto a query ampie.</span><span class="sxs-lookup"><span data-stu-id="ae8da-124">WMI is more efficient at processing restrictive, specific queries than broad queries.</span></span> <span data-ttu-id="ae8da-125">Creando una query specifica, è possibile evitare la comunicazione tra processi non necessaria e il traffico di rete.</span><span class="sxs-lookup"><span data-stu-id="ae8da-125">By creating a specific query, you can avoid unnecessary inter-process communication and network traffic.</span></span> <span data-ttu-id="ae8da-126">Nei casi di eventi generati da un provider, WMI esegue il filtro in corso per il provider. in questo modo si garantisce che solo gli eventi corrispondenti al filtro provochino il costo di comunicazione interprocesso.</span><span class="sxs-lookup"><span data-stu-id="ae8da-126">In cases of events generated by a provider, WMI performs the filtering in process to the provider; this ensures that only events matching the filter incur the interprocess communication cost.</span></span> <span data-ttu-id="ae8da-127">Per ulteriori informazioni, vedere [esecuzione di query su WMI](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="ae8da-127">For more information, see [Querying WMI](querying-wmi.md).</span></span>

4.  <span data-ttu-id="ae8da-128">Impostare la proprietà **QueryLanguage** sul tipo di linguaggio di query utilizzato nella proprietà **query** .</span><span class="sxs-lookup"><span data-stu-id="ae8da-128">Set the **QueryLanguage** property to the type of query language you use in the **Query** property.</span></span>

    <span data-ttu-id="ae8da-129">Si imposta quasi sempre **QueryLanguage** su "WQL".</span><span class="sxs-lookup"><span data-stu-id="ae8da-129">You will almost always set **QueryLanguage** to "WQL".</span></span>

<span data-ttu-id="ae8da-130">Nell'esempio di codice riportato di seguito viene descritto un filtro eventi che segnala un evento ogni volta che WMI crea un'istanza della classe [**\_ \_ TimerEvent**](--timerevent.md) nello \\ spazio dei nomi CIMV2 radice.</span><span class="sxs-lookup"><span data-stu-id="ae8da-130">The following code example describes an event filter that signals an event each time WMI creates an instance of the [**\_\_TimerEvent**](--timerevent.md) class in the root\\cimv2 namespace.</span></span>

``` syntax
instance of __EventFilter as $FILTER
{
    Name = "MyFilterName";
    Query = "select * from __TimerEvent where TimerID=\"MyTimer\"";
    QueryLanguage = "WQL";
    EventNamespace = "\root\cimv2";

    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

<span data-ttu-id="ae8da-131">La proprietà **EventNamespace** specifica lo spazio dei nomi da cui hanno origine gli eventi.</span><span class="sxs-lookup"><span data-stu-id="ae8da-131">The **EventNamespace** property specifies the namespace from which the events originate.</span></span> <span data-ttu-id="ae8da-132">Non è necessario creare un'istanza dei filtri nello spazio dei nomi da cui hanno origine gli eventi.</span><span class="sxs-lookup"><span data-stu-id="ae8da-132">You do not have to create an instance of the filters in the namespace where the events originate.</span></span> <span data-ttu-id="ae8da-133">Se non si specifica lo spazio dei nomi, WMI crea il filtro nello spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="ae8da-133">If you do not specify the namespace, then WMI creates the filter in the default namespace.</span></span> <span data-ttu-id="ae8da-134">Le classi degli eventi intrinseci, ad esempio [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md) , sono disponibili in ogni spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="ae8da-134">The intrinsic events classes, such as [**\_\_InstanceOperationEvent**](--instanceoperationevent.md) are available in every namespace.</span></span>

<span data-ttu-id="ae8da-135">Per registrare l'utente logico per le notifiche degli eventi, è necessario associare i filtri eventi a un consumer logico.</span><span class="sxs-lookup"><span data-stu-id="ae8da-135">To register your logical consumer for event notifications, you must bind the event filters to a logical consumer.</span></span> <span data-ttu-id="ae8da-136">Per ulteriori informazioni, vedere [associazione di un filtro eventi a un consumer logico](binding-an-event-filter-with-a-logical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="ae8da-136">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md).</span></span>

 

 



