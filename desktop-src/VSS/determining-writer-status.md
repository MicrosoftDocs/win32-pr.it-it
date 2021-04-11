---
description: Un richiedente deve avere una conoscenza ben definita dello stato del writer che vi partecipa durante la creazione della copia shadow e durante le operazioni di backup e ripristino.
ms.assetid: 676d5cff-bd28-43f0-a402-d184c96f0061
title: Determinazione dello stato del writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719322a18808748e92d412c48c7b7628fdac9d51
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234619"
---
# <a name="determining-writer-status"></a><span data-ttu-id="64df4-103">Determinazione dello stato del writer</span><span class="sxs-lookup"><span data-stu-id="64df4-103">Determining Writer Status</span></span>

<span data-ttu-id="64df4-104">Un richiedente deve avere una conoscenza ben definita dello stato del writer che vi partecipa durante la creazione della copia shadow e durante le operazioni di backup e ripristino.</span><span class="sxs-lookup"><span data-stu-id="64df4-104">A requester needs to have a well-defined understanding about the status of the writer that participates with it during shadow copy creation, and during backup and restore operations.</span></span> <span data-ttu-id="64df4-105">A tale scopo, è consigliabile:</span><span class="sxs-lookup"><span data-stu-id="64df4-105">To do so, it is recommended:</span></span>

-   <span data-ttu-id="64df4-106">I richiedenti usano [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus), [**IVssBackupComponents:: GetWriterStatusCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatuscount)e [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus).</span><span class="sxs-lookup"><span data-stu-id="64df4-106">Requesters use [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus), [**IVssBackupComponents::GetWriterStatusCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatuscount), and [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus).</span></span>
-   <span data-ttu-id="64df4-107">Come descritto in [Cenni preliminari sull'elaborazione di un backup in VSS](overview-of-processing-a-backup-under-vss.md) e [Panoramica sull'elaborazione di un ripristino in VSS](overview-of-processing-a-restore-under-vss.md), questi metodi sono particolarmente utili quando vengono chiamati in una sequenza di backup o ripristino ben definita.</span><span class="sxs-lookup"><span data-stu-id="64df4-107">As described in [Overview of Processing a Backup Under VSS](overview-of-processing-a-backup-under-vss.md) and [Overview of Processing a Restore Under VSS](overview-of-processing-a-restore-under-vss.md), these methods are most useful when called in a well-defined backup or restore sequence.</span></span> <span data-ttu-id="64df4-108">In genere, ciò significa che è necessario eseguire una query sui writer dopo che un richiedente ha completato una delle attività generando un evento VSS.</span><span class="sxs-lookup"><span data-stu-id="64df4-108">Typically, this means that the writers should be queried after a requester has completed one of its tasks and generated a VSS event.</span></span>

    <span data-ttu-id="64df4-109">Quando si elabora un backup, un richiedente deve eseguire una query su un writer in seguito al completamento dei metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="64df4-109">When processing a backup, a requester should query a writer following the completion of the following methods.</span></span> <span data-ttu-id="64df4-110">I richiedenti devono chiamare [**GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) dopo aver chiamato [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) per fare in modo che la sessione del writer venga impostata sullo stato Completed.</span><span class="sxs-lookup"><span data-stu-id="64df4-110">Requesters must call [**GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) after calling [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) to cause the writer session to be set to a completed state.</span></span>

    > [!Note]  
    > <span data-ttu-id="64df4-111">Questa operazione è necessaria solo in Windows Server 2008 con Service Pack 2 (SP2) e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="64df4-111">This is only necessary on Windows Server 2008 with Service Pack 2 (SP2) and earlier.</span></span>

     

    <dl> <dt>

[<span data-ttu-id="64df4-112">**IVssBackupComponents::P repareForBackup**</span><span class="sxs-lookup"><span data-stu-id="64df4-112">**IVssBackupComponents::PrepareForBackup**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)
</dt> <dt>

[<span data-ttu-id="64df4-113">**IVssBackupComponents::D oSnapshotSet**</span><span class="sxs-lookup"><span data-stu-id="64df4-113">**IVssBackupComponents::DoSnapshotSet**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)
</dt> <dt>

[<span data-ttu-id="64df4-114">**IVssBackupComponents:: BackupComplete**</span><span class="sxs-lookup"><span data-stu-id="64df4-114">**IVssBackupComponents::BackupComplete**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)
</dt> </dl>

<span data-ttu-id="64df4-115">Durante le operazioni di ripristino, un richiedente deve eseguire una query su un writer dopo il completamento di questi metodi:</span><span class="sxs-lookup"><span data-stu-id="64df4-115">During restore operations, a requester should query a writer after completion of these methods:</span></span>
<dl> <dt>

[<span data-ttu-id="64df4-116">**IVssBackupComponents: riripristino:P**</span><span class="sxs-lookup"><span data-stu-id="64df4-116">**IVssBackupComponents::PreRestore**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)
</dt> <dt>

[<span data-ttu-id="64df4-117">**IVssBackupComponents::P ostRestore**</span><span class="sxs-lookup"><span data-stu-id="64df4-117">**IVssBackupComponents::PostRestore**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)
</dt> </dl>

-   <span data-ttu-id="64df4-118">Le chiamate a [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) che non fanno parte di una sequenza di backup o ripristino ben definita non forniscono un'immagine affidabile dello stato del writer, perché potrebbero riflettere condizioni che non indicano un errore nell'operazione corrente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="64df4-118">Calls to [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) that are not part of a well-defined backup or restore sequence do not provide a reliable picture of writer status, because they might reflect conditions that do not indicate failure in the current operation, such as:</span></span>
    -   <span data-ttu-id="64df4-119">Errore durante la creazione di una copia shadow precedente</span><span class="sxs-lookup"><span data-stu-id="64df4-119">A failure of a previous shadow copy creation</span></span>
    -   <span data-ttu-id="64df4-120">Errore in un'operazione di backup o ripristino anticipata</span><span class="sxs-lookup"><span data-stu-id="64df4-120">An error in an early backup or restore operation</span></span>
    -   <span data-ttu-id="64df4-121">Un writer che non risponde attualmente elabora un evento</span><span class="sxs-lookup"><span data-stu-id="64df4-121">An unresponsive writer currently processing an event</span></span>

<span data-ttu-id="64df4-122">Pertanto, gli sviluppatori non devono basarsi sullo stato del writer restituito da altri processi, quindi dal richiedente o dal tentativo di monitorare lo stato di un'istanza dell'interfaccia [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) con un'altra, possibilmente in un thread separato.</span><span class="sxs-lookup"><span data-stu-id="64df4-122">Therefore, developers should not rely on writer status returned by processes other then the requester or attempt to monitor the progress of one instance of the [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) interface with another (possibly in a separate thread).</span></span>

<span data-ttu-id="64df4-123">Si noti che per le operazioni di backup, in cui è necessario esaminare i documenti dei metadati del writer Writer, non è necessario eseguire una chiamata del richiedente a [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) in seguito alla generazione e alla gestione dell'evento di [*Identificazione*](vssgloss-i.md) causato da [**IVssBackupComponents:: GatherWriterMetdata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).</span><span class="sxs-lookup"><span data-stu-id="64df4-123">Note that for backup operations, where it is necessary to examine writers' Writer Metadata Documents, there is no need for a requester call to [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) and [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) following the generation and handling of the [*Identify*](vssgloss-i.md) event caused by [**IVssBackupComponents::GatherWriterMetdata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).</span></span>

<span data-ttu-id="64df4-124">[**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) segnala solo lo stato dei writer i cui metadati sono stati forniti a VSS dai writer ' [*identificano*](vssgloss-i.md) i gestori eventi, [**CVssWriter:: onidentifi**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) (e restituiti al richiedente da [**IVssBackupComponents:: GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) e [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)).</span><span class="sxs-lookup"><span data-stu-id="64df4-124">[**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) reports only the status of those writers whose metadata was provided to VSS by writers' [*Identify*](vssgloss-i.md) event handlers, [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) (and returned to the requester by [**IVssBackupComponents::GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) and [**IVssBackupComponents::GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)).</span></span>

<span data-ttu-id="64df4-125">Se l'implementazione di [**CVssWriter:: onidentifi**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) ha esito negativo, i metadati del writer non faranno parte dell'elenco dei documenti di metadati del writer forniti a VSS, non saranno disponibili informazioni sullo stato e la chiamata risulterebbe ridondante.</span><span class="sxs-lookup"><span data-stu-id="64df4-125">If a writer's implementation of [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) fails, that writer's metadata will not be part of the list of Writer Metadata Documents provided to VSS, no status information will be available, and the call would be redundant.</span></span>

<span data-ttu-id="64df4-126">Per le operazioni di ripristino, in cui il richiedente non deve esaminare i documenti dei metadati del writer per l'esecuzione di writer, la chiamata di [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) può essere un modo più efficiente per determinare quali writer sono in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="64df4-126">For restore operations, where the requester does not need to examine Writer Metadata Documents of executing writers, calling [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) and [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) may be a more efficient way to determine which writers are executing.</span></span>

 

 



