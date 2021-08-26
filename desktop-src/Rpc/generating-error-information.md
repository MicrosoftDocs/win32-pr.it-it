---
title: Generazione di informazioni sugli errori
description: Se un server o un'applicazione rileva un errore irreversibile durante la chiamata tramite RPC, deve indicare al tempo di esecuzione RPC che si è verificato un errore e, idealmente, deve aggiungere informazioni sull'errore per facilitare la risoluzione dei problemi.
ms.assetid: 6658c387-94df-4d85-9749-53858f9e0f5f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7eb6868dfe11318e09b30217d5410a94ce32983ce64e75521c55fc5cc060ad0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020911"
---
# <a name="generating-error-information"></a>Generazione di informazioni sugli errori

Se un server o un'applicazione rileva un errore irreversibile durante la chiamata tramite RPC, deve indicare al tempo di esecuzione RPC che si è verificato un errore e, idealmente, deve aggiungere informazioni sull'errore per facilitare la risoluzione dei problemi.

## <a name="indicating-fatal-errors-to-the-rpc-run-time"></a>Indicazione di errori irreversibili al runtime RPC

Per indicare un errore in fase di esecuzione RPC, chiamare la funzione [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) nel thread RPC su cui è stata chiamata l'eccezione oppure [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) se la chiamata viene elaborata in modo asincrono su un altro thread. La restituzione di un codice di errore dalla routine del server, ad esempio la routine di gestione, non è sufficiente. In base alla specifica RPC, il valore restituito della funzione non ha alcuna semantica di errore nel server, indipendentemente dalle impostazioni del file idl/acf.

Quando si verifica un errore irreversibile nel componente, eseguire qualsiasi pulizia ritenuta necessaria e quindi chiamare la [**funzione RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) con il codice di errore. L'unica differenza tra **RpcRaiseException** e la restituzione di un codice di errore è che quando viene chiamato **RpcRaiseException,** non viene effettuato il marshalling dei parametri out. Questo è in genere un vantaggio, perché evitare parametri out non inizializzati non è necessario.

## <a name="generating-additional-extended-error-information"></a>Generazione di informazioni aggiuntive sugli errori estesi

Proprio come il run-time RPC compila una catena di record di errore, il server o l'applicazione può aggiungere i propri record alla catena. Questo approccio è spesso utile per il processo di risoluzione dei problemi. Ad esempio, un server può tentare di aprire un determinato file e ricevere un errore di file non trovato. La semplice restituzione dell'errore 2 non è utile per determinare il file mancante.

Al contrario, il server potrebbe chiamare la funzione [**RpcErrorAddRecord**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerroraddrecord) e fornire un parametro di stringa, ANSI o Unicode, nel record di errore che indica il percorso completo del file che stava cercando. Quando tutte queste informazioni vengono visualizzate sullo schermo dell'utente in un computer remoto, la risoluzione dei problemi diventa semplice. È possibile eseguire un semplice controllo dell'esistenza del file, soprattutto perché il nome del computer in questione è già fornito dal run-time RPC.

La [**chiamata alla funzione RpcErrorAddRecord**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerroraddrecord) potrebbe non riuscire se non è disponibile memoria sufficiente, anche se richiede solo pochi byte di spazio dell'heap. Inoltre, i record aggiunti da **RpcErrorAddRecord** si accumulano in un determinato thread. Il runtime normalmente pulisce tali record prima di chiamare la routine del server, ma se le informazioni sugli errori estesi vengono usate all'esterno di RPC, eseguire la pulizia dell'errore esteso accumulato nel thread chiamando [**RpcErrorClearInformation.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerrorclearinformation)

 

 




