---
description: Per abilitare il trasferimento dei file dell'applicazione, COMREPL gestisce automaticamente i set di cartelle file system nell'origine e nella destinazione. Queste cartelle di COMREPL sono tutte radicate nella replica% systemdir% \\ com \\ .
ms.assetid: 8c59577b-34ea-4675-aaea-a2732fd5ce14
title: Gestione file (Servizi componenti)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e785b8fd39d94bcf623810bca950862d22ec8762
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523426"
---
# <a name="file-management"></a><span data-ttu-id="6130b-104">Gestione dei file</span><span class="sxs-lookup"><span data-stu-id="6130b-104">File Management</span></span>

<span data-ttu-id="6130b-105">Per abilitare il trasferimento dei file dell'applicazione, COMREPL gestisce automaticamente i set di cartelle file system nell'origine e nella destinazione.</span><span class="sxs-lookup"><span data-stu-id="6130b-105">To enable the transfer of application files, COMREPL automatically manages sets of file system folders on the source and target.</span></span> <span data-ttu-id="6130b-106">Queste cartelle di COMREPL sono tutte radicate nella replica% systemdir% \\ com \\ .</span><span class="sxs-lookup"><span data-stu-id="6130b-106">These COMREPL folders are all rooted in %systemdir%\\com\\replication.</span></span>

## <a name="source-folders"></a><span data-ttu-id="6130b-107">Cartelle di origine</span><span class="sxs-lookup"><span data-stu-id="6130b-107">Source folders</span></span>



| <span data-ttu-id="6130b-108">Cartella</span><span class="sxs-lookup"><span data-stu-id="6130b-108">Folder</span></span>                   | <span data-ttu-id="6130b-109">Scopo</span><span class="sxs-lookup"><span data-stu-id="6130b-109">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6130b-110">ReplicaSource</span><span class="sxs-lookup"><span data-stu-id="6130b-110">ReplicaSource</span></span><br/> | <span data-ttu-id="6130b-111">Le applicazioni esportate durante la fase di preparazione vengono archiviate qui.</span><span class="sxs-lookup"><span data-stu-id="6130b-111">Applications exported during the prepare phase are stored here.</span></span><br/> <span data-ttu-id="6130b-112">Questa cartella viene sovrascritta ogni volta che la fase di preparazione viene eseguita su un computer di origine specifico.</span><span class="sxs-lookup"><span data-stu-id="6130b-112">This folder is overwritten each time the prepare phase is executed against a given source computer.</span></span> <span data-ttu-id="6130b-113">Questa cartella non viene mai eliminata in modo esplicito, quindi la replica sulle destinazioni può avvenire in qualsiasi momento dopo la preparazione dell'origine.</span><span class="sxs-lookup"><span data-stu-id="6130b-113">This folder is never explicitly deleted, so replication to targets can take place at any time after the source is prepared.</span></span><br/> <span data-ttu-id="6130b-114">Ogni applicazione viene archiviata nella propria sottocartella denominata <appName> + <appID> .</span><span class="sxs-lookup"><span data-stu-id="6130b-114">Each application is stored in its own subfolder named <appName>+<appID>.</span></span><br/> |



 

## <a name="target-folders"></a><span data-ttu-id="6130b-115">Cartelle di destinazione</span><span class="sxs-lookup"><span data-stu-id="6130b-115">Target folders</span></span>



| <span data-ttu-id="6130b-116">Cartella</span><span class="sxs-lookup"><span data-stu-id="6130b-116">Folder</span></span>                    | <span data-ttu-id="6130b-117">Scopo</span><span class="sxs-lookup"><span data-stu-id="6130b-117">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6130b-118">ReplicaNew</span><span class="sxs-lookup"><span data-stu-id="6130b-118">ReplicaNew</span></span><br/>     | <span data-ttu-id="6130b-119">La fase di copia copia tutti i file e le sottocartelle da ReplicaSource nell'origine in ReplicaNew nella destinazione.</span><span class="sxs-lookup"><span data-stu-id="6130b-119">The copy phase copies all files and subfolders from ReplicaSource on the source to ReplicaNew on the target.</span></span> <span data-ttu-id="6130b-120">Qualsiasi contenuto precedente di ReplicaNew viene eliminato ogni volta che la fase di copia viene eseguita su una determinata destinazione.</span><span class="sxs-lookup"><span data-stu-id="6130b-120">Any previous contents of ReplicaNew are deleted each time the copy phase is run against a given target.</span></span><br/> <span data-ttu-id="6130b-121">Questa cartella esiste solo durante l'esecuzione del processo di replica.</span><span class="sxs-lookup"><span data-stu-id="6130b-121">This folder exists only while the replication process is running.</span></span> <span data-ttu-id="6130b-122">Vedere ReplicaCurrent.</span><span class="sxs-lookup"><span data-stu-id="6130b-122">(See ReplicaCurrent.)</span></span><br/>           |
| <span data-ttu-id="6130b-123">ReplicaCurrent</span><span class="sxs-lookup"><span data-stu-id="6130b-123">ReplicaCurrent</span></span><br/> | <span data-ttu-id="6130b-124">Le applicazioni replicate attualmente installate nella destinazione vengono archiviate qui.</span><span class="sxs-lookup"><span data-stu-id="6130b-124">The replicated applications currently installed on the target are stored here.</span></span><br/> <span data-ttu-id="6130b-125">Quando viene avviata la fase di installazione, la cartella ReplicaNew viene rinominata ReplicaCurrent.</span><span class="sxs-lookup"><span data-stu-id="6130b-125">When the install phase is started, the ReplicaNew folder is renamed to ReplicaCurrent.</span></span> <span data-ttu-id="6130b-126">Se è presente una cartella ReplicaCurrent esistente, viene rinominata in ReplicaOld.</span><span class="sxs-lookup"><span data-stu-id="6130b-126">If there is an existing ReplicaCurrent folder, it is renamed to ReplicaOld.</span></span> <span data-ttu-id="6130b-127">Se è presente una cartella ReplicaOld esistente, il relativo contenuto viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="6130b-127">If there is an existing ReplicaOld folder, its contents are deleted.</span></span><br/> |
| <span data-ttu-id="6130b-128">ReplicaOld</span><span class="sxs-lookup"><span data-stu-id="6130b-128">ReplicaOld</span></span><br/>     | <span data-ttu-id="6130b-129">Salva i file dell'applicazione installati durante il prossimo all'ultima replica.</span><span class="sxs-lookup"><span data-stu-id="6130b-129">Saves the application files installed during the next to last replication.</span></span> <span data-ttu-id="6130b-130">Questi file vengono salvati solo a scopo di backup.</span><span class="sxs-lookup"><span data-stu-id="6130b-130">These files are saved for backup purposes only.</span></span><br/>                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="6130b-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6130b-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6130b-132">Registrazione e segnalazione errori</span><span class="sxs-lookup"><span data-stu-id="6130b-132">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="6130b-133">Fasi di replica</span><span class="sxs-lookup"><span data-stu-id="6130b-133">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="6130b-134">Uso di COMREPL</span><span class="sxs-lookup"><span data-stu-id="6130b-134">Using COMREPL</span></span>](using-comrepl.md)
</dt> <dt>

[<span data-ttu-id="6130b-135">Cosa viene replicato</span><span class="sxs-lookup"><span data-stu-id="6130b-135">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 




