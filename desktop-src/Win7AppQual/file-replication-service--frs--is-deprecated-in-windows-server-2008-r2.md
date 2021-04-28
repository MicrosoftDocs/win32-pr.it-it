---
description: Il servizio Replica file è deprecato in Windows Server 2008 R2
ms.assetid: 18a03469-737a-4905-9851-f7961c46b867
title: Il servizio Replica file è deprecato in Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3c34e43daf8346888a32ef76d55f93ac5a563e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088369"
---
# <a name="file-replication-service-frs-is-deprecated-in-windows-server-2008-r2"></a><span data-ttu-id="834bc-103">Il servizio Replica file è deprecato in Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="834bc-103">File Replication Service (FRS) Is Deprecated in Windows Server 2008 R2</span></span>

## <a name="platform"></a><span data-ttu-id="834bc-104">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="834bc-104">Platform</span></span>

 <span data-ttu-id="834bc-105">**Server -** Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="834bc-105">**Servers -** Windows Server 2008 R2</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="834bc-106">Impatto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="834bc-106">Feature Impact</span></span>

 <span data-ttu-id="834bc-107">**Gravità:** alto</span><span class="sxs-lookup"><span data-stu-id="834bc-107">**Severity -** High</span></span>  
<span data-ttu-id="834bc-108">**Frequenza:** alto</span><span class="sxs-lookup"><span data-stu-id="834bc-108">**Frequency -** High</span></span>  


## <a name="description"></a><span data-ttu-id="834bc-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="834bc-109">Description</span></span>

<span data-ttu-id="834bc-110">In Windows Server 2008 R2 non è possibile usare il servizio Replica file (FRS) per la replica di cartelle file system distribuito (DFS) o dati personalizzati (non SYSVOL).</span><span class="sxs-lookup"><span data-stu-id="834bc-110">In Windows Server 2008 R2, File Replication Service (FRS) cannot be used for replicating Distributed File System (DFS) folders or custom (non-SYSVOL) data.</span></span> <span data-ttu-id="834bc-111">Un controller di dominio di Windows Server 2008 R2 può comunque usare il servizio Replica file per replicare il contenuto della condivisione SYSVOL in un dominio che usa il servizio Replica file per la replica della condivisione SYSVOL tra controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="834bc-111">A Windows Server 2008 R2 domain controller can still use FRS to replicate the contents of the SYSVOL share in a domain that uses FRS for replicating the SYSVOL share between domain controllers.</span></span> <span data-ttu-id="834bc-112">Tuttavia, i server Windows Server 2008 R2 non possono usare il servizio Replica file per replicare il contenuto di qualsiasi set di repliche a parte la condivisione SYSVOL.</span><span class="sxs-lookup"><span data-stu-id="834bc-112">However, Windows Server 2008 R2 servers cannot use FRS to replicate the contents of any replica set apart from the SYSVOL share.</span></span> <span data-ttu-id="834bc-113">Il Replica DFS è una sostituzione del servizio Replica file e può essere usato per replicare il contenuto della condivisione SYSVOL, delle cartelle DFS e di altri dati personalizzati (non SYSVOL).</span><span class="sxs-lookup"><span data-stu-id="834bc-113">The DFS Replication service is a replacement for FRS and can be used to replicate the contents of the SYSVOL share, DFS folders as well as other custom (non-SYSVOL) data.</span></span> <span data-ttu-id="834bc-114">Eseguire la migrazione di tutti i set di repliche FRS non SYSVOL Replica DFS.</span><span class="sxs-lookup"><span data-stu-id="834bc-114">Migrate all non-SYSVOL FRS replica sets to DFS Replication.</span></span> <span data-ttu-id="834bc-115">È anche consigliabile eseguire la migrazione della replica della condivisione SYSVOL dal servizio Replica file al Replica DFS perché Replica DFS è più affidabile, scalabile e offre prestazioni di replica migliori rispetto al servizio Replica file.</span><span class="sxs-lookup"><span data-stu-id="834bc-115">We also highly recommend that you migrate replication of the SYSVOL share from FRS to DFS Replication because DFS Replication is more robust, scalable and has better replication performance than FRS.</span></span>

## <a name="manifestation"></a><span data-ttu-id="834bc-116">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="834bc-116">Manifestation</span></span>

<span data-ttu-id="834bc-117">La replica FRS dei dati personalizzati verrà erta in modo irreversibile durante l'aggiornamento sul posto.</span><span class="sxs-lookup"><span data-stu-id="834bc-117">FRS replication of custom data will break irreversibly upon in-place upgrade.</span></span> <span data-ttu-id="834bc-118">L'unico modo per eseguire il ripristino da questa situazione è reinstallare un sistema operativo precedente nel server e reinizializzare la replica frs.</span><span class="sxs-lookup"><span data-stu-id="834bc-118">The only way to recover from this situation would be to reinstall an older operating system on the server and reinitialize FRS replication.</span></span> <span data-ttu-id="834bc-119">I server aggiornati a Windows Server 2008 R2 non possono partecipare ai gruppi di replica FRS esistenti.</span><span class="sxs-lookup"><span data-stu-id="834bc-119">Servers that have been upgraded to Windows Server 2008 R2 are not allowed to participate in existing FRS replication groups.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="834bc-120">Mitigazione dell'impatto</span><span class="sxs-lookup"><span data-stu-id="834bc-120">Mitigation of Impact</span></span>

<span data-ttu-id="834bc-121">Per evitare problemi che potrebbero verificarsi in seguito a queste modifiche, eseguire la migrazione di set di replica FRS personalizzati Replica DFS.</span><span class="sxs-lookup"><span data-stu-id="834bc-121">To prevent issues that might occur as a result of these changes, migrate custom FRS replication sets to DFS Replication.</span></span> <span data-ttu-id="834bc-122">Il Replica DFS offre numerosi vantaggi rispetto al servizio Replica file, tra cui strumenti di gestione migliorati, prestazioni superiori e gestione delegata.</span><span class="sxs-lookup"><span data-stu-id="834bc-122">The DFS Replication service has many benefits over FRS, including improved management tools, higher performance, and delegated management.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="834bc-123">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="834bc-123">Links to Other Resources</span></span>

-   <span data-ttu-id="834bc-124">[Panoramica del servizio Replica file](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="834bc-124">[FRS Overview](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))</span></span>
-   [<span data-ttu-id="834bc-125">Replica DFS (Distributed File System): domande frequenti</span><span class="sxs-lookup"><span data-stu-id="834bc-125">Distributed File System Replication: Frequently Asked Questions</span></span>](/windows-server/storage/dfs-replication/dfsr-faq)
-   [<span data-ttu-id="834bc-126">Guida alla migrazione della replica SYSVOL: Replica da FRS a DFS</span><span class="sxs-lookup"><span data-stu-id="834bc-126">SYSVOL Replication Migration Guide: FRS to DFS Replication</span></span>](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)

 

 
