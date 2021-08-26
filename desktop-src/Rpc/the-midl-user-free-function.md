---
title: Funzione midl_user_free
description: La funzione midl \_ user free deve essere fornita dagli sviluppatori \_ RPC.
ms.assetid: 5e940e93-bdd4-48cc-b84e-654637699719
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd6ca52635da5bedb60fdc7f94165ad9c888c030d5fe3340c53dfc970a90ff49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080821"
---
# <a name="the-midl_user_free-function"></a>Funzione midl \_ user \_ free

La **funzione midl \_ user \_ free** deve essere fornita dagli sviluppatori RPC. Alloca memoria per gli stub RPC e le routine della libreria. La **funzione midl \_ user \_ free** deve corrispondere al prototipo seguente:

``` syntax
void __RPC_USER midl_user_free(void * pBuffer);
```

Il *parametro pBuffer* specifica un puntatore alla memoria da liberare. Sia l'applicazione client che l'applicazione server devono implementare la funzione **midl \_ user \_ free,** a meno che la compilazione non sia in modalità di compatibilità OSF ([**/osf**](/windows/desktop/Midl/-osf)). La **funzione midl \_ user \_ free** deve essere in grado di liberare tutta lo spazio di archiviazione allocato dall'utente [**midl \_ \_ allocare**](the-midl-user-allocate-function.md).

Le applicazioni e gli stub chiamano **gratuitamente \_ \_ l'utente midl** quando si gestiscono oggetti allocati:

-   L'applicazione server deve chiamare **l'utente midl \_ \_ free** per liberare la memoria allocata dall'applicazione, ad esempio quando si elimina un nodo di dati allocato dinamicamente.
-   Lo stub del server chiama **midl \_ user \_ free** per rilasciare memoria nel server dopo il marshalling di tutti gli argomenti out, in , negli argomenti out e \[ nel valore \] \[ \] \[ \] restituito dalla funzione.

Ad esempio, il programma di Windows RPC che visualizza "Hello, world" implementa **midl \_ user \_ free** in termini di funzione C free:


```C++
void __RPC_USER midl_user_free(void __RPC_FAR * p)
{
    free(p);
}
```



> [!Note]  
> Se il pacchetto RpcSs è abilitato (ad esempio, come risultato dell'uso dell'attributo enable allocate), il programma server deve usare \[ [**\_**](/windows/desktop/Midl/enable-allocate) \] [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) per liberare memoria. Per altre informazioni, vedere [RpcSs Memory Management Package](rpcss-memory-management-package.md).

 

 

 