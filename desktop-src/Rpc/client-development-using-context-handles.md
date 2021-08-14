---
title: Sviluppo client tramite handle di contesto
description: L'unico uso di un programma client per un handle di contesto è passarlo al server ogni volta che il client esegue una chiamata di procedura remota.
ms.assetid: fcbdfb1e-4f1e-4d22-9a3e-cf5a29d300d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ff599bebdf042bc2021d53538cff1c0203d2de875bdc52c50a72675b73a47f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931842"
---
# <a name="client-development-using-context-handles"></a>Sviluppo client tramite handle di contesto

L'unico uso di un programma client per un handle di contesto è passarlo al server ogni volta che il client esegue una chiamata di procedura remota. L'applicazione client non deve accedere al contenuto dell'handle. Non deve tentare di modificare i dati dell'handle di contesto in alcun modo. Le procedure remote richiamate dal client eseguono tutte le operazioni necessarie nel contesto del server.

Prima di richiedere un handle di contesto da un server, i client devono stabilire un'associazione con il server. Il client può usare un handle di associazione automatico, implicito o esplicito. Con un handle di associazione valido, il client può chiamare una procedura remota nel server che restituisce un handle di contesto aperto (non **NULL)** o ne passa uno tramite un parametro **\[ out \]** nell'elenco di parametri della procedura remota.

I client possono usare gli handle di contesto aperti in qualsiasi modo richiesto. È tuttavia consigliabile invalidare l'handle quando non è più necessario. A tale scopo, è possibile procedere in due modi:

-   Per richiamare una procedura remota offerta dal programma server che libera il contesto e chiude l'handle di contesto (impostarlo su **NULL).**
-   Quando il server non è raggiungibile, chiamare la [**funzione RpcSsDestroyClientContext.**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext)

Il secondo approccio pulisce solo lo stato sul lato client e non pulisce lo stato sul lato server, quindi deve essere usato solo quando si sospetta la partizione di rete e il client e il server eseereranno una pulizia indipendente. Il server esegue la pulizia indipendente tramite la routine run-down, il client lo esegue usando la [**funzione RpcSsDestroyClientContext.**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext)

Il frammento di codice seguente presenta un esempio di come un client potrebbe usare un handle di contesto. Per visualizzare la definizione dell'interfaccia utilizzata in questo esempio, vedere [Sviluppo di interfacce con handle di contesto](interface-development-using-context-handles.md). Per l'implementazione del server, vedere [Sviluppo di server tramite handle di contesto](server-development-using-context-handles.md).

In questo esempio il client chiama RemoteOpen per ottenere un handle di contesto contenente dati validi. Il client può quindi usare l'handle di contesto nelle chiamate di procedura remota. Poiché non richiede più l'handle di associazione, il client può liberare l'handle esplicito usato per creare l'handle di contesto:


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



L'applicazione client in questo esempio usa una procedura denominata RemoteRead per leggere un file di dati nel server fino a quando non viene rilevata una fine del file. Chiude quindi il file chiamando RemoteClose. L'handle di contesto viene visualizzato come parametro nelle funzioni RemoteRead e RemoteClose come:


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



 

 




