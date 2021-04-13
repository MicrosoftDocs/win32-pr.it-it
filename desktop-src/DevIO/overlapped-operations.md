---
description: Le operazioni sovrapposte consentono a un thread di eseguire un'operazione di I/O che richiede molto tempo in background, lasciando il thread libero per eseguire altre attività.
ms.assetid: 8c0eb20d-685a-4750-8253-a87089b68509
title: Operazioni sovrapposte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d8dc9e39386e25129d3e7d7a5281a8299d54ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483269"
---
# <a name="overlapped-operations"></a>Operazioni sovrapposte

Le operazioni sovrapposte consentono a un thread di eseguire un'operazione di I/O che richiede molto tempo in background, lasciando il thread libero per eseguire altre attività. Per abilitare le operazioni di I/O sovrapposte su una risorsa di comunicazione, è necessario che il thread specifichi il flag di **file \_ \_ sovrapposto** nella funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) quando viene aperto l'handle. Per eseguire la funzione [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) o [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) come operazione sovrapposta, il thread chiamante deve specificare un puntatore a una struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) . La struttura **sovrapposta** deve contenere un handle per un oggetto evento di reimpostazione manuale (non di reimpostazione automatica). Il sistema imposta lo stato dell'oggetto evento su non segnalato quando una chiamata alla funzione I/O restituisce un risultato prima del completamento dell'operazione. Il sistema imposta lo stato dell'oggetto evento su segnalato quando l'operazione è stata completata. Il thread usa una funzione wait per verificare lo stato corrente dell'oggetto evento o per attendere la segnalazione dello stato.

Le funzioni [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) e [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) possono essere eseguite solo come operazioni sovrapposte. Il thread chiamante specifica un puntatore alla funzione [**FileIOCompletionRoutine**](/windows/desktop/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine) , che viene eseguita quando l'operazione sovrapposta viene completata. La routine di completamento viene eseguita solo se il thread chiamante esegue un'operazione di avviso.

Per ulteriori informazioni sugli oggetti evento, sulle funzioni di attesa, sulle attese avvisi e sulle routine di completamento, vedere [informazioni sulla sincronizzazione](/windows/desktop/Sync/about-synchronization).

 

 
