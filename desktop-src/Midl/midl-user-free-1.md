---
title: attributo midl_user_free
description: La funzione della versione \_ gratuita dell'utente MIDL \_ viene fornita dalle applicazioni client e server per deallocare la memoria allocata in modo dinamico.
ms.assetid: b5d8f133-ddd9-4b92-8540-611a03835be0
keywords:
- attributo midl_user_free MIDL
topic_type:
- apiref
api_name:
- midl_user_free
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53819035f700a948c9ca45c565310d7796516147
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337166"
---
# <a name="midl_user_free-attribute"></a>\_attributo gratuito dell'utente MIDL \_

La funzione della versione **\_ \_ gratuita dell'utente MIDL** viene fornita dalle applicazioni client e server per deallocare la memoria allocata in modo dinamico.

``` syntax
void __RPC_API midl_user_free(void __RPC_FAR * p);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*p* 
</dt> <dd>

Puntatore al blocco di memoria da liberare.

</dd> </dl>

## <a name="remarks"></a>Commenti

Sia l'applicazione client che l'applicazione server devono implementare la funzione **MIDL \_ User \_ Free** , a meno che non si stia eseguendo la compilazione in modalità OSF-Compatibility ([**/OSF**](-osf.md)). La **funzione \_ User \_ Free MIDL** deve essere in grado di liberare tutte le archiviazioni allocate dall' [**\_ utente MIDL \_ allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function).

Le applicazioni e gli stub chiamano l' **\_ utente MIDL \_ gratuitamente** quando si gestiscono oggetti a cui fanno riferimento i puntatori:

-   L'applicazione server deve chiamare **l' \_ utente MIDL \_ gratuitamente** per liberare la memoria allocata da ApplicationA ", ad esempio quando si elimina un nodo specificato.
-   Lo stub del server chiama l' **\_ utente MIDL \_ gratuitamente** a rilasciare la memoria nel server dopo aver eseguito il marshalling di tutti gli **\[** argomenti [**out**](out-idl.md) **\]** , **\[** [**in**](in.md), **\] out** arguments e il valore restituito.

## <a name="examples"></a>Esempi


```C++
#include <windows.h>

void __RPC_API midl_user_free(void __RPC_FAR * p) 
{ 
    free(p); 
}
```



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**matrici**](arrays-1.md)
</dt> <dt>

[Matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Attributi array e Sized-Pointer](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**\_alloca utente \_ MIDL**](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**unico**](unique.md)
</dt> </dl>

 

 