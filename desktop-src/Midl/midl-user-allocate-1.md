---
title: attributo midl_user_allocate
description: La \_ \_ funzione di allocazione utente MIDL è una funzione fornita dalle applicazioni client e server per allocare memoria.
ms.assetid: 0eaf6df5-791d-4f6d-8f49-cc1ce64e7ab4
keywords:
- attributo midl_user_allocate MIDL
topic_type:
- apiref
api_name:
- midl_user_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4be10c5e1c7073afb3abf359c3ec2fb79a4335b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337375"
---
# <a name="midl_user_allocate-attribute"></a>\_attributo di \_ allocazione utente MIDL

La funzione di **\_ \_ allocazione utente MIDL** è una funzione fornita dalle applicazioni client e server per allocare memoria.

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate (size_t cBytes);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*cBytes* 
</dt> <dd>

Specifica il numero di byte da allocare.

</dd> </dl>

## <a name="remarks"></a>Commenti

Sia le applicazioni client che le applicazioni server devono implementare la funzione di **\_ \_ allocazione utente MIDL** , a meno che non si stia eseguendo la compilazione in modalità OSF-Compatibility ([**/OSF**](-osf.md)). Le applicazioni e gli stub generati chiamano l' **\_ utente MIDL \_ allocato** quando si gestiscono oggetti a cui fanno riferimento i puntatori:

-   L'applicazione server deve chiamare **MIDL \_ User \_ allocate** per allocare memoria per ApplicationA, ad esempio quando si crea un nuovo nodo.
-   Lo stub del server chiama l' **\_ utente MIDL \_ allocate** quando si esegue l'unmarshalling dei dati puntati nello spazio degli indirizzi del server.
-   Lo stub client chiama **l' \_ utente MIDL \_ allocate** quando si esegue l'unmarshalling dei dati dal server a cui fa riferimento un puntatore [**out**](out-idl.md) . Si noti che per i **\[** [](in.md) **\]** puntatori univoci in, **\[ out \]** e **\[** [**Unique**](unique.md) **\]** , lo stub client chiama l' **\_ utente MIDL \_ allocare** solo se il valore del puntatore **\[ univoco \]** è **null** per l'input e viene modificato in un valore non **null** durante la chiamata. Se per l'input il puntatore **\[ \] univoco** è diverso da **null** , lo stub client scrive i dati associati nella memoria esistente.

Se **\_ \_ allocare l'utente MIDL** non riesce ad allocare memoria, deve restituire un puntatore **null** .

È consigliabile che **MIDL \_ User \_ allocate** restituisca un puntatore a 8 byte allineato.

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

[**allocare**](allocate.md)
</dt> <dt>

[**matrici**](arrays-1.md)
</dt> <dt>

[Matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Attributi array e Sized-Pointer](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**\_utente MIDL \_ gratuito**](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**unico**](unique.md)
</dt> </dl>

 

 