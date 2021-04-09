---
title: Applicazione server
description: L'esempio seguente è relativo all'applicazione "Hello World" nella \\ directory Hello RPC di Platform Software Development Kit (SDK).
ms.assetid: 82ccfd67-6626-49c4-8974-86ebc5841444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e6f13e2c8fecdcff820c62f3076dd2a8edd1a5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856197"
---
# <a name="the-server-application"></a>Applicazione server

L'esempio seguente è relativo all'applicazione "Hello World" nella \\ directory Hello RPC di Platform Software Development Kit (SDK). Il lato server dell'applicazione distribuita informa il sistema che i servizi sono disponibili. Attende quindi le richieste del client. Il compilatore MIDL deve essere usato con l'esempio seguente.

A seconda delle dimensioni dell'applicazione e delle preferenze di codifica, è possibile scegliere di implementare procedure remote in uno o più file distinti. In questo programma di esercitazione, il file di origine Hells. c contiene la routine del server principale. Il file ciau. c contiene la procedura remota.

Il vantaggio di organizzare le procedure remote in file distinti è che le procedure possono essere collegate a un programma autonomo per eseguire il debug del codice prima che venga convertito in un'applicazione distribuita. Una volta che le procedure funzionano nel programma autonomo, è possibile compilare e collegare i file di origine contenenti le procedure remote con l'applicazione server. Come per il file di origine dell'applicazione client, il file di origine dell'applicazione server deve includere il file di intestazione Hello. h.

Il server chiama le funzioni di runtime RPC [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) e [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) per rendere disponibili al client le informazioni di binding. Questo programma di esempio passa il nome dell'handle dell'interfaccia a **RpcServerRegisterIf**. Gli altri parametri sono impostati su **null**. Il server chiama quindi la funzione [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) per indicare che è in attesa di richieste client.

L'applicazione server deve includere anche le due funzioni di gestione della memoria chiamate dallo stub del server: [**MIDL \_ User \_ allocate**](the-midl-user-allocate-function.md) e [**MIDL \_ User \_ Free**](the-midl-user-free-function.md). Queste funzioni allocano e liberano memoria sul server quando una procedura remota passa parametri al server. In questo programma di esempio **, MIDL \_ User \_ allocate** e **MIDL \_ User \_ Free** sono semplicemente wrapper per le funzioni C-Library [**malloc**](pointers-and-memory-allocation.md) e **Free**. Si noti che nelle dichiarazioni con estensione generate dal compilatore MIDL, "MIDL" è maiuscolo. Il file di intestazione Rpcndr. h definisce l'utente MIDL \_ \_ Free e MIDL \_ User \_ ALLOCAte per essere MIDL user \_ \_ Free e MIDL user \_ \_ allocate, rispettivamente.


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



 

 




