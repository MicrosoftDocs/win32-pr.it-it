---
description: A volte è utile eseguire il backup e il ripristino solo di sezioni di file. VSS fornisce meccanismi di file parziali che, se supportati da richiedenti, consentono ai writer di specificare backup e ripristini di file parziali.
ms.assetid: 02b74a4e-d69f-4eeb-866a-3399598b7035
title: Uso di file parziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e1aa2623788cc97d62c88d52ec7096829adc350e1d420e92cea12b8dd64d70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590455"
---
# <a name="working-with-partial-files"></a>Uso di file parziali

A volte è utile eseguire il backup e il ripristino solo di sezioni di file. VSS fornisce [*meccanismi di file*](vssgloss-p.md) parziali che, se supportati da richiedenti, consentono ai writer di specificare backup e ripristini di file parziali.

Le operazioni di file parziali sono spesso più usate per i writer che gestiscono file di dimensioni molto grandi, di cui solo una piccola frazione cambia tra le operazioni di backup. In questo caso, spesso è utile copiare solo la sezione modificata in supporti di backup. Per questo motivo, le operazioni di file parziali vengono in genere, ma non esclusivamente, usate per supportare le operazioni di backup e ripristino incrementali.

Se un writer vuole implementare un'operazione di file parziale, usa [**CVssWriter::IsPartialFileSupportEnabled**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled) per determinare se il richiedente che sta lavorando supporta l'operazione.

Se il richiedente supporta operazioni di file parziali e aggiunge il componente che gestisce il file (o il componente che definisce il set di componenti che contiene il file) al documento dei componenti di backup, un writer indica le sezioni del file da salvare (in genere durante la gestione di un evento [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) o [*PostSnapshot)*](vssgloss-p.md) chiamando [**IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile).

Oltre a un percorso e a un nome di file, il writer fornisce l'intervallo, informazioni facoltative sui metadati a [**IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile).

Le informazioni sull'intervallo vengono fornite come stringa che contiene uno degli elementi seguenti:

-   Coppie di offset nel file di cui eseguire il backup (in byte) e la lunghezza della sezione di cui eseguire il backup (in byte), l'offset e la lunghezza separati da due punti e ogni coppia separata da una virgola, ad esempio *Offset1***:**_Length1_*_,_* *Offset2***:**_Length2_.

    Ogni valore è un intero a 64 bit (in formato esadecimale o decimale) che specifica rispettivamente un offset di byte e una lunghezza in byte.

-   Percorso completo, incluso il nome file, nel sistema corrente di un file di intervalli binari contenente gli elementi seguenti:
    -   Numero (espresso come intero a 64 bit) di intervalli di file distinti contenuti nel file
    -   Ogni intervallo espresso come coppia di interi a 64 bit: il primo membro della coppia è l'offset nel file di cui viene eseguito il backup (in byte) e il secondo membro è la lunghezza dei dati di cui eseguire il backup (in byte)

Se un writer usa un file di intervalli per specificare un'operazione di file parziale, un richiedente deve garantire che sia stato eseguito il backup di questo file (anche se il file non fa necessariamente parte del set di backup predefinito) o che le informazioni sugli intervalli vengono mantenute nel supporto di backup in altro modo. Se non viene eseguito il backup delle informazioni del file di intervalli, il ripristino del file parzialmente sottoposto a backup sarà impossibile.

Il writer può anche aggiungere una stringa contenente metadati. Questi metadati possono essere in un formato specifico del writer perché è progettato per consentire al writer di convalidare eventuali ripristini futuri.

Con queste informazioni, un richiedente di supporto può eseguire un backup parziale del file.

Si consideri ad esempio un file di grandi dimensioni la cui intestazione (byte da 64 a 512) contiene un numero di record e altre informazioni aggiornate di frequente e i cui dati più recenti devono essere trovati negli ultimi 65536 byte del file, 0x1239E8577A a 0x1239E7577A.

Un writer può specificare un elenco di intervalli come stringa "**64:448,0x1239E8577A:65536**."

Al momento del ripristino e prima di eseguire effettivamente un'operazione di ripristino, un richiedente deve verificare se i file richiedono il supporto parziale dei file.

A tale scopo, il richiedente scorre prima i writer con i componenti archiviati nel documento Componenti di backup usando [**IVssBackupComponents::GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) e [**IVssBackupComponents::GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

L'interfaccia [**IVssBackupComponents::GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) viene quindi usata per restituire istanze dell'interfaccia [**IVssWriterComponentsExt,**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) che forniscono [**IVssWriterComponentsExt::GetComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) e [**IVssWriterComponentsExt::GetComponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount), che consentono al richiedente di ottenere istanze [**di IVssComponent.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)

Ciò consente a un richiedente di ottenere informazioni sui file parzialmente sottoposti a backup per partecipare a un ripristino usando [**IVssComponent::GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) e [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) per l'istanza di [**IVssComponent corrispondente**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) al componente che gestisce il file (o al componente che definisce il set di componenti che contiene il file).

Se l'operazione di file parziale è stata controllata da un file di intervalli, tale file deve essere ripristinato prima della copia dei dati su disco. È possibile che il richiedente sia necessario copiare nuovamente il file degli intervalli in un nuovo percorso su disco. In questo caso, indica che l'operazione è stata eseguita tramite [**IVssBackupComponents::SetRangesFilePath**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath).

Il richiedente procede quindi a copiare i dati nei percorsi appropriati nella destinazione di ripristino già su disco.

Un writer (durante la gestione di un evento [**PostRestore),**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) esaminando [**IVssComponent::GetFileRestoreStatus per**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus) i file indicati da [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile), determina se l'operazione di file parziale è riuscita. Il writer deve sempre tentare di verificare la correttezza del ripristino usando le informazioni di offset e tutti i metadati inclusi nel documento Dei componenti di backup.

Se il richiedente ha dovuto ripristinare il file degli intervalli in un nuovo percorso, VSS aggiornerà queste informazioni in modo che il percorso restituito da [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) sia corretto.

 

 
