---
title: Sviluppo di interfacce con handle di contesto
description: In genere, si crea un handle di contesto specificando l' \_ attributo \ context handle \ in una definizione di tipo nel file IDL.
ms.assetid: e4caf91f-f92d-4aef-a20f-0a3073230640
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8474d533b27ba1543a9d522dfa4478d306b33cf2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729311"
---
# <a name="interface-development-using-context-handles"></a>Sviluppo di interfacce con handle di contesto

In genere, si crea un handle di contesto specificando l'attributo dell' \[ [**\_ handle di contesto**](/windows/desktop/Midl/context-handle) in \] una definizione di tipo nel file IDL. La definizione del tipo specifica anche in modo implicito una routine di esecuzione del contesto, che è necessario fornire. Se la comunicazione tra il client e il server si interrompe, il tempo di esecuzione del server richiama questa routine per eseguire tutte le operazioni di pulizia necessarie. Per ulteriori informazioni sulle routine di esecuzione del contesto, vedere [routine di esecuzione del contesto del server](server-context-run-down-routine.md).

Un'interfaccia che utilizza un handle di contesto deve disporre di un handle di associazione per l'associazione iniziale, che deve essere eseguita prima che il server possa restituire un handle di contesto. È possibile utilizzare un handle di binding automatico, implicito o esplicito per creare l'associazione e stabilire il contesto.

Un handle di contesto deve essere del [**tipo \* void**](/windows/desktop/Midl/void) o un tipo che viene risolto in [**void \***](/windows/desktop/Midl/void). Il programma server ne esegue il cast al tipo richiesto.

> [!Note]  
> L'uso di \[ [**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl) \] per i parametri di handle di contesto è sconsigliato, ad eccezione delle routine che chiudono gli handle di contesto. Se il contesto gestisce i parametri contrassegnati \[ [**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl) \] vengono utilizzati, non passare un handle di contesto **null** o non inizializzato dal client al server. È necessario passare invece un puntatore **null** a un handle di contesto. Si noti che i parametri di handle \[ [**di**](/windows/desktop/Midl/in) contesto contrassegnati in non \] accettano puntatori **null** .

 

Il frammento di una definizione di interfaccia di esempio seguente mostra come un'applicazione distribuita può utilizzare un handle di contesto per aprire un server e aggiornare un file di dati per ogni client.

L'interfaccia deve contenere una chiamata di procedura remota per inizializzare l'handle e impostarlo su un valore non **null** . In questo esempio, la funzione RemoteOpen esegue questa operazione. Specifica l'handle di contesto con un \[ attributo [**out**](/windows/desktop/Midl/out-idl) \] Directional. In alternativa, è possibile restituire l'handle di contesto come valore restituito della stored procedure. Tuttavia, in questo esempio, l'handle del contesto verrà passato tramite l'elenco di parametri.

In questo esempio, le informazioni sul contesto sono un handle di file. Tiene traccia della posizione corrente nel file. L'interfaccia esegue il pacchetto dell'handle di file come handle di contesto e lo passa come parametro alle chiamate di procedura remota. Una struttura contiene il nome file e l'handle di file.

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

La funzione RemoteOpen crea un handle di contesto non **null** valido. Passa l'handle di contesto al client. Per le successive chiamate di procedure remote, ad esempio RemoteRead, viene utilizzato l'handle di contesto come puntatore in.

Oltre alla procedura remota che Inizializza l'handle del contesto, l'interfaccia deve contenere una procedura che libera il contesto del server e imposta l'handle del contesto su **null**. Nell'esempio precedente, la funzione RemoteClose esegue questa operazione.

 

 