---
title: Funzione midl_user_allocate
description: La \_ funzione di \_ allocazione utente MIDL è una procedura che deve essere fornita dagli sviluppatori di applicazioni RPC.
ms.assetid: 3def405c-da05-4cce-9dc4-499864a0de6e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12b2e3196de79992f5856b7117b25f05ad782d26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118115"
---
# <a name="the-midl_user_allocate-function"></a>Funzione di \_ \_ allocazione utente MIDL

La funzione di **\_ \_ allocazione utente MIDL** è una procedura che deve essere fornita dagli sviluppatori di applicazioni RPC. Alloca la memoria per gli stub RPC e le routine della libreria. La funzione di **\_ \_ allocazione utente MIDL** deve corrispondere al prototipo seguente:

``` syntax
void __RPC_FAR * __RPC_USER midl_user_allocate (size_t cBytes);
```

Il parametro *cBytes* specifica il numero di byte da allocare. Sia le applicazioni client che le applicazioni server devono implementare la funzione di **\_ \_ allocazione utente MIDL** a meno che non si stia eseguendo la compilazione in modalità OSF-Compatibility (/OSF). Le applicazioni e gli stub generati chiamano l' **\_ utente MIDL \_ allocare** direttamente o indirettamente per gestire gli oggetti allocati. Ad esempio:

-   Le applicazioni client e server chiamano **MIDL \_ User \_ allocate** per allocare memoria per l'applicazione, ad esempio quando si crea un nuovo nodo in un albero o un elenco collegato.
-   Lo stub del server chiama l' **\_ utente MIDL \_ allocate** quando si esegue l'unmarshalling dei dati nello spazio degli indirizzi del server.
-   Lo stub client chiama **l' \_ utente MIDL \_ allocate** quando si esegue l'unmarshalling dei dati dal server a cui fa riferimento un \[ \] puntatore out. Si noti che per i \[ \] \[ \] \[ puntatori univoci in, out e Unique \] , lo stub client chiama l' **\_ utente MIDL \_ allocare** solo se il \[ valore del \] puntatore univoco è null per l'input e viene modificato in un valore non null durante la chiamata. Se \[ per l' \] input il puntatore univoco è diverso da null, lo stub client scrive i dati associati nella memoria esistente.

Se **\_ \_ allocare l'utente MIDL** non riesce ad allocare memoria, deve restituire un puntatore null.

La funzione di **\_ \_ allocazione utente MIDL** deve restituire un puntatore allineato a 8 byte.

Ad esempio, i programmi di esempio forniti con Platform Software Development Kit (SDK) implementano l' **\_ utente MIDL \_ allocato** in termini della funzione C [**malloc**](pointers-and-memory-allocation.md):


```C++
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t cBytes)
{
    return((void __RPC_FAR *) malloc(cBytes));
}
```



> [!Note]  
> Se il pacchetto RpcSs è abilitato (ad esempio, come risultato dell'utilizzo dell'attributo \[ [**enable \_ allocate**](/windows/desktop/Midl/enable-allocate) \] ), utilizzare [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) per allocare memoria sul lato server. Per altre informazioni su \[ **enable \_ allocate** \] , vedere [riferimento a MIDL](/windows/desktop/Midl/midl-language-reference).

 

 

 