---
description: Nell'infrastruttura WMI, il servizio WMI (Winmgmt) è il componente del sistema operativo che funge da Mediator tra le applicazioni di gestione e i provider di dati WMI. Il repository WMI è un'area di archiviazione per i dati statici correlati a WMI.
ms.assetid: 6ef157be-fb75-4453-bc20-4568a3dc18c0
ms.tgt_platform: multiple
title: Infrastruttura WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4370af9ec062ffa845d54eafda054357a76dc07c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310336"
---
# <a name="wmi-infrastructure"></a><span data-ttu-id="2e185-104">Infrastruttura WMI</span><span class="sxs-lookup"><span data-stu-id="2e185-104">WMI Infrastructure</span></span>

<span data-ttu-id="2e185-105">Nell'infrastruttura WMI, il servizio WMI (Winmgmt) è il componente del sistema operativo che funge da Mediator tra le applicazioni di gestione e i [*provider*](gloss-p.md)di dati WMI.</span><span class="sxs-lookup"><span data-stu-id="2e185-105">In the WMI infrastructure, the WMI service (Winmgmt) is the operating system component that acts as the mediator between management applications and WMI data [*providers*](gloss-p.md).</span></span> <span data-ttu-id="2e185-106">Il [*repository WMI*](gloss-w.md) è un'area di archiviazione per i dati statici correlati a WMI.</span><span class="sxs-lookup"><span data-stu-id="2e185-106">The [*WMI repository*](gloss-w.md) is a storage area for WMI-related static data.</span></span>

<span data-ttu-id="2e185-107">Il servizio WMI viene implementato come processo del servizio all'interno di un processo host del servizio condiviso (SVCHOST).</span><span class="sxs-lookup"><span data-stu-id="2e185-107">The WMI service is implemented as a service process within a shared service host process (SVCHOST).</span></span> <span data-ttu-id="2e185-108">Per altre informazioni, vedere [hosting e sicurezza del provider](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="2e185-108">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

<span data-ttu-id="2e185-109">Il servizio WMI viene avviato quando il primo script o un'applicazione di gestione effettua una chiamata per connettersi a uno spazio dei nomi WMI.</span><span class="sxs-lookup"><span data-stu-id="2e185-109">The WMI service starts when the first management application or script makes a call to connect to a WMI namespace.</span></span> <span data-ttu-id="2e185-110">A seconda della configurazione, il servizio WMI potrebbe arrestarsi o passare a un profilo di memoria insufficiente quando non viene chiamato da un'applicazione di gestione.</span><span class="sxs-lookup"><span data-stu-id="2e185-110">Depending on the setup, the WMI service may shut down or go into a low memory profile when not being called by a management application.</span></span>

<span data-ttu-id="2e185-111">Il servizio WMI interagisce con le applicazioni di gestione tramite l'interfaccia COM.</span><span class="sxs-lookup"><span data-stu-id="2e185-111">The WMI service interacts with management applications through the COM interface.</span></span> <span data-ttu-id="2e185-112">Quando un'applicazione effettua una richiesta tramite l'interfaccia, WMI determina se la richiesta è per i dati statici o dinamici.</span><span class="sxs-lookup"><span data-stu-id="2e185-112">When an application makes a request through the interface, WMI determines whether the request is for static or dynamic data.</span></span> <span data-ttu-id="2e185-113">Se la richiesta prevede dati statici, ad esempio il nome di un oggetto gestito, WMI recupera i dati dal repository.</span><span class="sxs-lookup"><span data-stu-id="2e185-113">If the request involves static data, such as the name of a managed object, WMI retrieves the data from the repository.</span></span> <span data-ttu-id="2e185-114">Se la richiesta prevede dati dinamici, ad esempio la quantità di memoria attualmente utilizzata da un oggetto gestito, WMI passa la richiesta a un provider.</span><span class="sxs-lookup"><span data-stu-id="2e185-114">If the request involves dynamic data, such as the amount of memory a managed object is currently using, WMI passes the request on to a provider.</span></span>

<span data-ttu-id="2e185-115">I provider registrano il proprio percorso con il servizio WMI, che consente a WMI di instradare le richieste di dati.</span><span class="sxs-lookup"><span data-stu-id="2e185-115">Providers register their location with the WMI service, which allows WMI to route data requests.</span></span> <span data-ttu-id="2e185-116">Un provider registra anche il supporto per operazioni specifiche, ad esempio il recupero dei dati, la modifica, l'eliminazione, l'enumerazione o l'elaborazione delle query.</span><span class="sxs-lookup"><span data-stu-id="2e185-116">A provider also registers support for particular operations, such as data retrieval, modification, deletion, enumeration, or query processing.</span></span> <span data-ttu-id="2e185-117">Il servizio WMI utilizza le informazioni di registrazione del provider per soddisfare le richieste dell'applicazione con il provider appropriato.</span><span class="sxs-lookup"><span data-stu-id="2e185-117">The WMI service uses the provider registration information to match application requests with the appropriate provider.</span></span> <span data-ttu-id="2e185-118">WMI utilizza inoltre le informazioni di registrazione per caricare e scaricare i provider, a seconda delle esigenze.</span><span class="sxs-lookup"><span data-stu-id="2e185-118">WMI also uses the registration information to load and unload providers, as necessary.</span></span> <span data-ttu-id="2e185-119">Al termine dell'elaborazione di una richiesta da parte di un provider, il provider restituisce il risultato al servizio WMI.</span><span class="sxs-lookup"><span data-stu-id="2e185-119">When a provider finishes processing a request, the provider returns the result back to the WMI service.</span></span> <span data-ttu-id="2e185-120">WMI quindi trasmette il risultato all'applicazione tramite l'interfaccia COM.</span><span class="sxs-lookup"><span data-stu-id="2e185-120">WMI then forwards the result on to the application through the COM interface.</span></span> <span data-ttu-id="2e185-121">Per ulteriori informazioni, vedere la pagina relativa [alla fornitura di dati a WMI](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="2e185-121">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="2e185-122">WMI utilizza la [traccia eventi](/windows/desktop/ETW/event-tracing-portal) (ETW) per registrare l'attività del servizio WMI.</span><span class="sxs-lookup"><span data-stu-id="2e185-122">WMI uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) to record WMI service activity.</span></span>

<span data-ttu-id="2e185-123">Poiché l'infrastruttura gestisce tutto il traffico tra i provider e le applicazioni di gestione, l'infrastruttura fornisce le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="2e185-123">Because the infrastructure handles all traffic between the providers and the management applications, the infrastructure provides the following features:</span></span>

-   <span data-ttu-id="2e185-124">Supporto delle notifiche degli eventi</span><span class="sxs-lookup"><span data-stu-id="2e185-124">Event Notification Support</span></span>

    <span data-ttu-id="2e185-125">Per ulteriori informazioni, vedere [monitoraggio degli eventi](monitoring-events.md).</span><span class="sxs-lookup"><span data-stu-id="2e185-125">For more information, see [Monitoring Events](monitoring-events.md).</span></span>

-   <span data-ttu-id="2e185-126">Supporto del linguaggio di query</span><span class="sxs-lookup"><span data-stu-id="2e185-126">Query Language Support</span></span>

    <span data-ttu-id="2e185-127">Per ulteriori informazioni, vedere [esecuzione di query con WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="2e185-127">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>

-   <span data-ttu-id="2e185-128">Supporto per la sicurezza</span><span class="sxs-lookup"><span data-stu-id="2e185-128">Security Support</span></span>

    <span data-ttu-id="2e185-129">Per ulteriori informazioni, vedere [gestione della sicurezza WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="2e185-129">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

-   <span data-ttu-id="2e185-130">Creazione di script per l'accesso ai dati dei contatori delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="2e185-130">Scripting Access to Performance Counter Data</span></span>

    <span data-ttu-id="2e185-131">Per ulteriori informazioni, vedere [monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="2e185-131">For more information, see [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e185-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2e185-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e185-133">Architettura WMI</span><span class="sxs-lookup"><span data-stu-id="2e185-133">WMI Architecture</span></span>](wmi-architecture.md)
</dt> </dl>

 

 
