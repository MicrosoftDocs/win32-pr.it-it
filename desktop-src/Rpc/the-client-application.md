---
title: Applicazione client
description: L'esempio seguente è relativo all'applicazione "Hello World" nella \\ directory Hello RPC di Platform Software Development Kit (SDK).
ms.assetid: 8c33801a-341a-4674-bd41-5bdca7e244fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f97c7c35e00d3f36c645bfad2825dbada5e3a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474038"
---
# <a name="the-client-application"></a>Applicazione client

L'esempio seguente è relativo all'applicazione "Hello World" nella \\ directory Hello RPC di Platform Software Development Kit (SDK). Il file di origine Helloc. c contiene una direttiva per includere il file di intestazione generato da MIDL, Hello. h. All'interno di Hello. h sono presenti direttive che includono RPC. h e Rpcndr. h, che contengono le definizioni per le routine della fase di esecuzione RPC, **HelloProc** e **Shutdown** e i tipi di dati utilizzati dalle applicazioni client e server. Il compilatore MIDL deve essere usato con l'esempio seguente.

Poiché il client gestisce la connessione al server, l'applicazione client chiama le funzioni di runtime per stabilire un handle per il server e per rilasciare questo handle dopo il completamento delle chiamate di procedura remota. La funzione [**errore in RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) combina i componenti dell'handle di associazione in una rappresentazione di stringa di tale handle e alloca memoria per l'associazione di stringa. La funzione [**errore in RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) crea un handle di associazione server, **Hello \_ ClientIfHandle**, per l'applicazione client da tale rappresentazione di stringa.

Nella chiamata a [**errore in RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose), i parametri non specificano l'UUID perché in questa esercitazione si presuppone che esista una sola implementazione dell'interfaccia "Hello". Inoltre, la chiamata non specifica un indirizzo di rete perché l'applicazione utilizzerà il valore predefinito, ovvero il computer host locale. La sequenza di protocollo è una stringa di caratteri che rappresenta il trasporto di rete sottostante. L'endpoint è un nome specifico della sequenza del protocollo. Questo esempio USA named pipe per il trasporto di rete, quindi la sequenza di protocollo è "ncacn \_ NP". Il nome dell'endpoint è " \\ pipe \\ Hello".

Le chiamate a procedure remote effettive, **HelloProc** e **Shutdown**, avvengono all'interno del gestore di eccezioni RPC, ovvero un set di macro che consentono di controllare le eccezioni che si verificano all'esterno del codice dell'applicazione. Se il modulo della fase di esecuzione RPC segnala un'eccezione, il controllo passa al blocco [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) . Qui è possibile inserire il codice per eseguire tutte le operazioni di pulizia necessarie, quindi uscire normalmente. Questo programma di esempio informa semplicemente l'utente che si è verificata un'eccezione. Se non si desidera utilizzare le eccezioni, è possibile utilizzare lo [ \_ stato di comunicazione](/windows/desktop/Midl/comm-status) degli attributi ACF [e \_ lo stato di errore](/windows/desktop/Midl/fault-status) per segnalare gli errori.

Una volta completate le chiamate di procedura remota, il client chiama prima [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) per liberare la memoria allocata per l'associazione di stringa. Si noti che dopo aver creato l'handle di binding, un programma client può liberare un'associazione di stringa in qualsiasi momento. Il client chiama quindi [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) per rilasciare l'handle.


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



 

 