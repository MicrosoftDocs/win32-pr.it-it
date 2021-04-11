---
description: Network Monitor è un componente di Microsoft Systems Management Server (SMS) usato per rilevare e risolvere i problemi relativi alle LAN, alle WAN e ai collegamenti seriali che eseguono il server di accesso remoto Microsoft (RAS).
ms.assetid: bd273439-daa2-4263-8f12-28ec988beea0
title: Informazioni su Network Monitor 2,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f447f4763e0c73dc0dcac4cf719a0bad4b61f073
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049984"
---
# <a name="about-network-monitor-21"></a><span data-ttu-id="84285-103">Informazioni su Network Monitor 2,1</span><span class="sxs-lookup"><span data-stu-id="84285-103">About Network Monitor 2.1</span></span>

<span data-ttu-id="84285-104">Network Monitor è un componente di Microsoft Systems Management Server (SMS) usato per rilevare e risolvere i problemi relativi alle LAN, alle WAN e ai collegamenti seriali che eseguono il server di accesso remoto Microsoft (RAS).</span><span class="sxs-lookup"><span data-stu-id="84285-104">Network Monitor is a component of Microsoft Systems Management Server (SMS) used to detect and troubleshoot problems on LANs, WANs, and serial links running Microsoft Remote Access Server (RAS).</span></span> <span data-ttu-id="84285-105">Network Monitor fornisce l'analisi dei dati di rete post-acquisizione.</span><span class="sxs-lookup"><span data-stu-id="84285-105">Network Monitor provides post-capture network data analysis.</span></span>

<span data-ttu-id="84285-106">Nell'analisi post-acquisizione il traffico di rete viene salvato in un file di acquisizione proprietario, in modo che i dati acquisiti possano essere analizzati in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="84285-106">In post-capture analysis, network traffic is saved in a proprietary capture file, so that the captured data can be analyzed later.</span></span> <span data-ttu-id="84285-107">In questo caso, l'analisi può essere sotto forma di [*parser*](p.md) di protocollo che scelgono tipi specifici di frame di rete e visualizzano i dati del frame nell'interfaccia utente di Network Monitor; o l'analisi può essere sotto forma di [*esperti*](e.md) che esaminano i dati di rete e visualizzano un report (gli esperti possono anche modificare i dati di rete).</span><span class="sxs-lookup"><span data-stu-id="84285-107">In this case, analysis can be in the form of protocol [*parsers*](p.md) picking out specific network frame types and displaying the frame data in the Network Monitor UI; or analysis can be in the form of [*experts*](e.md) examining the network data and displaying a report (experts may also manipulate the network data).</span></span>

<span data-ttu-id="84285-108">Network Monitor offre i seguenti tipi di funzionalità:</span><span class="sxs-lookup"><span data-stu-id="84285-108">Network Monitor provides the following types of functionality:</span></span>

-   <span data-ttu-id="84285-109">Acquisisce i dati di rete in modalità in tempo reale o ritardato.</span><span class="sxs-lookup"><span data-stu-id="84285-109">Captures network data in real-time or delayed mode.</span></span>
-   <span data-ttu-id="84285-110">Fornisce funzionalità di filtro durante l'acquisizione dei dati.</span><span class="sxs-lookup"><span data-stu-id="84285-110">Provides filtering capabilities when capturing data.</span></span>
-   <span data-ttu-id="84285-111">USA esperti e parser per l'analisi post-acquisizione dettagliata.</span><span class="sxs-lookup"><span data-stu-id="84285-111">Uses experts and parsers for detailed post-capture analysis.</span></span>

<span data-ttu-id="84285-112">Per ulteriori informazioni sulle funzionalità di Network Monitor, vedere:</span><span class="sxs-lookup"><span data-stu-id="84285-112">For more information about Network Monitor features, see:</span></span>

-   [<span data-ttu-id="84285-113">Architettura di esperti e parser</span><span class="sxs-lookup"><span data-stu-id="84285-113">Expert and Parser Architecture</span></span>](expert-and-parser-architecture.md)
-   [<span data-ttu-id="84285-114">Esperti</span><span class="sxs-lookup"><span data-stu-id="84285-114">Experts</span></span>](experts.md)
-   [<span data-ttu-id="84285-115">Parser</span><span class="sxs-lookup"><span data-stu-id="84285-115">Parsers</span></span>](parsers.md)
-   [<span data-ttu-id="84285-116">Provider di pacchetti di rete</span><span class="sxs-lookup"><span data-stu-id="84285-116">Network Packet Providers</span></span>](network-packet-providers.md)
-   [<span data-ttu-id="84285-117">BLOB Network Monitor</span><span class="sxs-lookup"><span data-stu-id="84285-117">Network Monitor BLOBs</span></span>](network-monitor-blobs.md)
-   [<span data-ttu-id="84285-118">Pagina di riferimento evento</span><span class="sxs-lookup"><span data-stu-id="84285-118">Event Reference Page</span></span>](event-reference-page.md)
-   [<span data-ttu-id="84285-119">Filtri di acquisizione</span><span class="sxs-lookup"><span data-stu-id="84285-119">Capture Filters</span></span>](capture-filters.md)

<span data-ttu-id="84285-120">**Windows Vista:** Network Monitor 2,1 e versioni precedenti non sono supportati in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="84285-120">**Windows Vista:** Network Monitor 2.1 and earlier are not supported on this platform.</span></span>

 

 



