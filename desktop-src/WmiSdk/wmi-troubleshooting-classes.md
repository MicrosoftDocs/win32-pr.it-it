---
description: WMI fornisce un set di classi di risoluzione dei problemi che gli script e le applicazioni possono utilizzare per ottenere informazioni sullo stato interno WMI durante le operazioni di base e del provider WMI.
ms.assetid: 631e0cce-0e83-42e5-a381-e96b1f70d6f9
ms.tgt_platform: multiple
title: Classi di risoluzione dei problemi WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65b3972ba59c80a1495916ab24a72f6e93bef8e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968547"
---
# <a name="wmi-troubleshooting-classes"></a><span data-ttu-id="6c6eb-103">Classi di risoluzione dei problemi WMI</span><span class="sxs-lookup"><span data-stu-id="6c6eb-103">WMI Troubleshooting Classes</span></span>

<span data-ttu-id="6c6eb-104">WMI fornisce un set di classi di risoluzione dei problemi che gli script e le applicazioni possono utilizzare per ottenere informazioni sullo stato interno WMI durante le operazioni di base e del provider WMI.</span><span class="sxs-lookup"><span data-stu-id="6c6eb-104">WMI supplies a set of troubleshooting classes that scripts and applications can use to get information about WMI internal state during WMI core and provider operations.</span></span> <span data-ttu-id="6c6eb-105">Per ulteriori informazioni sulla risoluzione dei problemi relativi a WMI, vedere la pagina relativa alla risoluzione dei problemi e alle [classi](provider-configuration-and-troubleshooting-classes.md)di risoluzione dei problemi di [WMI](wmi-troubleshooting.md) .</span><span class="sxs-lookup"><span data-stu-id="6c6eb-105">For more information about WMI troubleshooting, see [WMI Troubleshooting](wmi-troubleshooting.md) and [Provider Configuration and Troubleshooting Classes](provider-configuration-and-troubleshooting-classes.md).</span></span>

<span data-ttu-id="6c6eb-106">WMI include diverse classi di risoluzione dei problemi di base per le operazioni di base e del provider WMI:</span><span class="sxs-lookup"><span data-stu-id="6c6eb-106">WMI has several basic troubleshooting classes for WMI core and provider operations:</span></span>

-   [<span data-ttu-id="6c6eb-107">**\_Contatori provider WMI \_ MSFT**</span><span class="sxs-lookup"><span data-stu-id="6c6eb-107">**MSFT\_WmiProvider\_Counters**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-counters)

    <span data-ttu-id="6c6eb-108">In ogni computer viene individuata solo una di queste classi.</span><span class="sxs-lookup"><span data-stu-id="6c6eb-108">Only one of these classes is found on each computer system.</span></span> <span data-ttu-id="6c6eb-109">Fornisce i conteggi di diversi tipi di operazioni del provider nel sistema.</span><span class="sxs-lookup"><span data-stu-id="6c6eb-109">It provides counts of various kind of provider operations on that system.</span></span>

-   [<span data-ttu-id="6c6eb-110">**MSFT \_ WmiSelfEvent**</span><span class="sxs-lookup"><span data-stu-id="6c6eb-110">**MSFT\_WmiSelfEvent**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)

    <span data-ttu-id="6c6eb-111">Le classi di risoluzione dei problemi degli eventi derivano da [**MSFT \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent).</span><span class="sxs-lookup"><span data-stu-id="6c6eb-111">The event troubleshooting classes derive from [**MSFT\_WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent).</span></span> <span data-ttu-id="6c6eb-112">Le query di questa classe restituiscono istanze delle classi di evento, ad esempio [**MSFT \_ WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated) o [**MSFT \_ provider WMI \_ CreateInstanceEnumAsyncEvent \_ post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-post).</span><span class="sxs-lookup"><span data-stu-id="6c6eb-112">Queries of this class return instances of event classes such as [**MSFT\_WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated) or [**MSFT\_WmiProvider\_CreateInstanceEnumAsyncEvent\_Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-post).</span></span>

    <span data-ttu-id="6c6eb-113">Nell'elenco seguente vengono forniti i collegamenti a diverse categorie di classi di evento derivate da [**MSFT \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent):</span><span class="sxs-lookup"><span data-stu-id="6c6eb-113">The following list provides links to different categories of event classes derived from [**MSFT\_WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent):</span></span>

    -   [<span data-ttu-id="6c6eb-114">Classi di risoluzione dei problemi degli eventi del provider</span><span class="sxs-lookup"><span data-stu-id="6c6eb-114">Provider Event Troubleshooting Classes</span></span>](provider-event-troubleshooting-classes.md)
    -   [<span data-ttu-id="6c6eb-115">Classi di risoluzione dei problemi ConsumerProvider</span><span class="sxs-lookup"><span data-stu-id="6c6eb-115">ConsumerProvider Troubleshooting Classes</span></span>](consumerprovider-troubleshooting-classes.md)
    -   [<span data-ttu-id="6c6eb-116">Classi di risoluzione dei problemi degli eventi del servizio WMI</span><span class="sxs-lookup"><span data-stu-id="6c6eb-116">WMI Service Event Troubleshooting Classes</span></span>](wmi-service-event-troubleshooting-classes.md)

## <a name="related-topics"></a><span data-ttu-id="6c6eb-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6c6eb-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c6eb-118">Risoluzione dei problemi WMI</span><span class="sxs-lookup"><span data-stu-id="6c6eb-118">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="6c6eb-119">Ricezione di un evento WMI</span><span class="sxs-lookup"><span data-stu-id="6c6eb-119">Receiving a WMI Event</span></span>](receiving-a-wmi-event.md)
</dt> </dl>

 

 
