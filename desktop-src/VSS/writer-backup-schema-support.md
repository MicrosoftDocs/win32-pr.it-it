---
description: Per implementare completamente un backup è necessario partecipare ai writer del sistema.
ms.assetid: ea504f8e-26d9-499e-b3e9-03515b480a75
title: Supporto dello schema di backup del writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 593df12f552f206d5d0eedbf8d021b69ef955c6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226109"
---
# <a name="writer-backup-schema-support"></a>Supporto dello schema di backup del writer

Per implementare completamente un backup è necessario partecipare ai writer del sistema. Tipi diversi di backup supportati sono detti schemi e sono indicati da una maschera di bit (OR bit per bit) dei membri dell'enumerazione [**\_ \_ dello schema di backup VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) . Gli schemi validi attualmente supportati sono i seguenti:

-   Schema predefinito: completo (VSS \_ BS non \_ definito): indica che un writer supporta un backup in cui verrà eseguito il backup di tutti i file indipendentemente dalla data dell'ultimo backup. La cronologia di backup di ogni file può essere aggiornata dal richiedente e i writer che supportano il \_ valore di enumerazione con timestamp di VSS BS \_ archiviano un timestamp aggiornato con il richiedente. Questo schema di backup può essere utilizzato come base per un backup incrementale o differenziale.

    Il ripristino di un backup completo richiede una sola immagine di backup.

-   Copia backup ( \_ \_ copia copia shadow del volume), come \_ lo \_ schema di backup completo VSS BS, indica che un writer supporta un backup in cui verrà eseguito il backup di tutti i file indipendentemente dalla data dell'ultimo backup. Tuttavia, la cronologia di backup di ogni file non verrà aggiornata dal richiedente o dal writer e questo tipo di backup non può essere utilizzato come base per un backup incrementale o differenziale.
-   File di log ( \_ log VSS BS \_ ): è necessario eseguire il backup solo dei file di log del writer. È necessario che un writer abbia aggiunto almeno un file ad almeno un componente usando il metodo [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) . Questo tipo di backup è specifico per VSS.
-   Percorsi di ripristino personalizzati (il writer del servizio Copia Shadow \_ \_ del volume \_ supporta \_ \_ la nuova destinazione): indica il supporto del writer per un richiedente che cambia, in fase di ripristino, in cui vengono ripristinati i file. Questo significa che un writer è stato codificato per verificare la rilocazione (usando [**IVssComponent:: GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)) e ha la capacità di utilizzare i file spostati.
-   Restore with Move (il writer del servizio Copia Shadow \_ \_ del volume supporta il \_ \_ ripristino \_ con \_ lo spostamento): indica che il writer supporta l'esecuzione di più istanze del writer con lo stesso ID di classe e supporta un richiedente che sposta un componente in un'istanza di writer diversa in fase di ripristino. L'istanza del writer viene specificata utilizzando un nome di istanza del writer persistente passato come parametro *wszWriterInstanceName* al metodo [**CVssWriter:: Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize) . Un richiedente può ottenere il nome dell'istanza del writer usando [**IVssExamineWriterMetadataEx:: GetIdentityEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadataex-getidentityex) e spostare i componenti durante il ripristino usando [**IVssBackupComponentsEx:: SetSelectedForRestoreEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex).

    **Windows Server 2003 e Windows XP:** Questo valore non è supportato fino a Windows Server 2003 con Service Pack 1 (SP1).

-   Incremental (VSS \_ BS \_ incrementale): indica che il writer usa l'API VSS per aiutare il richiedente, assicurando che solo i file che sono stati modificati o aggiunti dopo l'ultimo backup completo o incrementale vengano copiati in un supporto di archiviazione.

    Il ripristino di un backup incrementale richiede l'immagine di backup originale e tutte le immagini di backup incrementali effettuate dal backup iniziale.

-   Differenziale (VSS \_ BS \_ differenziale): indica che il writer usa l'API VSS per consentire al richiedente di assicurarsi che solo i file che sono stati modificati o aggiunti dopo l'ultimo backup completo vengano copiati in un supporto di archiviazione. tutte le informazioni sul backup intermedio verranno ignorate.

    Il ripristino di un backup differenziale richiede l'immagine di backup originale e l'immagine di backup differenziale più recente eseguita dopo l'ultimo backup completo.

-   Incrementale/differenziale: supporto per l'indicatore di data e ora (VSS \_ BS \_ con timestamp): indica che un writer supporta l'utilizzo del meccanismo di timestamp VSS per includere i file nelle operazioni incrementali o differenziali. Al momento del backup, il writer deve archiviare il timbro di backup di un [*set di file*](vssgloss-f.md) con il metodo [**IVssComponent:: SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) e in Restore recuperarlo con [**IVssComponent:: GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp).
-   Incrementale/differenziale: ora del supporto dell'Ultima modifica \_ ( \_ Ultima modifica di VSS BS): \_ indica che durante l'implementazione di backup incrementali o differenziali con file differenziati, un writer può fornire le informazioni sull'ora dell'Ultima modifica in modo indipendente. Queste informazioni possono essere fornite a un richiedente tramite il metodo [**IVssComponent:: AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) .
-   Incrementale/differenziale: limitazione del supporto (backup \_ \_ differenziale esclusivo VSS BS \_ ): \_ indica il supporto del writer per gli schemi di backup differenziali o incrementali, ma solo esclusivamente: ad esempio, non è possibile seguire un backup incrementale con un backup differenziale.
-   Stato del sistema indipendente ( \_ \_ stato del sistema indipendente VSS BS \_ \_ ): indica che il writer supporta il backup dei dati che fanno parte dello stato del sistema, ma di cui è anche possibile eseguire il backup indipendentemente dallo stato del sistema.

    **Windows Server 2003 e Windows XP:** Questo valore non è supportato fino a Windows Vista.

-   Roll-Forward Restore (VSS \_ BS \_ rollforward \_ Restore)-indica che il writer supporta un richiedente che imposta un punto di ripristino di rollforward tramite [**IVssBackupComponentsEx2:: SetRollForward**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setrollforward).

    **Windows Server 2003 e Windows XP:** Questo valore non è supportato fino a Windows Vista.

-   Restore Rename (VSS \_ BS \_ Restore \_ Rename)-indica che il writer supporta un richiedente che imposta un nome di ripristino usando [**IVssBackupComponentsEx2:: serestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setrestorename).

    **Windows Server 2003 e Windows XP:** Questo valore non è supportato fino a Windows Vista.

-   Ripristino autorevole (VSS \_ BS \_ autorevole \_ Restore)-indica che il writer supporta l'impostazione di un ripristino autorevole per un richiedente tramite [**IVssBackupComponentsEx2:: SetAuthoritativeRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setauthoritativerestore).

I writer impostano gli schemi usando il metodo [**IVssCreateWriterMetadata:: SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema) e un richiedente ottiene lo schema di ogni writer chiamando [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema).

 

 



