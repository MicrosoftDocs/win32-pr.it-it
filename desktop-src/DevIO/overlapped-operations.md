---
description: Le operazioni sovrapposte consentono a un thread di eseguire in background un'operazione di I/O dispendiosa in termini di tempo, lasciando il thread libero di eseguire altre attività.
ms.assetid: 8c0eb20d-685a-4750-8253-a87089b68509
title: Operazioni sovrapposte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ba148d0b2085e2c44e71c4c8d309f9a068223eebe8de8e239f13095c8ddd39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956890"
---
# <a name="overlapped-operations"></a>Operazioni sovrapposte

Le operazioni sovrapposte consentono a un thread di eseguire in background un'operazione di I/O dispendiosa in termini di tempo, lasciando il thread libero di eseguire altre attività. Per abilitare le operazioni di I/O sovrapposte in una risorsa di comunicazione, il thread deve specificare il flag **FILE \_ FLAG \_ OVERLAPPED** nella funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) all'apertura dell'handle. Per eseguire la [**funzione ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) [**o WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) come operazione sovrapposta, il thread chiamante deve specificare un puntatore a una [**struttura OVERLAPPED.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) La **struttura OVERLAPPED** deve contenere un handle per un oggetto evento di reimpostazione manuale (non di reimpostazione automatica). Il sistema imposta lo stato dell'oggetto evento su not-signaled quando una chiamata alla funzione di I/O viene restituita prima del completamento dell'operazione. Il sistema imposta lo stato dell'oggetto evento su segnalato quando l'operazione è stata completata. Il thread usa una funzione di attesa per controllare lo stato corrente dell'oggetto evento o per attendere che lo stato sia segnalato.

Le [**funzioni ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) [**e WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) possono essere eseguite solo come operazioni sovrapposte. Il thread chiamante specifica un puntatore alla [**funzione FileIOCompletionRoutine,**](/windows/desktop/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine) che viene eseguita al termine dell'operazione sovrapposta. La routine di completamento viene eseguita solo se il thread chiamante esegue un'operazione di avviso.

Per altre informazioni su oggetti evento, funzioni di attesa, attese avvisabili e routine di completamento, vedere [Informazioni sulla sincronizzazione.](/windows/desktop/Sync/about-synchronization)

 

 
