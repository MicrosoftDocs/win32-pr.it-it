---
description: Per implementare completamente un backup è necessaria la partecipazione dei writer del sistema.
ms.assetid: ea504f8e-26d9-499e-b3e9-03515b480a75
title: Supporto dello schema di backup del writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56b037591d6deda2657acdfe4f4e4755fef96b52bafc92e4cc51e4ef7119de1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344244"
---
# <a name="writer-backup-schema-support"></a>Supporto dello schema di backup del writer

Per implementare completamente un backup è necessaria la partecipazione dei writer del sistema. I diversi tipi di backup supportati vengono definiti schemi e sono indicati da una maschera di bit (o OR bit per bit) dei membri dell'enumerazione [**VSS \_ BACKUP \_ SCHEMA.**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) Gli schemi validi attualmente supportati includono:

-   Schema predefinito: completo (VSS BS UNDEFINED): indica che un writer supporta un backup in cui verrà eseguito il backup di tutti i file indipendentemente dalla data \_ \_ dell'ultimo backup. La cronologia di backup di ogni file può essere aggiornata dal richiedente e i writer che supportano il valore di enumerazione TIMESTAMPED di VSS BS archivieranno un timestamp aggiornato con il \_ \_ richiedente. Questo schema di backup può essere usato come base di un backup incrementale o differenziale.

    Il ripristino di un backup completo richiede una sola immagine di backup.

-   Copy Backup (VSS BS COPY), come lo schema di backup FULL di \_ \_ \_ VSS BS, indica che un writer supporta un backup in cui verrà eseguito il backup di tutti i file indipendentemente dalla data dell'ultimo \_ backup. Tuttavia, la cronologia di backup di ogni file non verrà aggiornata dal richiedente o dal writer e questo tipo di backup non può essere usato come base di un backup incrementale o differenziale.
-   File di log (VSS BS LOG): è necessario eseguire il backup solo dei \_ file di log di un \_ writer. È necessario che un writer abbia aggiunto almeno un file ad almeno un componente usando il metodo [**IVssCreateWriterMetadata::AddDatabaseLogFiles.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) Questo tipo di backup è specifico di VSS.
-   Percorsi di ripristino personalizzati (VSS BS WRITER SUPPORTA LA NUOVA DESTINAZIONE): indica il supporto del writer per un richiedente che modifica, in fase di ripristino, i file in cui \_ \_ vengono \_ \_ \_ ripristinati. Ciò significa che un writer è stato codificato per verificare tale rilocazione (usando [**IVssComponent::GetNewTarget)**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)e ha la capacità di usare i file ricollocati.
-   Restore with Move \_ (VSS BS WRITER SUPPORTA RESTORE WITH MOVE): indica che il writer supporta l'esecuzione di più istanze del writer con lo stesso ID classe e supporta lo spostamento di un componente in un'altra istanza del writer in fase di \_ \_ \_ \_ \_ ripristino. L'istanza del writer viene specificata usando un nome di istanza del writer persistente passato come parametro *wszWriterInstanceName* al metodo [**CVssWriter::Initialize.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize) Un richiedente può ottenere il nome dell'istanza del writer [**usando IVssExamineWriterMetadataEx::GetIdentityEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadataex-getidentityex) e spostare i componenti durante il ripristino [**usando IVssBackupComponentsEx::SetSelectedForRestoreEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex).

    **Windows Server 2003 e Windows XP:** Questo valore non è supportato fino Windows Server 2003 con Service Pack 1 (SP1).

-   Incremental (VSS BS INCREMENTAL): indica che il writer usa l'API VSS per aiutare il richiedente, assicurando che solo i file modificati o aggiunti dopo l'ultimo backup completo o incrementale devono essere copiati in un supporto di \_ \_ archiviazione.

    Il ripristino di un backup incrementale richiede l'immagine di backup originale e tutte le immagini di backup incrementale effettuate dopo il backup iniziale.

-   Differenziale (VSS BS DIFFERENTIAL): indica che il writer usa l'API VSS per aiutare il richiedente a garantire che solo i file modificati o aggiunti dopo l'ultimo backup completo siano copiati in un supporto di archiviazione; tutte le informazioni di backup intermedie vengono \_ \_ ignorate.

    Il ripristino di un backup differenziale richiede l'immagine di backup originale e l'immagine di backup differenziale più recente effettuata dopo l'ultimo backup completo.

-   Incrementale/differenziale: supporto timestamp (VSS BS TIMESTAMPED): indica che un writer supporta l'uso del meccanismo di timestamp vss per includere i file in operazioni incrementali o \_ \_ differenziali. Al momento del backup, il writer deve archiviare il timestamp di backup di un set di [*file*](vssgloss-f.md) con il metodo [**IVssComponent::SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) e al momento del ripristino recuperarlo con [**IVssComponent::GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp).
-   Incrementale/differenziale: supporto dell'ora dell'ultima modifica (VSS BS LAST MODIFY): indica che quando si implementano backup incrementali o differenziali con file con differenze, un writer può fornire informazioni sull'ora dell'ultima modifica in modo \_ \_ \_ indipendente. Queste informazioni possono essere fornite a un richiedente tramite il [**metodo IVssComponent::AddDifferencedFilesByLastModifyTime.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)
-   Incrementale/differenziale: limitazione del supporto (DIFFERENZIALE INCREMENTALE ESCLUSIVO VSS BS): indica il supporto del writer di schemi di backup differenziali o differenziali, ma solo esclusivamente: ad esempio, non è possibile seguire un backup incrementale con un \_ \_ backup \_ \_ differenziale.
-   Stato del sistema indipendente (VSS BS INDEPENDENT SYSTEM STATE): indica che il writer supporta il backup dei dati che fanno parte dello stato del sistema, ma che possono anche essere sottoposti a backup indipendentemente dallo stato del \_ \_ \_ \_ sistema.

    **Windows Server 2003 e Windows XP:** Questo valore non è supportato fino a Windows Vista.

-   Roll-Forward Restore (VSS BS ROLLFORWARD RESTORE): indica che il writer supporta un richiedente che imposta un punto di ripristino roll forward usando \_ \_ \_ [**IVssBackupComponentsEx2::SetRollForward**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setrollforward).

    **Windows Server 2003 e Windows XP:** Questo valore non è supportato fino a Windows Vista.

-   Restore Rename (VSS BS RESTORE RENAME): indica che il writer supporta l'impostazione di un nome di ripristino da parte del richiedente \_ \_ tramite \_ [**IVssBackupComponentsEx2::SetRestoreName**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setrestorename).

    **Windows Server 2003 e Windows XP:** Questo valore non è supportato fino a Windows Vista.

-   Ripristino autorevole (VSS BS AUTHORITATIVE RESTORE): indica che il writer supporta un'impostazione autorevole del richiedente tramite \_ \_ \_ [**IVssBackupComponentsEx2::SetAuthoritativeRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setauthoritativerestore).

I writer impostano gli schemi usando il metodo [**IVssCreateWriterMetadata::SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema) e un richiedente ottiene lo schema di ogni writer chiamando [**IVssExamineWriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema).

 

 



