---
title: Puntatori e allocazione di memoria
description: La possibilità di modificare la memoria tramite puntatori richiede spesso che il server e il client allocano memoria sufficiente per gli elementi nella matrice.
ms.assetid: 8a49582a-9ae4-4f26-a172-bc8fe2aab65a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23d634b209c1f6369429c432d5fad5d4e64b47aeae16778efd8916c00e65911e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927361"
---
# <a name="pointers-and-memory-allocation"></a>Puntatori e allocazione di memoria

La possibilità di modificare la memoria tramite puntatori richiede spesso che il server e il client allocano memoria sufficiente per gli elementi nella matrice.

Quando uno stub deve allocare o liberare memoria, chiama le funzioni della libreria di runtime che a loro volta chiamano le funzioni [**midl \_ user \_ allocate**](/windows/desktop/Midl/midl-user-allocate-1) e [**midl \_ user \_ free.**](/windows/desktop/Midl/midl-user-free-1) Queste funzioni non sono incluse nella libreria di runtime. È necessario scrivere le proprie versioni di queste funzioni e collegarle all'applicazione. In questo modo, è possibile decidere come gestire la memoria. Quando si compila il file IDL in modalità di compatibilità OSF (**/osf**), non è necessario implementare queste funzioni. È necessario scrivere queste funzioni nei prototipi seguenti:

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
```

Ad esempio, le versioni di queste funzioni per un'applicazione possono semplicemente chiamare funzioni di libreria standard:


```C++
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)
{
    return(malloc(len));
}

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
{
    free(ptr);
}
```



 

 