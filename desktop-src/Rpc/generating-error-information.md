---
title: Generazione di informazioni sugli errori
description: Se un server o un'applicazione rileva un errore irreversibile durante la chiamata tramite RPC, è necessario indicare al runtime RPC che si è verificato un errore e, idealmente, aggiungere informazioni sull'errore per facilitare la risoluzione dei problemi.
ms.assetid: 6658c387-94df-4d85-9749-53858f9e0f5f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b06a13e932034e6840479443e0b78f4c322c0b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298143"
---
# <a name="generating-error-information"></a>Generazione di informazioni sugli errori

Se un server o un'applicazione rileva un errore irreversibile durante la chiamata tramite RPC, è necessario indicare al runtime RPC che si è verificato un errore e, idealmente, aggiungere informazioni sull'errore per facilitare la risoluzione dei problemi.

## <a name="indicating-fatal-errors-to-the-rpc-run-time"></a>Segnalazione di errori irreversibili al runtime RPC

Per indicare un errore nel runtime RPC, chiamare la funzione [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) mentre sul thread RPC è stata chiamata l'eccezione o [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) se l'elaborazione della chiamata in modo asincrono in un altro thread. La restituzione di un codice di errore dalla routine del server, ad esempio la routine del Manager, non è sufficiente, in base alla specifica RPC, il valore restituito della funzione non presenta una semantica di errore nel server, indipendentemente dalle impostazioni del file IDL/ACF.

Quando si verifica un errore irreversibile nel componente, eseguire tutte le operazioni di pulizia ritenute necessarie, quindi chiamare la funzione [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) con il codice di errore. L'unica differenza tra **RpcRaiseException** e la restituzione di un codice di errore è quando viene chiamato il **RpcRaiseException** , i parametri out non vengono sottoposti a marshalling. Si tratta in genere di un vantaggio, perché evitare parametri non inizializzati non è necessario.

## <a name="generating-additional-extended-error-information"></a>Generazione di informazioni aggiuntive sugli errori estesi

Proprio come il tempo di esecuzione RPC compila una catena di record di errore, il server o l'applicazione può aggiungere i propri record alla catena. Questo approccio spesso facilita il processo di risoluzione dei problemi. Ad esempio, un server può tentare di aprire un file specifico e ricevere un errore di file non trovato. La semplice restituzione dell'errore 2 non è utile per determinare il file mancante.

Al contrario, il server può chiamare la funzione [**RpcErrorAddRecord**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerroraddrecord) e specificare un parametro di stringa, ANSI o Unicode, nel record di errore che indica il percorso completo del file che stava cercando. Quando tutte queste informazioni vengono visualizzate nella schermata utente in un computer remoto, la risoluzione dei problemi diventa semplice; un semplice controllo della presenza del file può essere eseguito, soprattutto perché il nome del computer in questione è già fornito dal tempo di esecuzione RPC.

La chiamata di funzione [**RpcErrorAddRecord**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerroraddrecord) potrebbe avere esito negativo se non è disponibile memoria sufficiente, anche se richiede solo pochi byte di spazio dell'heap. Inoltre, i record aggiunti da **RpcErrorAddRecord** si accumulano in un thread specifico. Il runtime di in genere pulisce tali record prima di chiamare la routine del server, ma se le informazioni estese sugli errori vengono utilizzate all'esterno di RPC, è necessario pulire l'errore esteso accumulato nel thread chiamando [**RpcErrorClearInformation**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerrorclearinformation).

 

 




