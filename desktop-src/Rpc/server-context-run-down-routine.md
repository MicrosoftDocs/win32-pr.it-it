---
title: Routine di esecuzione del contesto del server
description: Se la comunicazione si interrompe mentre il server mantiene il contesto per conto del client, potrebbe essere necessaria una routine di pulizia per pulire lo stato gestito dal server per conto di un determinato client.
ms.assetid: b39654e4-6f03-43a0-8a5d-6f24bd0a529c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef3bab4477555e5a304627d026c7471874af50daceb9fe3e4484928c290a55d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035491"
---
# <a name="server-context-run-down-routine"></a>Routine di esecuzione del contesto del server

Se la comunicazione si interrompe mentre il server mantiene il contesto per conto del client, potrebbe essere necessaria una routine di pulizia per pulire lo stato gestito dal server per conto di un determinato client. Questa routine di pulizia è detta *routine di esecuzione del contesto.* Quando una connessione si interrompe, lo stub del server e la libreria di runtime chiameranno questa routine su ogni handle di contesto aperto dal client.

La routine di esecuzione del contesto è obbligatoria e viene dichiarata e denominata in modo implicito quando si applica l'attributo \[ **\_ dell'handle** di contesto \] a una definizione di tipo. Il server non chiamerà la routine di esecuzione del contesto se l'attributo \[ **\_ dell'handle** \] di contesto è stato applicato direttamente a un parametro.

La sintassi della routine di esecuzione del contesto è la seguente:

``` syntax
void __RPC_USER type-id_rundown (type-id);
```

Si noti che il nome del tipo determina il nome della routine di esecuzione del contesto.

Il frammento di codice seguente presenta una routine di esecuzione del contesto di esempio. che chiama la procedura RemoteClose usata nell'esempio [in](interface-development-using-context-handles.md)Sviluppo di interfacce tramite handle di contesto, [Sviluppo server](server-development-using-context-handles.md)con handle di contesto e Sviluppo client tramite handle [di contesto](client-development-using-context-handles.md). Questa procedura chiude l'handle di file, libera la memoria associata al file e assegna **NULL** all'handle di contesto. **L'assegnazione di NULL** è il risultato della chiamata alla funzione RemoteClose e non è necessaria in uno scenario di run-down. Il tempo di esecuzione RPC pulisce lo stato indipendentemente dal fatto che l'handle di contesto sia impostato su **NULL.**

``` syntax
//file: cxhndp.c (fragment of file containing remote procedures)
//The rundown routine is associated with the context handle type.  
void __RPC_USER PCONTEXT_HANDLE_TYPE_rundown(
    PCONTEXT_HANDLE_TYPE phContext)
{
    printf("Client died with an open file, closing it..\n");
    RemoteClose(&phContext);
    assert(phContext == 0);
}
```

 

 




