---
description: Gli amministratori possono creare, eliminare e ricreare i journal delle modifiche.
ms.assetid: 26cbacc2-d26b-434b-91b5-31aedc96da13
title: Creazione, modifica ed eliminazione di un journal delle modifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c8cf7296f93549e7d9ec05f5d614131cc342ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316788"
---
# <a name="creating-modifying-and-deleting-a-change-journal"></a>Creazione, modifica ed eliminazione di un journal delle modifiche

Gli amministratori possono creare, eliminare e ricreare i journal delle modifiche in modo. Un amministratore deve eliminare un journal quando il valore del numero di sequenza di aggiornamento (USN) corrente si avvicina al valore di USN massimo possibile, come indicato dal membro **MaxUsn** della struttura dei [**\_ \_ dati del journal USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_journal_data_v0) . Un amministratore potrebbe inoltre eliminare e ricreare un journal delle modifiche per recuperare spazio su disco. Per eseguire questa e tutte le altre operazioni del journal delle modifiche non a livello di codice, è necessario disporre dei privilegi di amministratore di sistema. Ovvero, è necessario essere un membro del gruppo Administrators.

Per creare o modificare un journal delle modifiche in un volume specificato a livello di codice, usare il codice di controllo [**FSCTL \_ Create \_ USN \_ Journal**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal) .

Quando si crea un nuovo Journal delle modifiche o se ne modifica uno esistente, il file system NTFS imposta le informazioni per il Journal delle modifiche dalle informazioni della struttura di [**\_ \_ \_ dati create USN Journal**](/windows/desktop/api/WinIoCtl/ns-winioctl-create_usn_journal_data) , che [**FSCTL \_ Create \_ USN \_ Journal**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal) accetta come input. **Crea \_ I \_ \_ dati del journal USN** sono i membri **MaximumSize** e **DeltaAllocazione**.

**MaximumSize** è la dimensione massima di destinazione per il Journal delle modifiche in byte. Il Journal delle modifiche può aumentare di dimensioni superiori rispetto a questo valore, ma in NTFS file system Checkpoint il file system NTFS esamina il Journal e lo taglia quando la dimensione supera il valore di **MaximumSize** e il valore di **DeltaAllocazione**. Ai checkpoint file system NTFS, il sistema operativo scrive i record nel file di log file system NTFS che consentono al file system NTFS di determinare quale elaborazione è necessaria per il ripristino in caso di errore.

**DeltaAllocazione** è il numero di byte aggiunti alla fine e rimossi dall'inizio del journal delle modifiche ogni volta che la memoria viene allocata o deallocata. In altre parole, l'allocazione e la deallocazione avvengono in unità di queste dimensioni. Un multiplo Integer di dimensioni del cluster è un valore ragionevole per questo membro.

Se un amministratore modifica un journal delle modifiche esistente per avere un valore **MaximumSize** più grande, ad esempio se un volume viene reindicizzato troppo spesso, il Journal delle modifiche riceve semplicemente le nuove voci fino a quando non supera le nuove dimensioni massime.

Per eliminare un journal delle modifiche, usare il codice di controllo [**\_ \_ \_ journal USN FSCTL Delete**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal) . Quando si usa questa operazione, vengono esaminati tutti i file nel volume e viene reimpostato l'USN per ogni file su zero. L'operazione Elimina quindi il Journal delle modifiche esistente. Questa operazione viene mantenute tra i riavvii del sistema finché non viene completata. Eventuali tentativi di lettura, creazione o modifica del journal delle modifiche durante questo processo hanno esito negativo e il codice **\_ di errore eliminazione del journal è \_ \_ in \_ corso**.

È anche possibile usare il codice di controllo del [**\_ \_ \_ journal USN FSCTL Delete**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal) per determinare se un'eliminazione avviata da un altro processo è in corso. Ad esempio, l'applicazione, quando viene avviata, può determinare se è in corso un'operazione di eliminazione. Poiché le eliminazioni del journal vengono mantenute tra i riavvii del sistema, le applicazioni e i servizi avviati al riavvio del sistema devono verificare la presenza di un'eliminazione continua.

I journal delle modifiche non vengono necessariamente creati all'avvio. Per creare un journal delle modifiche, un amministratore può eseguire questa operazione in modo esplicito o avviare un altro servizio che richiede un journal delle modifiche.

 

 
