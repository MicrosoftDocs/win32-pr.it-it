---
description: Durante l'elaborazione di un backup, un richiedente e una coordinata di writer per fornire un'immagine di sistema stabile dalla quale eseguire il backup dei dati (il volume copiato Shadow), raggruppare i file in base all'utilizzo e archiviare le informazioni sui dati salvati.
ms.assetid: d7acb2a2-bb58-47e3-a950-d32f663ae36d
title: Cenni preliminari sull'elaborazione di un backup in VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a11aeab87b503241acefdd15a153c9e417e537
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345021"
---
# <a name="overview-of-processing-a-backup-under-vss"></a><span data-ttu-id="6937a-103">Cenni preliminari sull'elaborazione di un backup in VSS</span><span class="sxs-lookup"><span data-stu-id="6937a-103">Overview of Processing a Backup Under VSS</span></span>

<span data-ttu-id="6937a-104">Durante l'elaborazione di un backup, un richiedente e una coordinata di writer per fornire un'immagine di sistema stabile dalla quale eseguire il backup dei dati (il volume copiato Shadow), raggruppare i file in base all'utilizzo e archiviare le informazioni sui dati salvati.</span><span class="sxs-lookup"><span data-stu-id="6937a-104">In processing a backup, requester and writers coordinate to provide a stable system image from which to back up data (the shadow copied volume), to group files together on the basis of their usage, and to store information on the saved data.</span></span> <span data-ttu-id="6937a-105">Questa operazione deve essere eseguita durante la creazione di un'interruzione minima del flusso di lavoro normale del writer.</span><span class="sxs-lookup"><span data-stu-id="6937a-105">This must all be done while creating only minimal interruption to the writer's normal work flow.</span></span>

<span data-ttu-id="6937a-106">Un richiedente esegue una query di writer per i relativi metadati, elabora questi dati, invia una notifica ai writer prima dell'inizio della copia shadow e delle operazioni di backup e quindi notifica nuovamente i writer al termine delle operazioni di copia shadow e backup.</span><span class="sxs-lookup"><span data-stu-id="6937a-106">A requester queries writers for their metadata, processes this data, notifies the writers prior to the beginning of the shadow copy and of the backup operations, and then notifies the writers again after the shadow copy and backup operations end.</span></span>

<span data-ttu-id="6937a-107">In risposta a queste notifiche, il writer fornisce informazioni sui file di cui eseguire il backup, ad esempio specificando i gruppi di file da coordinare ([*componenti*](vssgloss-c.md)), sospendendo le operazioni di i/O prima di una copia shadow e quindi torna al normale funzionamento dopo il completamento di una copia shadow o alla fine del backup.</span><span class="sxs-lookup"><span data-stu-id="6937a-107">In response to these notifications, the writer provides information about files to be backed up—including specifying groups of files to coordinate ([*components*](vssgloss-c.md))—pauses in its I/O operations prior to a shadow copy, and then returns to normal operation following the completion of a shadow copy or at the end of the backup.</span></span>

<span data-ttu-id="6937a-108">Nel corso dell'elaborazione del backup, un writer specifica i file di cui è responsabile tramite i metadati di sola lettura, ovvero il documento di metadati del writer (vedere [metadati VSS: utilizzo del documento di metadati del writer](working-with-the-writer-metadata-document.md)).</span><span class="sxs-lookup"><span data-stu-id="6937a-108">In the course of processing the backup, a writer specifies the files it is responsible for through its read-only metadata—the Writer Metadata Document (see [VSS Metadata: Working with the Writer Metadata Document](working-with-the-writer-metadata-document.md)).</span></span> <span data-ttu-id="6937a-109">Il richiedente interpreta quindi questi metadati, sceglie gli elementi di cui eseguire il backup e archivia tali decisioni nel relativo oggetto metadati, il documento componenti di backup (vedere [metadati VSS: utilizzo del documento componenti di backup](working-with-the-backup-components-document.md)).</span><span class="sxs-lookup"><span data-stu-id="6937a-109">The requester then interprets this metadata, chooses what to back up, and stores these decisions in its own metadata object, the Backup Components Document (see [VSS Metadata: Working with the Backup Components Document](working-with-the-backup-components-document.md)).</span></span> <span data-ttu-id="6937a-110">Questo documento dei componenti di backup è disponibile per l'ispezione e la modifica del writer durante le operazioni di backup e ripristino.</span><span class="sxs-lookup"><span data-stu-id="6937a-110">This Backup Components Document is available for writer inspection and modification during both the backup and restore operations.</span></span>

<span data-ttu-id="6937a-111">Questo diagramma illustra le interazioni tra il richiedente, il servizio VSS, il supporto del kernel VSS, gli eventuali writer VSS interessati ed eventuali provider hardware VSS.</span><span class="sxs-lookup"><span data-stu-id="6937a-111">This diagram shows the interactions between the requester, the VSS service, the VSS kernel support, any VSS writers involved, and any VSS hardware providers.</span></span>

![interazioni tra richiedente, componenti di backup, writer e provider](images/vssimpl.png)

<span data-ttu-id="6937a-113">Per comprendere appieno le attività di base necessarie per l'esecuzione di un backup, è utile suddividere questa panoramica negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="6937a-113">To more fully understand the basic tasks involved in performing a backup, it is useful to break down this overview into the following topics:</span></span>

-   [<span data-ttu-id="6937a-114">Panoramica dell'inizializzazione del backup</span><span class="sxs-lookup"><span data-stu-id="6937a-114">Overview of Backup Initialization</span></span>](overview-of-backup-initialization.md)
-   [<span data-ttu-id="6937a-115">Panoramica della fase di individuazione del backup</span><span class="sxs-lookup"><span data-stu-id="6937a-115">Overview of the Backup Discovery Phase</span></span>](overview-of-the-backup-discovery-phase.md)
-   [<span data-ttu-id="6937a-116">Panoramica delle attività di pre-backup</span><span class="sxs-lookup"><span data-stu-id="6937a-116">Overview of Pre-Backup Tasks</span></span>](overview-of-pre-backup-tasks.md)
-   [<span data-ttu-id="6937a-117">Panoramica del backup effettivo dei file</span><span class="sxs-lookup"><span data-stu-id="6937a-117">Overview of Actual Backup Of Files</span></span>](overview-of-actual-backup-of-files.md)
-   [<span data-ttu-id="6937a-118">Panoramica della terminazione del backup</span><span class="sxs-lookup"><span data-stu-id="6937a-118">Overview of Backup Termination</span></span>](overview-of-backup-termination.md)

 

 



