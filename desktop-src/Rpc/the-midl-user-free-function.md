---
title: Funzione midl_user_free
description: La \_ funzione User \_ Free MIDL deve essere fornita dagli sviluppatori RPC.
ms.assetid: 5e940e93-bdd4-48cc-b84e-654637699719
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4713ed05173b709780b6496f233051fa3adddff8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399635"
---
# <a name="the-midl_user_free-function"></a>\_Funzione gratuita dell'utente MIDL \_

La **funzione \_ User \_ Free MIDL** deve essere fornita dagli sviluppatori RPC. Alloca la memoria per gli stub RPC e le routine della libreria. La funzione della versione **\_ \_ gratuita dell'utente MIDL** deve corrispondere al prototipo seguente:

``` syntax
void __RPC_USER midl_user_free(void * pBuffer);
```

Il parametro *pbuffer* specifica un puntatore alla memoria che deve essere liberata. Sia l'applicazione client che l'applicazione server devono implementare la funzione di utilizzo **\_ \_ gratuito di MIDL** , a meno che non si stia eseguendo la compilazione in modalità OSF-Compatibility ([**/OSF**](/windows/desktop/Midl/-osf)). La **funzione \_ User \_ Free MIDL** deve essere in grado di liberare tutte le archiviazioni allocate dall' [**\_ utente MIDL \_ allocate**](the-midl-user-allocate-function.md).

Le applicazioni e gli stub chiamano l' **\_ utente MIDL \_ gratis** quando si gestiscono gli oggetti allocati:

-   L'applicazione server deve chiamare **l' \_ utente \_ MIDL** per liberare la memoria allocata dall'applicazione, ad esempio quando si elimina un nodo di dati allocato in modo dinamico.
-   Lo stub del server chiama l' **\_ utente MIDL \_ gratuitamente** a rilasciare la memoria nel server dopo aver eseguito il marshalling di tutti gli \[ \] argomenti out, \[ in \] , \[ out \] arguments e il valore restituito della funzione.

Ad esempio, il programma RPC Windows Sample che Visualizza "Hello, World" implementa l' **\_ utente MIDL \_ gratuitamente** in termini di funzione C gratuita:


```C++
void __RPC_USER midl_user_free(void __RPC_FAR * p)
{
    free(p);
}
```



> [!Note]  
> Se il pacchetto RpcSs è abilitato, ad esempio in seguito all'utilizzo dell' \[ attributo [**enable \_ allocate**](/windows/desktop/Midl/enable-allocate) \] , il programma server deve utilizzare [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) per liberare memoria. Per ulteriori informazioni, vedere il [pacchetto di gestione della memoria RPCSS](rpcss-memory-management-package.md).

 

 

 