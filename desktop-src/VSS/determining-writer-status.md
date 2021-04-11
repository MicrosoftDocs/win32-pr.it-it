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
# <a name="determining-writer-status"></a>Determinazione dello stato del writer

Un richiedente deve avere una conoscenza ben definita dello stato del writer che vi partecipa durante la creazione della copia shadow e durante le operazioni di backup e ripristino. A tale scopo, è consigliabile:

-   I richiedenti usano [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus), [**IVssBackupComponents:: GetWriterStatusCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatuscount)e [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus).
-   Come descritto in [Cenni preliminari sull'elaborazione di un backup in VSS](overview-of-processing-a-backup-under-vss.md) e [Panoramica sull'elaborazione di un ripristino in VSS](overview-of-processing-a-restore-under-vss.md), questi metodi sono particolarmente utili quando vengono chiamati in una sequenza di backup o ripristino ben definita. In genere, ciò significa che è necessario eseguire una query sui writer dopo che un richiedente ha completato una delle attività generando un evento VSS.

    Quando si elabora un backup, un richiedente deve eseguire una query su un writer in seguito al completamento dei metodi seguenti. I richiedenti devono chiamare [**GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) dopo aver chiamato [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) per fare in modo che la sessione del writer venga impostata sullo stato Completed.

    > [!Note]  
    > Questa operazione è necessaria solo in Windows Server 2008 con Service Pack 2 (SP2) e versioni precedenti.

     

    <dl> <dt>

[**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)
</dt> <dt>

[**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)
</dt> <dt>

[**IVssBackupComponents:: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)
</dt> </dl>

Durante le operazioni di ripristino, un richiedente deve eseguire una query su un writer dopo il completamento di questi metodi:
<dl> <dt>

[**IVssBackupComponents: riripristino:P**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)
</dt> <dt>

[**IVssBackupComponents::P ostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)
</dt> </dl>

-   Le chiamate a [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) che non fanno parte di una sequenza di backup o ripristino ben definita non forniscono un'immagine affidabile dello stato del writer, perché potrebbero riflettere condizioni che non indicano un errore nell'operazione corrente, ad esempio:
    -   Errore durante la creazione di una copia shadow precedente
    -   Errore in un'operazione di backup o ripristino anticipata
    -   Un writer che non risponde attualmente elabora un evento

Pertanto, gli sviluppatori non devono basarsi sullo stato del writer restituito da altri processi, quindi dal richiedente o dal tentativo di monitorare lo stato di un'istanza dell'interfaccia [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) con un'altra, possibilmente in un thread separato.

Si noti che per le operazioni di backup, in cui è necessario esaminare i documenti dei metadati del writer Writer, non è necessario eseguire una chiamata del richiedente a [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) in seguito alla generazione e alla gestione dell'evento di [*Identificazione*](vssgloss-i.md) causato da [**IVssBackupComponents:: GatherWriterMetdata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).

[**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) segnala solo lo stato dei writer i cui metadati sono stati forniti a VSS dai writer ' [*identificano*](vssgloss-i.md) i gestori eventi, [**CVssWriter:: onidentifi**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) (e restituiti al richiedente da [**IVssBackupComponents:: GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) e [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)).

Se l'implementazione di [**CVssWriter:: onidentifi**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) ha esito negativo, i metadati del writer non faranno parte dell'elenco dei documenti di metadati del writer forniti a VSS, non saranno disponibili informazioni sullo stato e la chiamata risulterebbe ridondante.

Per le operazioni di ripristino, in cui il richiedente non deve esaminare i documenti dei metadati del writer per l'esecuzione di writer, la chiamata di [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) può essere un modo più efficiente per determinare quali writer sono in esecuzione.

 

 



