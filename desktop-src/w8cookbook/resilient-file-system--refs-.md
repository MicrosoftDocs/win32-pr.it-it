---
title: file system resiliente
description: file system resiliente
ms.assetid: 6E5532F9-64BC-4DD7-9873-3FE4E4DE2DD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dba011dcdd3cd39280e0a79d0b325f9e75d6b64
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/10/2020
ms.locfileid: "104047539"
---
# <a name="resilient-file-system"></a><span data-ttu-id="8ad8f-103">file system resiliente</span><span class="sxs-lookup"><span data-stu-id="8ad8f-103">Resilient file system</span></span>

## <a name="platform"></a><span data-ttu-id="8ad8f-104">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="8ad8f-104">Platform</span></span>

<span data-ttu-id="8ad8f-105">**Server** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8ad8f-105">**Servers** – Windows Server 2012</span></span> 

## <a name="description"></a><span data-ttu-id="8ad8f-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ad8f-106">Description</span></span>

<span data-ttu-id="8ad8f-107">Resilient file System (ReFS) è un nuovo file system locale.</span><span class="sxs-lookup"><span data-stu-id="8ad8f-107">Resilient File System (ReFS) is a new local file system.</span></span> <span data-ttu-id="8ad8f-108">Ottimizza la disponibilità dei dati, nonostante gli errori che potrebbero causare la perdita di dati o tempi di inattività.</span><span class="sxs-lookup"><span data-stu-id="8ad8f-108">It maximizes data availability, despite errors that would historically cause data loss or downtime.</span></span> <span data-ttu-id="8ad8f-109">L'integrità dei dati garantisce che i dati aziendali critici siano protetti da errori e disponibili quando necessario.</span><span class="sxs-lookup"><span data-stu-id="8ad8f-109">Data integrity ensures that business critical data is protected from errors and available when needed.</span></span> <span data-ttu-id="8ad8f-110">La sua architettura è progettata per fornire scalabilità e prestazioni in un'era di dimensioni dei set di dati costantemente crescenti e di carichi di lavoro dinamici.</span><span class="sxs-lookup"><span data-stu-id="8ad8f-110">Its architecture is designed to provide scalability and performance in an era of constantly growing data set sizes and dynamic workloads.</span></span>

<span data-ttu-id="8ad8f-111">Le funzionalità principali di ReFS sono:</span><span class="sxs-lookup"><span data-stu-id="8ad8f-111">The key features of ReFS are:</span></span>

-   <span data-ttu-id="8ad8f-112">**Integrità**: refs archivia i dati in modo che siano protetti da molti degli errori comuni che possono causare la perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="8ad8f-112">**Integrity**: ReFS stores data so that it is protected from many of the common errors that can cause data loss.</span></span> <span data-ttu-id="8ad8f-113">I metadati del file System sono sempre protetti.</span><span class="sxs-lookup"><span data-stu-id="8ad8f-113">File system metadata is always protected.</span></span> <span data-ttu-id="8ad8f-114">Facoltativamente, i dati utente possono essere protetti in base al volume, alla directory o al file.</span><span class="sxs-lookup"><span data-stu-id="8ad8f-114">Optionally, user data can be protected on a per-volume, per-directory, or per-file basis.</span></span> <span data-ttu-id="8ad8f-115">Se si verificano danneggiamenti, ReFS può rilevare e, se configurato con spazi di archiviazione, correggere automaticamente il danneggiamento.</span><span class="sxs-lookup"><span data-stu-id="8ad8f-115">If corruption occurs, ReFS can detect and, when configured with Storage Spaces, automatically correct the corruption.</span></span> <span data-ttu-id="8ad8f-116">In caso di errore di sistema, ReFS è progettato per il ripristino rapido da tale errore, senza perdita di dati utente.</span><span class="sxs-lookup"><span data-stu-id="8ad8f-116">In the event of a system error, ReFS is designed to recover from that error rapidly, with no loss of user data.</span></span>
-   <span data-ttu-id="8ad8f-117">**Disponibilità**: refs è progettato per definire la priorità della disponibilità dei dati.</span><span class="sxs-lookup"><span data-stu-id="8ad8f-117">**Availability**: ReFS is designed to prioritize the availability of data.</span></span> <span data-ttu-id="8ad8f-118">Con ReFS, in caso di danneggiamento e non può essere riparato automaticamente, il processo di recupero online viene localizzato nell'area di danneggiamento, che non richiede il tempo di inattività del volume.</span><span class="sxs-lookup"><span data-stu-id="8ad8f-118">With ReFS, if corruption occurs, and it cannot be repaired automatically, the online salvage process is localized to the area of corruption, requiring no volume down-time.</span></span> <span data-ttu-id="8ad8f-119">In breve, se si verificano danneggiamenti, ReFS resterà online.</span><span class="sxs-lookup"><span data-stu-id="8ad8f-119">In short, if corruption occurs, ReFS will stay online.</span></span>
-   <span data-ttu-id="8ad8f-120">**Scalabilità**: refs è progettato per le dimensioni dei set di dati attuali e per le dimensioni dei set di dati di domani; è ottimizzato per la scalabilità elevata.</span><span class="sxs-lookup"><span data-stu-id="8ad8f-120">**Scalability**: ReFS is designed for the data set sizes of today and the data set sizes of tomorrow; it’s optimized for high scalability.</span></span>
-   <span data-ttu-id="8ad8f-121">**Compatibilità delle app**: per massimizzare AppCompat, refs supporta un sottoinsieme di funzionalità NTFS, oltre ad API Win32 ampiamente adottate.</span><span class="sxs-lookup"><span data-stu-id="8ad8f-121">**App Compatibility**: To maximize AppCompat, ReFS supports a subset of NTFS features plus Win32 APIs that are widely adopted.</span></span>
-   <span data-ttu-id="8ad8f-122">**Identificazione proattiva degli errori**: le funzionalità di integrità di refs vengono sfruttate da uno scanner di integrità dei dati (uno "scrubber") che analizza periodicamente il volume, tenta di identificare il danneggiamento latente e quindi attiva in modo proattivo un ripristino dei dati danneggiati.</span><span class="sxs-lookup"><span data-stu-id="8ad8f-122">**Proactive Error Identification**: The integrity capabilities of ReFS are leveraged by a data integrity scanner (a “scrubber”) that periodically scans the volume, attempts to identify latent corruption, and then proactively triggers a repair of that corrupt data.</span></span>

## <a name="resources"></a><span data-ttu-id="8ad8f-123">Risorse</span><span class="sxs-lookup"><span data-stu-id="8ad8f-123">Resources</span></span>

-   [<span data-ttu-id="8ad8f-124">Creazione di un post di Blog su Windows 8-Creazione di una nuova generazione file system per Windows: ReFS</span><span class="sxs-lookup"><span data-stu-id="8ad8f-124">Building Windows 8 Blog Post – Building the next generation file system for Windows: ReFS</span></span>](/archive/blogs/b8/building-the-next-generation-file-system-for-windows-refs)
-   [<span data-ttu-id="8ad8f-125">Compatibilità delle applicazioni e ReFS</span><span class="sxs-lookup"><span data-stu-id="8ad8f-125">Application Compatibility and ReFS</span></span>](https://www.microsoft.com/download/en/details.aspx?id=29043)

 

 