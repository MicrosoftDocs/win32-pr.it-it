---
title: Puntatori e allocazione di memoria
description: La possibilità di modificare la memoria tramite puntatori spesso richiede che il server e il client allochino memoria sufficiente per gli elementi nella matrice.
ms.assetid: 8a49582a-9ae4-4f26-a172-bc8fe2aab65a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdd4c51207de093dfe2d32ec0c275aa7a05a317
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118231"
---
# <a name="pointers-and-memory-allocation"></a>Puntatori e allocazione di memoria

La possibilità di modificare la memoria tramite puntatori spesso richiede che il server e il client allochino memoria sufficiente per gli elementi nella matrice.

Quando uno stub deve allocare o liberare memoria, chiama funzioni della libreria di run-time che a loro volta chiamano le funzioni [**MIDL \_ User \_ allocate**](/windows/desktop/Midl/midl-user-allocate-1) e l' [**\_ utente MIDL \_ Free**](/windows/desktop/Midl/midl-user-free-1). Queste funzioni non sono incluse come parte della libreria di Runtime. È necessario scrivere versioni personalizzate di queste funzioni e collegarle all'applicazione. In questo modo, è possibile decidere come gestire la memoria. Quando si compila il file IDL in modalità OSF-Compatibility (**/OSF**), non è necessario implementare queste funzioni. È necessario scrivere queste funzioni nei prototipi seguenti:

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
```

Ad esempio, le versioni di queste funzioni per un'applicazione possono semplicemente chiamare funzioni della libreria standard:


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



 

 