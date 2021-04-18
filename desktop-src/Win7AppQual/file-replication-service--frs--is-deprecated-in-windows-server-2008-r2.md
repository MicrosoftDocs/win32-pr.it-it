---
description: .
ms.assetid: 18a03469-737a-4905-9851-f7961c46b867
title: Il servizio Replica file (FRS) è deprecato in Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af3acf7eb6310f2c296abfd5eb1db0f30c4b48dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312700"
---
# <a name="file-replication-service-frs-is-deprecated-in-windows-server-2008-r2"></a><span data-ttu-id="ebd81-103">Il servizio Replica file (FRS) è deprecato in Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ebd81-103">File Replication Service (FRS) Is Deprecated in Windows Server 2008 R2</span></span>

## <a name="platform"></a><span data-ttu-id="ebd81-104">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="ebd81-104">Platform</span></span>

 <span data-ttu-id="ebd81-105">**Server-** Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ebd81-105">**Servers -** Windows Server 2008 R2</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="ebd81-106">Effetto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="ebd81-106">Feature Impact</span></span>

 <span data-ttu-id="ebd81-107">**Gravità-** Alta</span><span class="sxs-lookup"><span data-stu-id="ebd81-107">**Severity -** High</span></span>  
<span data-ttu-id="ebd81-108">**Frequenza-** Alta</span><span class="sxs-lookup"><span data-stu-id="ebd81-108">**Frequency -** High</span></span>  


## <a name="description"></a><span data-ttu-id="ebd81-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ebd81-109">Description</span></span>

<span data-ttu-id="ebd81-110">In Windows Server 2008 R2 non è possibile usare il servizio Replica file (FRS) per la replica di cartelle file system distribuito (DFS) o dati personalizzati (non SYSVOL).</span><span class="sxs-lookup"><span data-stu-id="ebd81-110">In Windows Server 2008 R2, File Replication Service (FRS) cannot be used for replicating Distributed File System (DFS) folders or custom (non-SYSVOL) data.</span></span> <span data-ttu-id="ebd81-111">Un controller di dominio Windows Server 2008 R2 può comunque utilizzare il servizio Replica file per replicare il contenuto della condivisione SYSVOL in un dominio che utilizza FRS per la replica della condivisione SYSVOL tra controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="ebd81-111">A Windows Server 2008 R2 domain controller can still use FRS to replicate the contents of the SYSVOL share in a domain that uses FRS for replicating the SYSVOL share between domain controllers.</span></span> <span data-ttu-id="ebd81-112">Tuttavia, i server Windows Server 2008 R2 non possono usare il servizio Replica file per replicare il contenuto di un set di repliche separato dalla condivisione SYSVOL.</span><span class="sxs-lookup"><span data-stu-id="ebd81-112">However, Windows Server 2008 R2 servers cannot use FRS to replicate the contents of any replica set apart from the SYSVOL share.</span></span> <span data-ttu-id="ebd81-113">Il servizio Replica DFS è una sostituzione per FRS e può essere usato per replicare il contenuto della condivisione SYSVOL, delle cartelle DFS, nonché di altri dati personalizzati (non SYSVOL).</span><span class="sxs-lookup"><span data-stu-id="ebd81-113">The DFS Replication service is a replacement for FRS and can be used to replicate the contents of the SYSVOL share, DFS folders as well as other custom (non-SYSVOL) data.</span></span> <span data-ttu-id="ebd81-114">Eseguire la migrazione di tutti i set di repliche FRS non SYSVOL a Replica DFS.</span><span class="sxs-lookup"><span data-stu-id="ebd81-114">Migrate all non-SYSVOL FRS replica sets to DFS Replication.</span></span> <span data-ttu-id="ebd81-115">Si consiglia inoltre di eseguire la migrazione della replica della condivisione SYSVOL da FRS a Replica DFS perché Replica DFS è più affidabile e scalabile e offre prestazioni di replica migliori rispetto a FRS.</span><span class="sxs-lookup"><span data-stu-id="ebd81-115">We also highly recommend that you migrate replication of the SYSVOL share from FRS to DFS Replication because DFS Replication is more robust, scalable and has better replication performance than FRS.</span></span>

## <a name="manifestation"></a><span data-ttu-id="ebd81-116">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="ebd81-116">Manifestation</span></span>

<span data-ttu-id="ebd81-117">La replica FRS dei dati personalizzati si interrompe in maniera irreversibile durante l'aggiornamento sul posto.</span><span class="sxs-lookup"><span data-stu-id="ebd81-117">FRS replication of custom data will break irreversibly upon in-place upgrade.</span></span> <span data-ttu-id="ebd81-118">L'unico modo per risolvere questo problema è reinstallare un sistema operativo precedente nel server e reinizializzare la replica FRS.</span><span class="sxs-lookup"><span data-stu-id="ebd81-118">The only way to recover from this situation would be to reinstall an older operating system on the server and reinitialize FRS replication.</span></span> <span data-ttu-id="ebd81-119">Ai server che sono stati aggiornati a Windows Server 2008 R2 non è consentito partecipare ai gruppi di replica FRS esistenti.</span><span class="sxs-lookup"><span data-stu-id="ebd81-119">Servers that have been upgraded to Windows Server 2008 R2 are not allowed to participate in existing FRS replication groups.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="ebd81-120">Attenuazione dell'effetto</span><span class="sxs-lookup"><span data-stu-id="ebd81-120">Mitigation of Impact</span></span>

<span data-ttu-id="ebd81-121">Per evitare problemi che potrebbero verificarsi in seguito a queste modifiche, eseguire la migrazione di set di replica FRS personalizzati a Replica DFS.</span><span class="sxs-lookup"><span data-stu-id="ebd81-121">To prevent issues that might occur as a result of these changes, migrate custom FRS replication sets to DFS Replication.</span></span> <span data-ttu-id="ebd81-122">Il servizio Replica DFS offre molti vantaggi rispetto a FRS, inclusi strumenti di gestione migliorati, prestazioni superiori e gestione delegata.</span><span class="sxs-lookup"><span data-stu-id="ebd81-122">The DFS Replication service has many benefits over FRS, including improved management tools, higher performance, and delegated management.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="ebd81-123">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="ebd81-123">Links to Other Resources</span></span>

-   <span data-ttu-id="ebd81-124">[Panoramica di FRS](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="ebd81-124">[FRS Overview](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))</span></span>
-   [<span data-ttu-id="ebd81-125">Replica DFS (Distributed File System): domande frequenti</span><span class="sxs-lookup"><span data-stu-id="ebd81-125">Distributed File System Replication: Frequently Asked Questions</span></span>](/windows-server/storage/dfs-replication/dfsr-faq)
-   [<span data-ttu-id="ebd81-126">Guida alla migrazione della replica SYSVOL: Replica da FRS a DFS</span><span class="sxs-lookup"><span data-stu-id="ebd81-126">SYSVOL Replication Migration Guide: FRS to DFS Replication</span></span>](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)

 

 
