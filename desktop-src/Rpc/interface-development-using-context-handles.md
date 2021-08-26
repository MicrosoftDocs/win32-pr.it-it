---
title: Sviluppo di interfacce tramite handle di contesto
description: In genere, si crea un handle di contesto specificando l'attributo \ context \_ handle\ in una definizione di tipo nel file IDL.
ms.assetid: e4caf91f-f92d-4aef-a20f-0a3073230640
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77e65e36384bda3d81526d5891eca92a77a67402e7cd3aa7af8b61e061a9d3b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020471"
---
# <a name="interface-development-using-context-handles"></a>Sviluppo di interfacce tramite handle di contesto

In genere, si crea un handle di contesto specificando l'attributo \[ [**\_ dell'handle**](/windows/desktop/Midl/context-handle) \] di contesto in una definizione di tipo nel file IDL. La definizione del tipo specifica anche in modo implicito una routine di esecuzione del contesto, che è necessario fornire. Se la comunicazione tra il client e il server si interrompe, il run-time del server richiama questa routine per eseguire la pulizia necessaria. Per altre informazioni sulle routine di esecuzione del contesto, vedere Routine di [esecuzione del contesto del server.](server-context-run-down-routine.md)

Un'interfaccia che utilizza un handle di contesto deve disporre di un handle di associazione per l'associazione iniziale, che deve avere luogo prima che il server possa restituire un handle di contesto. È possibile utilizzare un handle di associazione automatico, implicito o esplicito per creare l'associazione e stabilire il contesto.

Un handle di contesto deve essere [ * *del tipo void \** _](/windows/desktop/Midl/void) o di un tipo che viene risolto in _ [*void \** *](/windows/desktop/Midl/void). Il programma server esegue il cast al tipo richiesto.

> [!Note]  
> L'uso di in , out per i parametri di handle di contesto è sconsigliato, ad eccezione \[ [](/windows/desktop/Midl/in)delle routine [](/windows/desktop/Midl/out-idl) \] che chiudono gli handle di contesto. Se context gestisce i parametri contrassegnati in , out viene usato, non passare un handle di contesto NULL o non inizializzato dal \[ [](/windows/desktop/Midl/in)client [](/windows/desktop/Midl/out-idl) \] al server.  È **invece necessario** passare un puntatore NULL a un handle di contesto. Si noti che i parametri di handle di contesto \[ [**contrassegnati in**](/windows/desktop/Midl/in) \] non accettano **puntatori** NULL.

 

Nel frammento seguente di una definizione di interfaccia di esempio viene illustrato come un'applicazione distribuita può usare un handle di contesto per aprire un server e aggiornare un file di dati per ogni client.

L'interfaccia deve contenere una chiamata di procedura remota per inizializzare l'handle e impostarlo su un **valore** non Null. In questo esempio la funzione RemoteOpen esegue questa operazione. Specifica l'handle di contesto con un \[ [**attributo direzionale**](/windows/desktop/Midl/out-idl) \] out. In alternativa, è possibile restituire l'handle di contesto come valore restituito della procedura. In questo esempio, tuttavia, si passerà l'handle di contesto tramite l'elenco di parametri.

In questo esempio le informazioni di contesto sono un handle di file. Tiene traccia della posizione corrente nel file. L'interfaccia consente di creare un pacchetto dell'handle di file come handle di contesto e di passarlo come parametro alle chiamate di procedura remota. Una struttura contiene il nome del file e l'handle di file.

``` syntax
/* file: cxhndl.idl (fragment of interface definition file) */
typedef [context_handle] void * PCONTEXT_HANDLE_TYPE;
typedef [ref] PCONTEXT_HANDLE_TYPE * PPCONTEXT_HANDLE_TYPE;
 
short RemoteOpen([out] PPCONTEXT_HANDLE_TYPE pphContext,
    [in, string] unsigned char * pszFile);
 
void RemoteRead(
    [in] PCONTEXT_HANDLE_TYPE phContext,
    [out, size_is(cbBuf)] unsigned char achBuf[],
    [in, out] short *pcbBuf);
 
short RemoteClose([in, out] PPCONTEXT_HANDLE_TYPE pphContext);
```

La funzione RemoteOpen crea un handle di contesto valido non **Null.** Passa l'handle di contesto al client. Le chiamate di procedura remota successive, ad esempio RemoteRead, usano l'handle di contesto come puntatore in .

Oltre alla procedura remota che inizializza l'handle di contesto, l'interfaccia deve contenere una routine che libera il contesto del server e imposta l'handle di contesto su **NULL.** Nell'esempio precedente la funzione RemoteClose esegue questa operazione.

 

 