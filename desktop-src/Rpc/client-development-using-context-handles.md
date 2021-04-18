---
title: Sviluppo di client con handle di contesto
description: L'unico utilizzo di un programma client per un handle di contesto consiste nel passarlo al server ogni volta che il client esegue una chiamata di procedura remota.
ms.assetid: fcbdfb1e-4f1e-4d22-9a3e-cf5a29d300d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c7d2dfca901085c743b25eb233ee2493b893e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515982"
---
# <a name="client-development-using-context-handles"></a>Sviluppo di client con handle di contesto

L'unico utilizzo di un programma client per un handle di contesto consiste nel passarlo al server ogni volta che il client esegue una chiamata di procedura remota. Non è necessario che l'applicazione client acceda al contenuto dell'handle. Non deve tentare di modificare i dati di gestione del contesto in alcun modo. Le procedure remote richiamate dal client eseguono tutte le operazioni necessarie sul contesto del server.

Prima di richiedere un handle di contesto da un server, i client devono stabilire un'associazione con il server. Il client può utilizzare un handle di binding automatico, implicito o esplicito. Con un handle di associazione valido, il client può chiamare una procedura remota sul server che restituisce un handle di contesto aperto (non **null**) o passa uno tramite un parametro **\[ out \]** nell'elenco di parametri della procedura remota.

I client possono utilizzare handle di contesto aperti in qualsiasi modo. Devono, tuttavia, invalidare il punto di gestione quando non è più necessario. Esistono due modi per eseguire questa operazione:

-   Per richiamare una procedura remota offerta dal programma server che libera il contesto e chiude l'handle del contesto (lo imposta su **null**).
-   Quando il server non è raggiungibile, chiamare la funzione [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) .

Il secondo approccio pulisce solo lo stato lato client e non esegue la pulizia dello stato sul lato server, quindi deve essere utilizzato solo quando si sospetta la partizione di rete e il client e il server eseguiranno una pulizia indipendente. Il server esegue la pulizia indipendente tramite la routine di esecuzione, il client esegue questa operazione utilizzando la funzione [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) .

Il frammento di codice seguente presenta un esempio di come un client può utilizzare un handle di contesto. Per visualizzare la definizione dell'interfaccia utilizzata in questo esempio, vedere [sviluppo di interfacce mediante handle di contesto](interface-development-using-context-handles.md). Per l'implementazione del server, vedere [sviluppo di server con handle di contesto](server-development-using-context-handles.md).

In questo esempio, il client chiama RemoteOpen per ottenere un handle di contesto che contiene dati validi. Il client può quindi utilizzare l'handle di contesto nelle chiamate a procedure remote. Poiché non necessita più dell'handle di associazione, il client può liberare l'handle esplicito utilizzato per creare l'handle del contesto:


```C++
// cxhndlc.c  (fragment of client side application)
printf("Calling the remote procedure RemoteOpen\n");
if (RemoteOpen(&phContext, pszFileName) < 0) 
{
    printf("Unable to open %s\n", pszFileName);
    Shutdown();
    exit(2);
}
 
// Now the context handle also manages the binding.
// The variable hBindingHandle is a valid binding handle.
status = RpcBindingFree(&hBindingHandle);
printf("RpcBindingFree returned 0x%x\n", status);
if (status) 
    exit(status);
```



Nell'applicazione client di questo esempio viene utilizzata una stored procedure denominata RemoteRead per leggere un file di dati nel server fino a quando non viene rilevata una fine del file. Chiude quindi il file chiamando RemoteClose. L'handle del contesto viene visualizzato come parametro nelle funzioni RemoteRead e RemoteClose come:


```C++
printf("Calling the remote procedure RemoteRead\n");
do 
{
    cbRead = 1024; // Using a 1K buffer
    RemoteRead(phContext, pbBuf, &cbRead);
    // cbRead contains the number of bytes actually read.
    for (int i = 0; i < cbRead; i++)
        putchar(*(pbBuf+i));
} while(cbRead);
 
printf("Calling the remote procedure RemoteClose\n");
if (RemoteClose(&phContext) < 0 ) 
{
    printf("Close failed on %s\n", pszFileName);
    exit(2);
}
```



 

 




