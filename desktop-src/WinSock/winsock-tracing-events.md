---
description: Dettagli degli eventi di traccia Winsock.
ms.assetid: 246AE0BE-E8E2-4291-8BF4-577F889F055B
title: Eventi di traccia Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeabd2d06741f8dfa1f47b513a09c941ee1490b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129103"
---
# <a name="winsock-tracing-events"></a><span data-ttu-id="1de51-103">Eventi di traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="1de51-103">Winsock Tracing Events</span></span>

<span data-ttu-id="1de51-104">In questa sezione vengono descritte le informazioni dettagliate sui dettagli specifici degli eventi di traccia di Winsock.</span><span class="sxs-lookup"><span data-stu-id="1de51-104">This section describes detailed information on specific Winsock Tracing Events details.</span></span>

<span data-ttu-id="1de51-105">La traccia Winsock è una funzionalità di risoluzione dei problemi che può essere abilitata nei file binari finali per tracciare alcuni eventi socket di Windows con un sovraccarico minimo.</span><span class="sxs-lookup"><span data-stu-id="1de51-105">Winsock tracing is a troubleshooting feature that can be enabled in retail binaries to trace certain Windows socket events with minimal overhead.</span></span> <span data-ttu-id="1de51-106">Questa funzionalità consente di migliorare le funzionalità di diagnostica per gli sviluppatori e il supporto tecnico.</span><span class="sxs-lookup"><span data-stu-id="1de51-106">This feature allows for better diagnostic capabilities for developers and product support.</span></span> <span data-ttu-id="1de51-107">La traccia eventi di rete Winsock supporta la traccia di operazioni socket per le applicazioni IPv4 e IPv6.</span><span class="sxs-lookup"><span data-stu-id="1de51-107">Winsock network event tracing supports tracing socket operations for IPv4 and IPv6 applications.</span></span> <span data-ttu-id="1de51-108">La traccia delle modifiche del catalogo Winsock supporta la traccia delle modifiche apportate al catalogo Winsock dai provider di servizi a più livelli (LSP).</span><span class="sxs-lookup"><span data-stu-id="1de51-108">Winsock catalog change tracing supports tracing changes made to the Winsock catalog by layered service providers (LSPs).</span></span>

> [!Note]  
> <span data-ttu-id="1de51-109">I provider di servizi sovrapposti sono deprecati.</span><span class="sxs-lookup"><span data-stu-id="1de51-109">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="1de51-110">A partire da Windows 8 e Windows Server 2012, usare la [piattaforma filtro Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="1de51-110">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="1de51-111">La traccia Winsock utilizza Event Tracing for Windows (ETW), una funzionalità di traccia a utilizzo generale e ad alta velocità fornita dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1de51-111">Winsock tracing uses Event Tracing for Windows (ETW), a general-purpose, high-speed tracing facility provided by the operating system.</span></span> <span data-ttu-id="1de51-112">ETW fornisce un meccanismo di traccia per gli eventi generati da applicazioni in modalità utente e driver di dispositivo in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="1de51-112">ETW provides a tracing mechanism for events raised by both user-mode applications and kernel-mode device drivers.</span></span> <span data-ttu-id="1de51-113">ETW può abilitare e disabilitare la registrazione in modo dinamico, semplificando l'esecuzione di analisi dettagliate negli ambienti di produzione senza richiedere riavvii o riavvii di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1de51-113">ETW can enable and disable logging dynamically, making it easy to perform detailed tracing in production environments without requiring reboots or application restarts.</span></span> <span data-ttu-id="1de51-114">Il supporto per la traccia Winsock mediante ETW è stato aggiunto in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="1de51-114">Support for Winsock tracing using ETW was added on Windows Vista and later.</span></span> <span data-ttu-id="1de51-115">Per informazioni generali su ETW, vedere [migliorare il debug e l'ottimizzazione delle prestazioni con ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).</span><span class="sxs-lookup"><span data-stu-id="1de51-115">For general information on ETW, see [Improve Debugging And Performance Tuning With ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).</span></span>

<span data-ttu-id="1de51-116">Nell'elenco seguente vengono fornite informazioni dettagliate per ogni evento di traccia Winsock.</span><span class="sxs-lookup"><span data-stu-id="1de51-116">The following list provides detailed information for each Winsock tracing event.</span></span> <span data-ttu-id="1de51-117">Per ulteriori informazioni su qualsiasi evento, fare clic sul nome dell'evento.</span><span class="sxs-lookup"><span data-stu-id="1de51-117">For additional information on any event, click the event name.</span></span>



| <span data-ttu-id="1de51-118">Nome evento</span><span class="sxs-lookup"><span data-stu-id="1de51-118">Event Name</span></span>                                                            | <span data-ttu-id="1de51-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1de51-119">Description</span></span>                                                                               |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1de51-120">**\_creazione evento \_ AFD**</span><span class="sxs-lookup"><span data-stu-id="1de51-120">**AFD\_EVENT\_CREATE**</span></span>](afd-event-create.md)                        | <span data-ttu-id="1de51-121">Evento di traccia di rete Winsock per un'operazione di creazione del socket.</span><span class="sxs-lookup"><span data-stu-id="1de51-121">Winsock network tracing event for a socket creation operation.</span></span>                            |
| [<span data-ttu-id="1de51-122">**\_chiusura evento \_ AFD**</span><span class="sxs-lookup"><span data-stu-id="1de51-122">**AFD\_EVENT\_CLOSE**</span></span>](afd-event-close.md)                          | <span data-ttu-id="1de51-123">Evento di traccia di rete Winsock per l'operazione di chiusura del socket.</span><span class="sxs-lookup"><span data-stu-id="1de51-123">Winsock network tracing event for socket close operation.</span></span>                                 |
| [<span data-ttu-id="1de51-124">**Installazione di WINSOCK \_ ws2help \_ LSP \_**</span><span class="sxs-lookup"><span data-stu-id="1de51-124">**WINSOCK\_WS2HELP\_LSP\_INSTALL**</span></span>](winsock-ws2help-lsp-install.md) | <span data-ttu-id="1de51-125">Evento di modifica del catalogo Winsock per un'operazione di installazione di un provider di servizi a più livelli (LSP).</span><span class="sxs-lookup"><span data-stu-id="1de51-125">Winsock catalog change event for a layered service provider (LSP) installation operation.</span></span> |
| [<span data-ttu-id="1de51-126">**Rimozione di WINSOCK \_ ws2help \_ LSP \_**</span><span class="sxs-lookup"><span data-stu-id="1de51-126">**WINSOCK\_WS2HELP\_LSP\_REMOVE**</span></span>](winsock-ws2help-lsp-remove.md)   | <span data-ttu-id="1de51-127">Evento di modifica del catalogo Winsock per un'operazione di rimozione di un provider di servizi a più livelli (LSP).</span><span class="sxs-lookup"><span data-stu-id="1de51-127">Winsock catalog change event for a layered service provider (LSP) removal operation.</span></span>      |
| [<span data-ttu-id="1de51-128">**\_Disabilitare ws2help \_ LSP di Winsock \_**</span><span class="sxs-lookup"><span data-stu-id="1de51-128">**WINSOCK\_WS2HELP\_LSP\_DISABLE**</span></span>](winsock-ws2help-lsp-disable.md) | <span data-ttu-id="1de51-129">Evento di modifica del catalogo Winsock per un'operazione di disabilitazione di un provider di servizi a più livelli (LSP).</span><span class="sxs-lookup"><span data-stu-id="1de51-129">Winsock catalog change event for a layered service provider (LSP) disable operation.</span></span>      |
| [<span data-ttu-id="1de51-130">**Reimpostazione di WINSOCK \_ ws2help \_ LSP \_**</span><span class="sxs-lookup"><span data-stu-id="1de51-130">**WINSOCK\_WS2HELP\_LSP\_RESET**</span></span>](winsock-ws2help-lsp-reset.md)     | <span data-ttu-id="1de51-131">Evento di modifica del catalogo Winsock per un'operazione di reimpostazione del catalogo Winsock.</span><span class="sxs-lookup"><span data-stu-id="1de51-131">Winsock catalog change event for a Winsock catalog reset operation.</span></span>                       |



 

## <a name="related-topics"></a><span data-ttu-id="1de51-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1de51-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1de51-133">Migliorare il debug e la regolazione delle prestazioni con ETW</span><span class="sxs-lookup"><span data-stu-id="1de51-133">Improve Debugging And Performance Tuning With ETW</span></span>](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[<span data-ttu-id="1de51-134">Traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="1de51-134">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="1de51-135">Livelli di traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="1de51-135">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="1de51-136">Controllo della traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="1de51-136">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="1de51-137">Dettagli traccia eventi di rete Winsock</span><span class="sxs-lookup"><span data-stu-id="1de51-137">Winsock Network Event Tracing Details</span></span>](winsock-tracing-event-details.md)
</dt> <dt>

[<span data-ttu-id="1de51-138">Dettagli della traccia delle modifiche del catalogo Winsock</span><span class="sxs-lookup"><span data-stu-id="1de51-138">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
