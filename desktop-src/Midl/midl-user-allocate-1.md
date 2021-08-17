---
title: midl_user_allocate attributo
description: La funzione midl \_ user allocate è una funzione che le applicazioni client e server forniscono per \_ allocare memoria.
ms.assetid: 0eaf6df5-791d-4f6d-8f49-cc1ce64e7ab4
keywords:
- midl_user_allocate attributo MIDL
topic_type:
- apiref
api_name:
- midl_user_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16729e0a0a422c8ed2d8a8f323b563cb6a268fcb041e6a9d2ba13a9c9b847d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117806659"
---
# <a name="midl_user_allocate-attribute"></a>Attributo midl \_ user \_ allocate

La **funzione midl \_ user \_ allocate** è una funzione che le applicazioni client e server forniscono per allocare memoria.

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate (size_t cBytes);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*cByte* 
</dt> <dd>

Specifica il numero di byte da allocare.

</dd> </dl>

## <a name="remarks"></a>Commenti

Sia le applicazioni client che le applicazioni server devono implementare la funzione di allocazione utente **midl, \_ \_** a meno che non si esezioni in modalità di compatibilità OSF ([**/osf**](-osf.md)). Le applicazioni e gli stub generati chiamano **l'allocazione \_ \_ utente midl** quando gestiscono oggetti a cui fanno riferimento i puntatori:

-   L'applicazione server deve chiamare **midl \_ user allocate \_ per** allocare memoria per l'applicazione, ad esempio quando si crea un nuovo nodo.
-   Lo stub del server chiama **l'allocazione \_ \_** utente midl durante l'unmarshaling dei dati puntati nello spazio indirizzi del server.
-   Lo stub client chiama **l'allocazione utente \_ \_ midl** durante l'unmarshaling dei dati dal server a cui fa riferimento un [**puntatore out.**](out-idl.md) Si noti che per i puntatori **\[** [**in**](in.md) **\]** , **\[ out \]** e **\[** [**univoci,**](unique.md) lo **\]** **\[ \]** stub client   chiama l'allocazione utente **midl \_ \_** solo se il valore univoco del puntatore è NULL per l'input e viene modificato in un valore non NULL durante la chiamata. Se il **\[ puntatore \]** univoco non è **NULL nell'input,** lo stub client scrive i dati associati nella memoria esistente.

Se **l'allocazione \_ \_ dell'utente midl** non riesce a allocare memoria, deve restituire un **puntatore NULL.**

È consigliabile che **l'allocazione utente midl \_ \_** restituirà un puntatore allineato a 8 byte.

## <a name="examples"></a>Esempi


```C++
#include <windows.h>

void __RPC_FAR * __RPC_API midl_user_allocate(size_t cBytes) 
{ 
    return(malloc(cBytes)); 
}
```



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**Allocare**](allocate.md)
</dt> <dt>

[**Matrici**](arrays-1.md)
</dt> <dt>

[Matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Attributi array e Sized-Pointer](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**Pollici**](in.md)
</dt> <dt>

[**midl \_ user \_ free**](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**in uscita**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**Unico**](unique.md)
</dt> </dl>

 

 