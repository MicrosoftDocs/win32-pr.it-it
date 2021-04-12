---
title: Interpretazione delle informazioni di binding
description: Microsoft RPC consente ai programmi client e server di accedere e interpretare le informazioni in un handle di binding.
ms.assetid: 0116b7a1-85f8-4860-8fba-4aa1960c6799
keywords:
- RPC, attività, interpretazione dell'associazione di procedura remota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423564a844bfbf959de8a2fcf4dfff5ae86b8b6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471734"
---
# <a name="interpreting-binding-information"></a>Interpretazione delle informazioni di binding

Microsoft RPC consente ai programmi client e server di accedere e interpretare le informazioni in un handle di binding. Ciò non significa che è possibile o tentare di accedere direttamente al contenuto di un handle di associazione. Microsoft RPC fornisce funzioni che consentono di impostare e recuperare le informazioni negli handle di associazione.

Per ottenere le informazioni in un handle di associazione, passare l'handle a [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding). Restituisce le informazioni di binding sotto forma di stringa. Per ogni chiamata a **RpcBindingToStringBinding**, è necessario disporre di una chiamata corrispondente alla funzione [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree).

È possibile chiamare la funzione [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) per analizzare la stringa ottenuta da [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding). Questa funzione alloca stringhe in modo che contengano le informazioni analizzate. Se non si desidera che analizzi un particolare elemento di informazioni di binding, passare un valore **null** come valore di tale parametro. Assicurarsi di chiamare [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) per ogni stringa allocata.

Nel frammento di codice seguente viene illustrato il modo in cui un'applicazione può chiamare queste funzioni.


```C++
RPC_STATUS status;
UCHAR *lpzStringBinding;
UCHAR *lpzProtocolSequence;
UCHAR *lpzNetworkAddress;
UCHAR *lpzEndpoint;
UCHAR *NetworkOptions;
 
// The variable hBindingHandle is a valid binding handle.
 
status = RpcBindingToStringBinding(hBindingHandle,&lpzStringBinding);
// Code to check the status goes here.
 
status = RpcStringBindingParse(
    lpzStringBinding,
    NULL,
    &lpzProtocolSequence;
    &lpzNetworkAddress;
    &lpzEndpoint;
    &NetworkOptions);
// Code to check the status goes here.
 
// Code to analyze and alter the binding information in the strings
// goes here.
 
status = RpcStringFree(&lpzStringBinding);
// Code to check the status goes here.
 
status = RpcStringFree(&lpzProtocolSequence);
// Code to check the status goes here.
 
status = RpcStringFree(&lpzNetworkAddress);
// Code to check the status goes here.
 
status = RpcStringFree(&NetworkOptions);
// Code to check the status goes here.
```



Il codice di esempio precedente chiama le funzioni [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) e [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) per ottenere e analizzare le informazioni in un handle di associazione valido. Si noti che il valore **null** è stato passato come secondo parametro a **RpcStringBindingParse**. In questo modo, la funzione ignorerà l'UUID dell'oggetto. Poiché non analizza l'UUID, **RpcStringBindingParse** non ne allocherà una stringa. Questa tecnica consente all'applicazione di allocare memoria solo per le informazioni di interesse per l'analisi e l'analisi.

 

 




