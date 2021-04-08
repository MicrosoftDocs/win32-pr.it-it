---
title: Handle di binding impliciti
description: Gli handle di binding impliciti consentono all'applicazione di selezionare un server specifico per eseguire le chiamate di procedura remota.
ms.assetid: cf4e179b-8d97-4597-89e6-c8967b9db6c7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5fda8501224d66518ad2e86f13fb769c4b2fa0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046854"
---
# <a name="implicit-binding-handles"></a>Handle di binding impliciti

Gli handle di binding impliciti consentono all'applicazione di selezionare un server specifico per eseguire le chiamate di procedura remota. Per informazioni dettagliate, vedere [Binding lato client](client-side-binding.md). Consentono inoltre al programma client/server di utilizzare binding autenticati. Ovvero il client può specificare le informazioni di autenticazione in un handle di binding implicito. La libreria di runtime RPC utilizza le informazioni di autenticazione per stabilire una sessione RPC autenticata tra il client e il server. Per altre informazioni, vedere [Sicurezza](security.md).

> [!Note]  
> Gli handle di binding impliciti non sono thread-safe. Le applicazioni multithread devono pertanto evitare di utilizzare handle di binding impliciti.

 

Quando nell'applicazione vengono utilizzate associazioni implicite, il client deve impostare le informazioni di binding in modo che sia possibile creare l'associazione. Dopo che il client ha creato un'associazione implicita, non è necessario passare gli handle di associazione alle procedure remote. La libreria RPC gestisce il resto dei meccanismi della sessione di comunicazione.

Il client archivia le informazioni di binding per un handle implicito in una variabile globale. Quando il compilatore MIDL genera lo stub e il file di intestazione del client dalla specifica dell'interfaccia nel file MIDL, genera anche il codice per una variabile di handle di binding globale. Il programma client Inizializza l'handle e quindi non vi fa riferimento finché non elimina l'associazione.

Per creare un handle implicito, è necessario specificare l' \[ attributo [**\_ handle implicito**](/windows/desktop/Midl/implicit-handle) \] in ACF per un'interfaccia, come indicato di seguito:

``` syntax
/* ACF file (complete) */
 
[
  implicit_handle(handle_t hHello)
]
interface hello
{
}
```

Il tipo di **handle \_ t** , usato nell'esempio precedente, è un tipo di dati MIDL usato per la definizione degli handle di associazione.

Dopo aver creato l'handle implicito, l'applicazione deve utilizzarla come parametro per le funzioni della libreria di runtime RPC. Non usare l'handle implicito come parametro per le chiamate di procedura remota. Nell'esempio di codice riportato di seguito viene illustrato l'utilizzo degli handle di associazione impliciti.

``` syntax
RPC_STATUS status;
status = RpcBindingFromStringBinding(
            pszStringBinding,
            &hHello);
 
status = MyRemoteProcedure();
 
status = RpcBindingFree(hHello);
...
```

Nell'esempio precedente, le funzioni della libreria run-time RPC [**errore in RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) e [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) richiedono entrambi l'handle di binding implicito da passare nei rispettivi elenchi di parametri. Tuttavia, la procedura remota MyRemoteProcedure non è stata eseguita perché non è una funzione della libreria di runtime RPC.

 

 