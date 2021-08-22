---
title: Handle di associazione impliciti
description: Gli handle di associazione impliciti consentono all'applicazione di selezionare un server specifico per eseguire le chiamate di procedura remota.
ms.assetid: cf4e179b-8d97-4597-89e6-c8967b9db6c7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d49618ec505cc776c346a504fb19b65db539dadb90d030e45efbabcf08371db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929076"
---
# <a name="implicit-binding-handles"></a>Handle di associazione impliciti

Gli handle di associazione impliciti consentono all'applicazione di selezionare un server specifico per eseguire le chiamate di procedura remota. Per informazioni dettagliate, vedere [Associazione lato client](client-side-binding.md). Consentono inoltre al programma client/server di usare associazioni autenticate. In altre informazioni, il client può specificare le informazioni di autenticazione in un handle di associazione implicito. La libreria di runtime RPC usa le informazioni di autenticazione per stabilire una sessione RPC autenticata tra il client e il server. Per altre informazioni, vedere [Sicurezza](security.md).

> [!Note]  
> Gli handle di associazione implicita non sono thread-safe. Le applicazioni multi-thread devono pertanto evitare l'uso di handle di associazione impliciti.

 

Quando l'applicazione usa associazioni implicite, il client deve impostare le informazioni sull'associazione in modo che possa creare l'associazione. Dopo aver creato un'associazione implicita, il client non deve passare alcun handle di associazione alle procedure remote. La libreria RPC gestisce il resto dei meccanismi della sessione di comunicazione.

Il client archivia le informazioni di associazione per un handle implicito in una variabile globale. Quando il compilatore MIDL genera lo stub client e il file di intestazione dalla specifica dell'interfaccia nel file MIDL, genera anche il codice per una variabile di handle di associazione globale. Il programma client inizializza l'handle e quindi non fa riferimento a esso finché non elimina l'associazione.

Per creare un handle implicito, specificare l'attributo \[ [**\_ handle implicito**](/windows/desktop/Midl/implicit-handle) \] in ACF per un'interfaccia come indicato di seguito:

``` syntax
/* ACF file (complete) */
 
[
  implicit_handle(handle_t hHello)
]
interface hello
{
}
```

Il **tipo \_ handle t,** usato nell'esempio precedente, è un tipo di dati MIDL usato per definire gli handle di associazione.

Dopo aver creato l'handle implicito, l'applicazione deve usarlo come parametro per le funzioni della libreria di runtime RPC. Non usare l'handle implicito come parametro per le chiamate di procedura remota. Nell'esempio di codice seguente viene illustrato l'uso di handle di associazione impliciti.

``` syntax
RPC_STATUS status;
status = RpcBindingFromStringBinding(
            pszStringBinding,
            &hHello);
 
status = MyRemoteProcedure();
 
status = RpcBindingFree(hHello);
...
```

Nell'esempio precedente le funzioni della libreria di runtime RPC [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) e [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) richiedevano entrambi il passaggio dell'handle di associazione implicito nei relativi elenchi di parametri. Tuttavia, la procedura remota MyRemoteProcedure non è stata eseguita perché non è una funzione della libreria di runtime RPC.

 

 