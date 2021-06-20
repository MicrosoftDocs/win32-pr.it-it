---
title: Applicazione client
description: Visualizzare la parte dell'applicazione client di un esempio RPC (Remote Procedure Call). L'esempio seguente deriva dall'applicazione "Hello World" in Platform SDK.
ms.assetid: 8c33801a-341a-4674-bd41-5bdca7e244fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e0b798543cd70e61f3ff1161503fa64710e53e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405014"
---
# <a name="the-client-application"></a>Applicazione client

L'esempio seguente deriva dall'applicazione "Hello World" nella directory RPC \\ Hello di Platform Software Development Kit (SDK). Il file di origine Helloc.c contiene una direttiva per includere il file di intestazione generato da MIDL, Hello.h. All'interno di Hello.h sono presenti direttive per includere Rpc.h e rpcndr.h, che contengono le definizioni per le routine di run-time RPC, **HelloProc** e **Shutdown** e i tipi di dati utilizzati dalle applicazioni client e server. Il compilatore MIDL deve essere usato con l'esempio seguente.

Poiché il client gestisce la connessione al server, l'applicazione client chiama le funzioni di run-time per stabilire un handle per il server e rilasciare questo handle al termine delle chiamate di procedura remota. La funzione [**RpcStringBindingCompose combina**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) i componenti dell'handle di associazione in una rappresentazione di stringa di tale handle e alloca memoria per l'associazione di stringhe. La funzione [**RpcBindingFromStringBinding crea**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) un handle di associazione server, **hello \_ ClientIfHandle,** per l'applicazione client da tale rappresentazione di stringa.

Nella chiamata a [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose)i parametri non specificano l'UUID perché questa esercitazione presuppone che sia presente una sola implementazione dell'interfaccia "hello". Inoltre, la chiamata non specifica un indirizzo di rete perché l'applicazione userà l'impostazione predefinita, ovvero il computer host locale. La sequenza di protocollo è una stringa di caratteri che rappresenta il trasporto di rete sottostante. L'endpoint è un nome specifico della sequenza di protocollo. In questo esempio vengono utilizzate named pipe per il trasporto di rete, quindi la sequenza del protocollo è "ncacn \_ np". Il nome dell'endpoint è \\ \\ "pipe hello".

Le chiamate di procedura remota effettive, **HelloProc** e **Shutdown,** vengono eseguite all'interno del gestore di eccezioni RPC, un set di macro che consentono di controllare le eccezioni che si verificano all'esterno del codice dell'applicazione. Se il modulo di run-time RPC segnala un'eccezione, il controllo passa al [**blocco RpcExcept.**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) Qui è possibile inserire il codice per eseguire la pulizia necessaria e quindi uscire normalmente. Questo programma di esempio informa semplicemente l'utente che si è verificata un'eccezione. Se non si desidera utilizzare le eccezioni, è possibile utilizzare gli attributi ACF [stato comm \_ ](/windows/desktop/Midl/comm-status) e lo stato [di \_ errore](/windows/desktop/Midl/fault-status) per segnalare gli errori.

Al termine delle chiamate di procedura remota, il client chiama [**innanzitutto RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) per liberare la memoria allocata per l'associazione di stringhe. Si noti che dopo aver creato l'handle di associazione, un programma client può liberare un'associazione di stringhe in qualsiasi momento. Il client chiama quindi [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) per rilasciare l'handle.


```C++
/* file: helloc.c */
#include <stdlib.h>
#include <stdio.h>
#include <ctype.h>
#include "hello.h" 
#include <windows.h>

void main()
{
    RPC_STATUS status;
    unsigned char * pszUuid             = NULL;
    unsigned char * pszProtocolSequence = "ncacn_np";
    unsigned char * pszNetworkAddress   = NULL;
    unsigned char * pszEndpoint         = "\\pipe\\hello";
    unsigned char * pszOptions          = NULL;
    unsigned char * pszStringBinding    = NULL;
    unsigned char * pszString           = "hello, world";
    unsigned long ulCode;
 
    status = RpcStringBindingCompose(pszUuid,
                                     pszProtocolSequence,
                                     pszNetworkAddress,
                                     pszEndpoint,
                                     pszOptions,
                                     &pszStringBinding);
    if (status) exit(status);

    status = RpcBindingFromStringBinding(pszStringBinding, &hello_ClientIfHandle);
 
    if (status) exit(status);
 
    RpcTryExcept  
    {
        HelloProc(pszString);
        Shutdown();
    }
    RpcExcept(1) 
    {
        ulCode = RpcExceptionCode();
        printf("Runtime reported exception 0x%lx = %ld\n", ulCode, ulCode);
    }
    RpcEndExcept
 
    status = RpcStringFree(&pszStringBinding); 
 
    if (status) exit(status);
 
    status = RpcBindingFree(&hello_IfHandle);
 
    if (status) exit(status);

    exit(0);
}

/******************************************************/
/*         MIDL allocate and free                     */
/******************************************************/
 
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t len)
{
    return(malloc(len));
}
 
void __RPC_USER midl_user_free(void __RPC_FAR * ptr)
{
    free(ptr);
}
```



 

 