---
description: A volte è utile eseguire il backup e il ripristino solo di sezioni di file. VSS fornisce meccanismi parziali dei file, che, se richiesti dai richiedenti, consentono ai writer di specificare backup e ripristini parziali dei file.
ms.assetid: 02b74a4e-d69f-4eeb-866a-3399598b7035
title: Utilizzo di file parziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7194f01df11f6c0e368941e17ef6ab1620b17f67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307126"
---
# <a name="working-with-partial-files"></a>Utilizzo di file parziali

A volte è utile eseguire il backup e il ripristino solo di sezioni di file. VSS fornisce meccanismi [*parziali dei file*](vssgloss-p.md) , che, se richiesti dai richiedenti, consentono ai writer di specificare backup e ripristini parziali dei file.

Le operazioni parziali sui file sono spesso più utilizzate per i writer che gestiscono file di dimensioni molto grandi, ma solo una piccola parte del cambiamento tra le operazioni di backup. Questo è il caso, spesso è utile copiare solo la sezione modificata nei supporti di backup. Per questo motivo, le operazioni di file parziali sono in genere, ma non esclusivamente, utilizzate per supportare operazioni di backup e ripristino incrementali.

Se un writer desidera implementare un'operazione di file parziale, USA [**CVssWriter:: IsPartialFileSupportEnabled**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled) per determinare se il richiedente che sta utilizzando supporta l'operazione.

Se il richiedente supporta operazioni di file parziali e aggiunge il componente che gestisce il file (o il componente che definisce il set di componenti che contiene il file) al documento dei componenti di backup, un writer indica le sezioni del file da salvare, in genere durante la gestione di un evento [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) o [*PostSnapshot*](vssgloss-p.md) , chiamando [**IVssComponent:: AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile).

Oltre a un percorso e un nome file, il writer fornisce l'intervallo, le informazioni facoltative sui metadati di [**IVssComponent:: AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile).

Le informazioni sull'intervallo vengono fornite come una stringa che contiene uno dei seguenti elementi:

-   Coppie di offset nel file di cui eseguire il backup (in byte) e la lunghezza della sezione di cui eseguire il backup (in byte), l'offset e la lunghezza separati da due punti e ogni coppia separata da una virgola, ad esempio *Offset1 ***:**_length1_*_,_* * Offset2 ***:**_length2_.

    Ogni valore è un Integer a 64 bit, in formato esadecimale o decimale, che specifica rispettivamente un offset di byte e la lunghezza in byte.

-   Percorso completo, incluso il nome del file, nel sistema corrente di un file di intervalli binari che contiene gli elementi seguenti:
    -   Numero (espresso come intero a 64 bit) di intervalli di file distinti contenuti nel file
    -   Ogni intervallo espresso come coppia di interi a 64 bit: il primo membro della coppia che è l'offset nel file di cui viene eseguito il backup (in byte) e il secondo membro è la lunghezza dei dati di cui eseguire il backup (in byte)

Se un writer utilizza un file di intervalli per specificare un'operazione di file parziale, un richiedente deve garantire che venga eseguito il backup di questo file (anche se il file non è necessariamente parte del set di backup predefinito) o che le informazioni sugli intervalli vengono conservate nel supporto di backup in altro modo. Se non viene eseguito il backup delle informazioni del file degli intervalli, il ripristino del file di backup parziale non sarà possibile.

Il writer può anche aggiungere una stringa contenente i metadati. Questi metadati possono essere in un formato specifico del writer perché sono destinati a consentire al writer di convalidare eventuali ripristini futuri.

Con queste informazioni, un richiedente di supporto può eseguire un backup parziale del file.

Si consideri ad esempio un file di grandi dimensioni la cui intestazione (byte 64-512) contiene un numero di record e altre informazioni aggiornate di frequente e i cui dati più recenti si trovano negli ultimi 65536 byte del file, ovvero i byte 0x1239E8577A in 0x1239E7577A.

Un writer può specificare un elenco di intervalli come stringa "**64:448, 0x1239E8577A: 65536**".

In fase di ripristino e prima di eseguire effettivamente un'operazione di ripristino, un richiedente deve verificare se i file richiedono un supporto file parziale.

A tale scopo, il richiedente scorre prima i writer con i componenti archiviati nel documento relativo ai componenti di backup usando [**IVssBackupComponents:: GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) e [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

L'interfaccia [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) viene quindi utilizzata per restituire le istanze dell'interfaccia [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) che forniscono [**IVssWriterComponentsExt:: getComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) e [**IVssWriterComponentsExt:: GetComponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount), che consentono al richiedente di ottenere istanze di [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

Questo consente a un richiedente di ottenere informazioni sui file parzialmente sottoposti a backup per partecipare a un ripristino usando [**IVssComponent:: GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) e [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) per l'istanza di [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) corrispondente al componente che gestisce il file (o il componente che definisce il set di componenti che contiene il file).

Se l'operazione relativa al file parziale è stata controllata da un file degli intervalli, il file deve essere ripristinato prima della copia dei dati sul disco. È possibile che il richiedente ricopi il file degli intervalli in una nuova posizione sul disco. In questo caso, indica che l'operazione è stata eseguita tramite [**IVssBackupComponents:: SetRangesFilePath**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath).

Il richiedente procede quindi alla copia dei dati nelle posizioni appropriate nella destinazione di ripristino già presente su disco.

Un writer (durante la gestione di un evento [**PostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) ), esaminando [**IVssComponent:: GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus) per i file indicati da [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile), determina se l'operazione di file parziale è stata completata correttamente. Il writer deve sempre provare a verificare la correttezza del ripristino usando le informazioni di offset ed eventuali metadati inclusi nel documento dei componenti di backup.

Se il richiedente deve ripristinare il file degli intervalli in un nuovo percorso, VSS aggiornerà queste informazioni in modo che il percorso restituito da [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) sia corretto.

 

 
