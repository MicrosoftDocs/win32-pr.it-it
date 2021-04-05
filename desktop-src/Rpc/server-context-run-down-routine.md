---
title: Routine di esecuzione del contesto del server
description: Se la comunicazione si interrompe mentre il server mantiene il contesto per conto del client, potrebbe essere necessaria una routine di pulitura per pulire lo stato gestito dal server per conto di un determinato client.
ms.assetid: b39654e4-6f03-43a0-8a5d-6f24bd0a529c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ad8afb7f698a258d7c4403143e74d566f813a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045159"
---
# <a name="server-context-run-down-routine"></a>Routine di esecuzione del contesto del server

Se la comunicazione si interrompe mentre il server mantiene il contesto per conto del client, potrebbe essere necessaria una routine di pulitura per pulire lo stato gestito dal server per conto di un determinato client. Questa routine di pulizia è detta *routine di esecuzione del contesto*. Quando una connessione viene interrotta, lo stub del server e la libreria di runtime chiamerà questa routine a ogni handle di contesto aperto dal client.

La routine di esecuzione del contesto è obbligatoria ed è dichiarata in modo implicito e viene denominata quando si applica l'attributo dell' \[ **\_ handle di contesto** \] a una definizione di tipo. Il server non chiamerà la routine di esecuzione del contesto se l'attributo dell' \[ **\_ handle di contesto** \] è stato applicato direttamente a un parametro.

La sintassi di routine di esecuzione del contesto è:

``` syntax
void __RPC_USER type-id_rundown (type-id);
```

Si noti che il nome del tipo determina il nome della routine di esecuzione del contesto.

Il frammento di codice che segue presenta una routine di esecuzione del contesto di esempio. che chiama la stored procedure RemoteClose usata nell'esempio nello [sviluppo di interfacce usando handle di contesto](interface-development-using-context-handles.md), [lo sviluppo di server con handle di contesto](server-development-using-context-handles.md)e [lo sviluppo di client con handle di contesto](client-development-using-context-handles.md). Questa procedura chiude l'handle di file, libera la memoria associata al file e assegna **null** all'handle di contesto. L'assegnazione di **valori null** è il risultato della chiamata alla funzione RemoteClose e non è necessario in uno scenario di esecuzione. Il tempo di esecuzione RPC pulisce lo stato indipendentemente dal fatto che l'handle di contesto sia impostato su **null**.

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

 

 




