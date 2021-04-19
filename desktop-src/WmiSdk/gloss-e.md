---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 40d26ea1-3081-4afd-8b12-bc6521fad390
ms.tgt_platform: multiple
title: E (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd162feb3936712b396db016de036f78aea35a09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317556"
---
# <a name="e-wmi"></a><span data-ttu-id="bc58e-103">E (WMI)</span><span class="sxs-lookup"><span data-stu-id="bc58e-103">E (WMI)</span></span>

<span data-ttu-id="bc58e-104">[A](gloss-a.md) B [C](gloss-c.md) [d](gloss-d.md) E [F](gloss-f.md) G [H](gloss-h.md) [i](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="bc58e-104">[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) E [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="bc58e-105"><span id="wmi.gloss_event_class"></span><span id="WMI.GLOSS_EVENT_CLASS"></span>**classe di evento**</span><span class="sxs-lookup"><span data-stu-id="bc58e-105"><span id="wmi.gloss_event_class"></span><span id="WMI.GLOSS_EVENT_CLASS"></span>**event class**</span></span>
</dt> <dd>

<span data-ttu-id="bc58e-106">Classe WMI che *i consumer di eventi* possono sottoscrivere da una *query di eventi*.</span><span class="sxs-lookup"><span data-stu-id="bc58e-106">A WMI class that *event consumers* can subscribe to by an *event query*.</span></span> <span data-ttu-id="bc58e-107">La classe segnala un tipo di occorrenza specifico.</span><span class="sxs-lookup"><span data-stu-id="bc58e-107">The class reports a specific type of occurrence.</span></span> <span data-ttu-id="bc58e-108">Ad esempio, la classe [**Win32 \_ ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace) segnala che un processo specifico è stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="bc58e-108">For example, the [**Win32\_ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace) class reports that a specific process has stopped.</span></span>

</dd> <dt>

<span data-ttu-id="bc58e-109"><span id="wmi.gloss_event_consumer"></span><span id="WMI.GLOSS_EVENT_CONSUMER"></span>**consumer di eventi**</span><span class="sxs-lookup"><span data-stu-id="bc58e-109"><span id="wmi.gloss_event_consumer"></span><span id="WMI.GLOSS_EVENT_CONSUMER"></span>**event consumer**</span></span>
</dt> <dd>

<span data-ttu-id="bc58e-110">Destinatario delle notifiche che segnalano il verificarsi di un evento.</span><span class="sxs-lookup"><span data-stu-id="bc58e-110">A recipient of notifications that report an occurrence of an event.</span></span> <span data-ttu-id="bc58e-111">Un consumer di eventi può essere [*temporaneo*](gloss-t.md) o [*permanente*](gloss-p.md).</span><span class="sxs-lookup"><span data-stu-id="bc58e-111">An event consumer is either [*temporary*](gloss-t.md) or [*permanent*](gloss-p.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc58e-112"><span id="wmi.gloss_event_consumer_provider"></span><span id="WMI.GLOSS_EVENT_CONSUMER_PROVIDER"></span>**provider di consumer di eventi**</span><span class="sxs-lookup"><span data-stu-id="bc58e-112"><span id="wmi.gloss_event_consumer_provider"></span><span id="WMI.GLOSS_EVENT_CONSUMER_PROVIDER"></span>**event consumer provider**</span></span>
</dt> <dd>

<span data-ttu-id="bc58e-113">Provider che determina il consumer di eventi permanente che gestisce un dato evento.</span><span class="sxs-lookup"><span data-stu-id="bc58e-113">A provider that determines which permanent event consumer handles a given event.</span></span> <span data-ttu-id="bc58e-114">Un provider di consumer di eventi viene registrato con WMI da un'istanza di [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md), che contiene un elenco delle classi di [*consumer logiche*](gloss-l.md) supportate dal provider di consumer di eventi.</span><span class="sxs-lookup"><span data-stu-id="bc58e-114">An event consumer provider is registered with WMI by an instance of [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md), which contains a list of the [*logical consumer*](gloss-l.md) classes that the event consumer provider supports.</span></span> <span data-ttu-id="bc58e-115">Un provider di consumer di eventi è un server COM che esegue il mapping di [*consumer fisici*](gloss-p.md) a *utenti logici*.</span><span class="sxs-lookup"><span data-stu-id="bc58e-115">An event consumer provider is a COM server that maps [*physical consumers*](gloss-p.md) to *logical consumers*.</span></span> <span data-ttu-id="bc58e-116">Un provider di consumer di eventi supporta l'interfaccia [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) ed è un componente dell'architettura del consumer permanente.</span><span class="sxs-lookup"><span data-stu-id="bc58e-116">An event consumer provider supports the [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) interface and is a component of the permanent consumer architecture.</span></span>

</dd> <dt>

<span data-ttu-id="bc58e-117"><span id="wmi.gloss_event_filter"></span><span id="WMI.GLOSS_EVENT_FILTER"></span>**filtro eventi**</span><span class="sxs-lookup"><span data-stu-id="bc58e-117"><span id="wmi.gloss_event_filter"></span><span id="WMI.GLOSS_EVENT_FILTER"></span>**event filter**</span></span>
</dt> <dd>

<span data-ttu-id="bc58e-118">Istanza della classe di sistema [**\_ \_ EventFilter**](--eventfilter.md) che descrive un tipo di evento e le condizioni per il recapito di una notifica.</span><span class="sxs-lookup"><span data-stu-id="bc58e-118">An instance of the [**\_\_EventFilter**](--eventfilter.md) system class that describes an event type and the conditions for delivering a notification.</span></span> <span data-ttu-id="bc58e-119">Un consumer utilizza un filtro eventi per eseguire la registrazione per ricevere la notifica di un tipo specifico di evento.</span><span class="sxs-lookup"><span data-stu-id="bc58e-119">A consumer uses an event filter to register to receive notification of a specific type of event.</span></span>

</dd> <dt>

<span data-ttu-id="bc58e-120"><span id="wmi.gloss_event_provider"></span><span id="WMI.GLOSS_EVENT_PROVIDER"></span>**provider di eventi**</span><span class="sxs-lookup"><span data-stu-id="bc58e-120"><span id="wmi.gloss_event_provider"></span><span id="WMI.GLOSS_EVENT_PROVIDER"></span>**event provider**</span></span>
</dt> <dd>

<span data-ttu-id="bc58e-121">Provider WMI che monitora un'origine di eventi e notifica a WMI quando si verificano gli eventi.</span><span class="sxs-lookup"><span data-stu-id="bc58e-121">A WMI provider that monitors a source of events and notifies WMI when events occur.</span></span> <span data-ttu-id="bc58e-122">Un provider di eventi implementa le interfacce [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) e [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) e talvolta [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink).</span><span class="sxs-lookup"><span data-stu-id="bc58e-122">An event provider implements the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) interfaces, and sometimes [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink).</span></span>

</dd> <dt>

<span data-ttu-id="bc58e-123"><span id="wmi.gloss_event_query"></span><span id="WMI.GLOSS_EVENT_QUERY"></span>**query di eventi**</span><span class="sxs-lookup"><span data-stu-id="bc58e-123"><span id="wmi.gloss_event_query"></span><span id="WMI.GLOSS_EVENT_QUERY"></span>**event query**</span></span>
</dt> <dd>

<span data-ttu-id="bc58e-124">Istruzione [*WMI Query Language*](gloss-w.md) utilizzata dai consumer di eventi per la registrazione per la ricezione di notifiche di eventi specifici.</span><span class="sxs-lookup"><span data-stu-id="bc58e-124">A [*WMI Query Language*](gloss-w.md) statement that event consumers use to register to receive notification of specific events.</span></span> <span data-ttu-id="bc58e-125">Un provider di eventi utilizza una query di eventi per eseguire la registrazione per generare notifiche di specifici eventi.</span><span class="sxs-lookup"><span data-stu-id="bc58e-125">An event provider uses an event query to register to generate notifications of specific events.</span></span>

</dd> <dt>

<span data-ttu-id="bc58e-126"><span id="wmi.gloss_extension_schema"></span><span id="WMI.GLOSS_EXTENSION_SCHEMA"></span>**schema estensione**</span><span class="sxs-lookup"><span data-stu-id="bc58e-126"><span id="wmi.gloss_extension_schema"></span><span id="WMI.GLOSS_EXTENSION_SCHEMA"></span>**extension schema**</span></span>
</dt> <dd>

<span data-ttu-id="bc58e-127">Terzo livello dello [*schema CIM*](gloss-c.md), che include le estensioni specifiche della piattaforma dello schema CIM, ad esempio Windows, UNIX ed Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="bc58e-127">The third layer of the [*CIM schema*](gloss-c.md), which includes platform-specific extensions of the CIM schema such as Windows, UNIX, and Exchange Server.</span></span> <span data-ttu-id="bc58e-128">Vedere anche modello [*comune*](gloss-c.md) e modello di base.</span><span class="sxs-lookup"><span data-stu-id="bc58e-128">Also see [*common model*](gloss-c.md) and core model.</span></span>

</dd> <dt>

<span data-ttu-id="bc58e-129"><span id="wmi.gloss_extrinsic_event"></span><span id="WMI.GLOSS_EXTRINSIC_EVENT"></span>**evento estrinseco**</span><span class="sxs-lookup"><span data-stu-id="bc58e-129"><span id="wmi.gloss_extrinsic_event"></span><span id="WMI.GLOSS_EXTRINSIC_EVENT"></span>**extrinsic event**</span></span>
</dt> <dd>

<span data-ttu-id="bc58e-130">Notifica degli eventi da un provider.</span><span class="sxs-lookup"><span data-stu-id="bc58e-130">An event notification from a provider.</span></span> <span data-ttu-id="bc58e-131">La maggior parte dei provider crea un'istanza di una classe di evento definita nei file MOF del provider.</span><span class="sxs-lookup"><span data-stu-id="bc58e-131">Most providers create an instance of an event class defined in the provider MOF files.</span></span> <span data-ttu-id="bc58e-132">Un evento estrinseco eredita da [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md).</span><span class="sxs-lookup"><span data-stu-id="bc58e-132">An extrinsic event inherits from [**\_\_ExtrinsicEvent**](--extrinsicevent.md).</span></span> <span data-ttu-id="bc58e-133">Il [provider del registro eventi](/previous-versions/windows/desktop/eventlogprov/event-log-provider) , ad esempio, definisce la classe di evento [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span><span class="sxs-lookup"><span data-stu-id="bc58e-133">For example, the [Event Log Provider](/previous-versions/windows/desktop/eventlogprov/event-log-provider) defines the event class [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span></span> <span data-ttu-id="bc58e-134">Vedere anche [*evento intrinseco*](gloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="bc58e-134">Also see [*intrinsic event*](gloss-i.md).</span></span>

</dd> </dl>

 

 
