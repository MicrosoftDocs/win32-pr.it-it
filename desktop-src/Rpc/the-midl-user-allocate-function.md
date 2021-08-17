---
title: Funzione midl_user_allocate
description: La funzione midl \_ user allocate è una procedura che deve essere fornita dagli sviluppatori di applicazioni \_ RPC.
ms.assetid: 3def405c-da05-4cce-9dc4-499864a0de6e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8e064fc16a303660be96a4a3c47aa361c4616f54a8cb825c1fce5334543fc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924250"
---
# <a name="the-midl_user_allocate-function"></a>Funzione di allocazione \_ utente \_ midl

La **funzione midl \_ user \_ allocate** è una procedura che deve essere fornita dagli sviluppatori di applicazioni RPC. Alloca memoria per gli stub RPC e le routine della libreria. La **funzione di \_ \_ allocazione utente midl** deve corrispondere al prototipo seguente:

``` syntax
void __RPC_FAR * __RPC_USER midl_user_allocate (size_t cBytes);
```

Il *parametro cBytes* specifica il numero di byte da allocare. Sia le applicazioni client che le applicazioni server devono implementare la funzione di allocazione utente **midl, \_ \_** a meno che non si esezioni in modalità di compatibilità OSF (/osf). Le applicazioni e gli stub generati chiamano **l'utente midl \_ \_ allocare** direttamente o indirettamente per gestire gli oggetti allocati. Esempio:

-   Le applicazioni client e server chiamano **midl \_ user \_ allocate** per allocare memoria per l'applicazione, ad esempio quando si crea un nuovo nodo in un albero o in un elenco collegato.
-   Lo stub del server chiama **l'allocazione utente midl \_ \_** durante l'unmarshaling dei dati nello spazio degli indirizzi del server.
-   Lo stub client chiama **l'allocazione \_ \_ utente midl** durante l'annullamento delmarsaling dei dati dal server a cui fa riferimento un \[ puntatore \] out. Si noti che per i puntatori in , out e \[ \] \[ univoci, lo stub client chiama \] \[ \] **\_ \_ l'allocazione** utente midl \[ solo se il valore univoco del puntatore è \] Null nell'input e viene modificato in un valore non Null durante la chiamata. Se il \[ \] puntatore univoco non è Null nell'input, lo stub client scrive i dati associati nella memoria esistente.

Se **midl \_ user allocate \_ non** riesce a allocare memoria, deve restituire un puntatore Null.

La **funzione midl \_ user \_ allocate** deve restituire un puntatore allineato a 8 byte.

Ad esempio, i programmi di esempio forniti con Platform Software Development Kit (SDK) implementano l'allocazione utente **midl \_ \_** in termini di funzione C [**malloc**](pointers-and-memory-allocation.md):


```C++
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t cBytes)
{
    return((void __RPC_FAR *) malloc(cBytes));
}
```



> [!Note]  
> Se il pacchetto RpcSs è abilitato(ad esempio, come risultato dell'uso dell'attributo \[ [**\_ enable allocate),**](/windows/desktop/Midl/enable-allocate) usare \] [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) per allocare memoria sul lato server. Per altre informazioni \[ **sull'abilitazione \_ dell'allocazione,** \] vedere [MidL Reference](/windows/desktop/Midl/midl-language-reference).

 

 

 