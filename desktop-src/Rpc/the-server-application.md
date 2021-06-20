---
title: Applicazione server
description: Visualizzare la parte dell'applicazione server di un esempio RPC (Remote Procedure Call). L'esempio deriva dall'applicazione "Hello World" in Platform SDK.
ms.assetid: 82ccfd67-6626-49c4-8974-86ebc5841444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34b8a2bb66fd415a9b8f778134edb4903f88a717
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406064"
---
# <a name="the-server-application"></a>Applicazione server

L'esempio seguente deriva dall'applicazione "Hello World" nella directory RPC \\ Hello di Platform Software Development Kit (SDK). Il lato server dell'applicazione distribuita informa il sistema che i relativi servizi sono disponibili. Attende quindi le richieste del client. Il compilatore MIDL deve essere usato con l'esempio seguente.

A seconda delle dimensioni dell'applicazione e delle preferenze di scrittura del codice, è possibile scegliere di implementare procedure remote in uno o più file separati. In questo programma di esercitazione il file di origine Hellos.c contiene la routine del server principale. Il file Hellop.c contiene la procedura remota.

Il vantaggio di organizzare le procedure remote in file separati è che le procedure possono essere collegate a un programma autonomo per eseguire il debug del codice prima della conversione in un'applicazione distribuita. Quando le procedure funzionano nel programma autonomo, è possibile compilare e collegare i file di origine contenenti le procedure remote all'applicazione server. Come per il file di origine dell'applicazione client, il file di origine dell'applicazione server deve includere il file di intestazione Hello.h.

Il server chiama le funzioni di run-time RPC [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) e [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) per rendere disponibili al client le informazioni di associazione. Questo programma di esempio passa il nome dell'handle di interfaccia **a RpcServerRegisterIf.** Gli altri parametri sono impostati su **NULL.** Il server chiama quindi la [**funzione RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) per indicare che è in attesa di richieste client.

L'applicazione server deve includere anche le due funzioni di gestione della memoria chiamate dal server stub: [**midl \_ user \_ allocate**](the-midl-user-allocate-function.md) e [**midl \_ user \_ free.**](the-midl-user-free-function.md) Queste funzioni allocano e liberano memoria nel server quando una procedura remota passa parametri al server. In questo programma di esempio **midl \_ user \_ allocate** e **midl \_ user \_ free** sono semplicemente wrapper per le funzioni della libreria C [**malloc**](pointers-and-memory-allocation.md) e **free.** Si noti che, nelle dichiarazioni con inoltro generate dal compilatore MIDL, "MIDL" è in maiuscolo. Il file di intestazione Rpcndr.h definisce midl user free e midl user allocate rispettivamente come MIDL user free e \_ \_ \_ \_ \_ \_ MIDL \_ user \_ allocate.


```C++
/* file: hellos.c */
#include <stdlib.h>
#include <stdio.h>
#include <ctype.h>
#include "hello.h"
#include <windows.h>

void main()
{
    RPC_STATUS status;
    unsigned char * pszProtocolSequence = "ncacn_np";
    unsigned char * pszSecurity         = NULL; 
    unsigned char * pszEndpoint         = "\\pipe\\hello";
    unsigned int    cMinCalls = 1;
    unsigned int    fDontWait = FALSE;
 
    status = RpcServerUseProtseqEp(pszProtocolSequence,
                                   RPC_C_LISTEN_MAX_CALLS_DEFAULT,
                                   pszEndpoint,
                                   pszSecurity); 
 
    if (status) exit(status);
 
    status = RpcServerRegisterIf(hello_ServerIfHandle,  
                                 NULL,   
                                 NULL); 
 
    if (status) exit(status);
 
    status = RpcServerListen(cMinCalls,
                             RPC_C_LISTEN_MAX_CALLS_DEFAULT,
                             fDontWait);
 
    if (status) exit(status);
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



 

 




