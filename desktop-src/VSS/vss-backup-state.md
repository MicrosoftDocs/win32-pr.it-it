---
description: Durante un'operazione di backup, il richiedente usa IVssBackupComponents::SetBackupState per definire il tipo di operazione in corso.
ms.assetid: 43dcdac7-ed8e-4150-83eb-585e0e92f13c
title: Stato del backup VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35701e1b576d9ea2e5464516589ae419dc73b74898768af06e974da05afffa8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056219"
---
# <a name="vss-backup-state"></a>Stato del backup VSS

Durante un'operazione di backup, il richiedente usa [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) per definire il tipo di operazione in corso.

Queste informazioni non sono incluse in un formato facilmente recuperabile nel documento dei componenti di backup, quindi gli sviluppatori richiedenti devono archiviare queste informazioni in modo indipendente in qualsiasi supporto di backup.

Lo stato del backup contiene quanto segue:

<dl> <dt>

<span id="Backup_Type"></span><span id="backup_type"></span><span id="BACKUP_TYPE"></span>Tipo di backup
</dt> <dd>

Il tipo di backup specifica i criteri per identificare i file di cui eseguire il backup. La valutazione di questi criteri deve essere effettuata usando l'API vss.

Quando si decide il tipo di backup da eseguire e quali writer usare, i richiedenti devono esaminare i tipi (o gli schemi, vedere Supporto dello schema di backup del [writer)](writer-backup-schema-support.md)delle operazioni di backup supportate da ognuno dei writer del sistema. I backup in VSS possono essere dei tipi seguenti:

-   Completo (VSS BT FULL): verrà eseguito il backup dei file \_ \_ indipendentemente dalla data dell'ultimo backup. La cronologia di backup di ogni file verrà aggiornata e questo tipo di backup può essere utilizzato come base per un backup incrementale o differenziale. Il ripristino di un backup completo richiede una sola immagine di backup.
-   Copia backup (COPIA BT VSS): come il tipo di backup FULL di VSS BT, verrà eseguito il backup dei file indipendentemente dalla \_ \_ data \_ \_ dell'ultimo backup. Tuttavia, la cronologia di backup di ogni file non verrà aggiornata e questo tipo di backup non può essere utilizzato come base di un backup incrementale o differenziale.
-   Incrementale (VSS \_ BT INCREMENTAL): l'API VSS viene usata per garantire che solo i file che sono stati modificati o aggiunti dopo l'ultimo backup completo o incrementale devono essere copiati in un supporto di \_ archiviazione. Il ripristino di un backup incrementale richiede l'immagine di backup originale e tutte le immagini di backup incrementale effettuate dopo il backup iniziale.
-   Differenziale (VSS \_ BT DIFFERENTIAL): l'API VSS viene usata per garantire che solo i file che sono stati modificati o aggiunti dopo l'ultimo backup completo devono essere copiati in un supporto di archiviazione. Tutte le informazioni di backup intermedie vengono \_ ignorate. Il ripristino di un backup differenziale richiede l'immagine di backup originale e l'immagine di backup differenziale più recente dall'ultimo backup completo.
-   File di log (VSS BT LOG): verrà eseguito il backup solo dei file di log di un writer (file aggiunti a un componente con il metodo \_ \_ [**IVssCreateWriterMetadata::AddDataBaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) e recuperati da una chiamata a [**IVssWMComponent::GetDatabaseLogFile).**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile) Questo tipo di backup è specifico di VSS.

È possibile che i richiedenti implementino questi backup usando informazioni e metodi all'esterno del Servizio Copia Copia Backup. Solo quando un richiedente implementa un backup usando l'API vss, deve essere detto che ha uno dei tipi di backup elencati. Ad esempio, un richiedente partecipa a un tipo di backup VSS BT LOG solo se ha usato le informazioni restituite da \_ \_ [**IVssWMComponent::GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile) per identificare i file di log. Analogamente, i tipi VSS BT INCREMENTAL e VSS BT DIFFERENTIAL si applicano solo alle operazioni incrementali o differenziali, come descritto \_ \_ in Backup \_ \_ [incrementali e differenziali.](incremental-and-differential-backups.md)

</dd> <dt>

<span id="Specification_about_Selectability"></span><span id="specification_about_selectability"></span><span id="SPECIFICATION_ABOUT_SELECTABILITY"></span>Specifica sulla selezionabilità
</dt> <dd>

Un backup vss può scegliere di rispettare le nozioni vss sulla selezionabilità dei componenti, ovvero l'esecuzione [*in*](vssgloss-c.md)modalità componente, o di ignorarle.

Un esempio di non esecuzione in modalità componente potrebbe essere l'esecuzione di un backup dell'immagine del sistema, in cui l'applicazione di backup avrebbe bisogno della collaborazione del writer per garantire la stabilità dei dati, ma in cui la selezione dei componenti sarebbe irrilevante.

</dd> <dt>

<span id="Saving_Bootable_State"></span><span id="saving_bootable_state"></span><span id="SAVING_BOOTABLE_STATE"></span>Salvataggio dello stato di avvio
</dt> <dd>

VSS supporta il salvataggio dello stato del sistema in esecuzione in una configurazione completamente avviabile. Tuttavia, questo non è sempre necessario e la preparazione del writer per salvare uno stato di avvio può talvolta ridurre le prestazioni in tempo reale di un sistema in esecuzione.

Pertanto, i richiedenti indicano se un backup includerà uno stato del sistema di avvio come argomento di [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate). I writer determinano se è necessario supportare il salvataggio dello stato del sistema di avvio chiamando [**CVssWriter::IsBootableStateBackedUp.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-isbootablesystemstatebackedup)

Anche se lo stato del sistema di avvio non è selezionato, verranno effettuate copie shadow dei file di sistema e potrebbe essere eseguito il backup dei file.

Tuttavia, è necessario prestare molta attenzione nel ripristino dei file di sistema se il backup non ha salvato lo stato del sistema di avvio (vedere Backup e ripristino dello stato del sistema [in Windows Server 2003 R2 e Windows Server 2003 SP1).](backing-up-and-restoring-system-state-under-vss.md)

Non è possibile recuperare queste informazioni da un documento dei componenti di backup recuperato, pertanto gli autori del richiedente devono archiviare se il backup del sistema è stato eseguito o meno con uno stato del sistema di avvio.

</dd> <dt>

<span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>Supporto di file parziali
</dt> <dd>

Alcuni writer supportano il ripristino dei file tramite la sovrascrittura di parti dei file gestiti. Un richiedente può essere progettato per sfruttare questo vantaggio e, in tal caso, lo indica impostando le informazioni in [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate).

</dd> </dl>

 

 



