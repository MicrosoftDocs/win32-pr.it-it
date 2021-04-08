---
description: "Durante un'operazione di backup, il richiedente USA IVssBackupComponents:: SetBackupState per definire il tipo di operazione in corso."
ms.assetid: 43dcdac7-ed8e-4150-83eb-585e0e92f13c
title: Stato backup VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9aa9250139aee9f48f9880fd4a657fa7c6c4991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751567"
---
# <a name="vss-backup-state"></a>Stato backup VSS

Durante un'operazione di backup, il richiedente USA [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) per definire il tipo di operazione in corso.

Queste informazioni non sono incluse in un modulo facilmente recuperabile nel documento componenti di backup, quindi gli sviluppatori del richiedente devono archiviare queste informazioni in modo indipendente in qualsiasi supporto di backup.

Lo stato di backup contiene gli elementi seguenti:

<dl> <dt>

<span id="Backup_Type"></span><span id="backup_type"></span><span id="BACKUP_TYPE"></span>Tipo di backup
</dt> <dd>

Il tipo di backup specifica i criteri per l'identificazione dei file di cui eseguire il backup. La valutazione di questi criteri deve essere eseguita usando l'API VSS.

Quando si decide il tipo di backup da perseguire e quali writer usare, i richiedenti devono esaminare i tipi o gli schemi, vedere [supporto dello schema di backup del writer](writer-backup-schema-support.md), delle operazioni di backup supportate da ciascuno dei writer del sistema. I backup in VSS possono essere i tipi seguenti:

-   Completo (VSS \_ BT \_ Full): verrà eseguito il backup dei file indipendentemente dalla data dell'ultimo backup. La cronologia di backup di ogni file verrà aggiornata e questo tipo di backup può essere utilizzato come base per un backup incrementale o differenziale. Il ripristino di un backup completo richiede una sola immagine di backup.
-   Copia backup ( \_ copia servizio \_ Copia Shadow del volume): Analogamente al \_ \_ tipo di backup completo VSS BT, viene eseguito il backup dei file indipendentemente dalla data dell'ultimo backup. Tuttavia, la cronologia di backup di ogni file non verrà aggiornata e questo tipo di backup non può essere utilizzato come base per un backup incrementale o differenziale.
-   Incrementale (VSS \_ BT \_ incrementale): l'API VSS viene utilizzata per garantire che solo i file che sono stati modificati o aggiunti dopo l'ultimo backup completo o incrementale vengano copiati in un supporto di archiviazione. Il ripristino di un backup incrementale richiede l'immagine di backup originale e tutte le immagini di backup incrementali effettuate dal backup iniziale.
-   Differenziale ( \_ \_ differenziale del servizio Copia Shadow del volume): l'API VSS viene usata per garantire che solo i file che sono stati modificati o aggiunti dopo l'ultimo backup completo vengano copiati in un supporto di archiviazione; tutte le informazioni sul backup intermedio verranno ignorate. Il ripristino di un backup differenziale richiede l'immagine di backup originale e l'immagine di backup differenziale più recente eseguita dopo l'ultimo backup completo.
-   File di log ( \_ \_ log di VSS BT): verrà eseguito il backup solo dei file di log del writer, ovvero i file aggiunti a un componente con il metodo [**IVssCreateWriterMetadata:: AddDataBaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) e recuperati da una chiamata a [**IVssWMComponent:: GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile). Questo tipo di backup è specifico per VSS.

È possibile che i richiedenti implementino questi backup usando informazioni e metodi esterni a VSS. Solo quando un richiedente implementa un backup con l'API VSS, dovrebbe essere definito uno dei tipi di backup elencati. Un richiedente, ad esempio, fa parte di un \_ \_ tipo di log VSS BT solo se ha usato le informazioni restituite da [**IVssWMComponent:: GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile) per identificare i file di log. Analogamente, i \_ \_ tipi differenziali di VSS BT incrementali e VSS \_ BT \_ si applicano solo alle operazioni incrementali o differenziali, come descritto in [backup incrementali e differenziali](incremental-and-differential-backups.md).

</dd> <dt>

<span id="Specification_about_Selectability"></span><span id="specification_about_selectability"></span><span id="SPECIFICATION_ABOUT_SELECTABILITY"></span>Specifica sulla selezione
</dt> <dd>

Un backup del servizio Copia Shadow del volume può scegliere di rispettare le nozioni VSS della selezione dei componenti. questa operazione viene definita esecuzione in [*modalità componente*](vssgloss-c.md), oppure per ignorarle.

Un esempio di non esecuzione in modalità componente consiste nell'esecuzione di un backup delle immagini del sistema, in cui l'applicazione di backup richiederebbe la collaborazione del writer per garantire la stabilità dei dati, ma la selezione dei componenti sarebbe irrilevante.

</dd> <dt>

<span id="Saving_Bootable_State"></span><span id="saving_bootable_state"></span><span id="SAVING_BOOTABLE_STATE"></span>Salvataggio dello stato di avvio
</dt> <dd>

VSS supporta il salvataggio dello stato del sistema in esecuzione in una configurazione di avvio completo. Tuttavia, questo non è sempre necessario e la preparazione del writer per salvare uno stato di avvio può a volte peggiorare le prestazioni in tempo reale di un sistema in esecuzione.

Pertanto, i richiedenti indicano se un backup includerà uno stato del sistema di avvio come argomento di [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate). I writer determinano se devono supportare il salvataggio dello stato del sistema di avvio chiamando [**CVssWriter:: IsBootableStateBackedUp**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-isbootablesystemstatebackedup).

Anche se lo stato del sistema di avvio non è selezionato, verranno eseguite copie shadow dei file di sistema ed è possibile eseguire il backup dei file.

Tuttavia, è opportuno prestare particolare attenzione durante il ripristino dei file di sistema se il backup non ha salvato lo stato del sistema di avvio (vedere [backup e ripristino dello stato del sistema in Windows server 2003 R2 e Windows server 2003 SP1](backing-up-and-restoring-system-state-under-vss.md)).

Non è possibile recuperare queste informazioni da un documento relativo ai componenti di backup recuperati, quindi gli autori del richiedente devono archiviare se è stato eseguito il backup del sistema con uno stato del sistema di avvio.

</dd> <dt>

<span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>Supporto file parziale
</dt> <dd>

Alcuni writer supportano il ripristino dei file tramite la sovrascrittura delle parti dei file gestiti. Un richiedente può essere progettato per trarre vantaggio da questo e, in caso affermativo, impostando le informazioni in [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate).

</dd> </dl>

 

 



