---
description: Gli amministratori possono creare, eliminare e ri-creare i journal delle modifiche.
ms.assetid: 26cbacc2-d26b-434b-91b5-31aedc96da13
title: Creazione, modifica ed eliminazione di un journal delle modifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d4cf9a597baa14fc929028eab262479da30797a2e423b779083f028927ce50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150867"
---
# <a name="creating-modifying-and-deleting-a-change-journal"></a>Creazione, modifica ed eliminazione di un journal delle modifiche

Gli amministratori possono creare, eliminare e ri-creare di nuovo i journal delle modifiche. Un amministratore deve eliminare un journal quando il valore USN (Update Sequence Number) corrente si avvicina al valore USN massimo possibile, come indicato dal membro **MaxUsn** della struttura [**USN \_ JOURNAL \_ DATA.**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_journal_data_v0) Un amministratore può anche eliminare e creare nuovamente un journal delle modifiche per recuperare spazio su disco. Per eseguire questa e tutte le altre operazioni di journal delle modifiche non a livello di codice, è necessario disporre dei privilegi di amministratore di sistema. In altri modo, è necessario essere un membro del gruppo Administrators.

Per creare o modificare un journal delle modifiche in un volume specificato a livello di codice, usare il [**codice di controllo FSCTL \_ CREATE \_ USN \_ JOURNAL.**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal)

Quando si crea un nuovo journal delle modifiche o ne si modifica uno esistente, il file system NTFS imposta le informazioni per il journal delle modifiche dalle informazioni contenute nella struttura [**CREATE \_ USN \_ JOURNAL \_ DATA,**](/windows/desktop/api/WinIoCtl/ns-winioctl-create_usn_journal_data) che [**FSCTL \_ CREATE \_ USN \_ JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal) accetta come input. **CREATE \_ USN \_ JOURNAL \_ DATA** ha i membri **MaximumSize** e **AllocationDelta**.

**MaximumSize è** la dimensione massima di destinazione in byte per il journal delle modifiche. Il journal delle modifiche può aumentare rispetto a questo valore, ma nei checkpoint NTFS file system il file system NTFS esamina il journal e lo taglia quando le dimensioni superano il valore **MaximumSize** più il valore **di AllocationDelta**. Nei checkpoint file system NTFS, il sistema operativo scrive record nel file di log file system NTFS che consentono al file system NTFS di determinare quale elaborazione è necessaria per il ripristino in caso di errore.

**AllocationDelta** è il numero di byte aggiunti alla fine e rimossi dall'inizio del journal delle modifiche ogni volta che la memoria viene allocata o deallocata. In altre parole, l'allocazione e la deallocazione si svolgono in unità di queste dimensioni. Un multiplo intero di dimensioni del cluster è un valore ragionevole per questo membro.

Se un amministratore modifica un journal delle modifiche esistente in modo che abbia un valore **MaximumSize** maggiore, ad esempio se un volume viene indicizzato troppo spesso, il journal delle modifiche riceve semplicemente nuove voci finché non supera le nuove dimensioni massime.

Per eliminare un journal delle modifiche, usare il [**codice di controllo \_ FSCTL DELETE \_ USN \_ JOURNAL.**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal) Quando si usa questa operazione, vengono eserciti tutti i file nel volume e l'USN per ogni file viene reimpostato su zero. L'operazione elimina quindi il journal delle modifiche esistente. Questa operazione viene mantenuta tra i riavvii del sistema fino al completamento. Qualsiasi tentativo di lettura, creazione o modifica del journal delle modifiche durante questo processo ha esito negativo con codice di errore **ERROR JOURNAL DELETE IN \_ \_ \_ \_ PROGRESS**.

È anche possibile usare il codice di [**controllo \_ FSCTL DELETE \_ USN \_ JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal) per determinare se è in corso un'eliminazione avviata da un altro processo. Ad esempio, l'applicazione, quando viene avviata, può determinare se è in corso un'eliminazione. Poiché le eliminazioni del journal vengono mantenute nei riavvii del sistema, i servizi e le applicazioni avviati al riavvio del sistema devono verificare la presenza di un'eliminazione in corso.

I journal delle modifiche non vengono necessariamente creati all'avvio. Per creare un journal delle modifiche, un amministratore può eseguire questa operazione in modo esplicito o avviare un altro servizio che richiede un journal delle modifiche.

 

 
