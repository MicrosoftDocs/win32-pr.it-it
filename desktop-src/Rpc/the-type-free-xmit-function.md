---
title: Funzione type_free_xmit
description: Gli stub chiamano la funzione xmit di tipo \_ free per liberare la memoria \_ associata ai dati trasmessi.
ms.assetid: f15ce25b-d36c-4ee5-b796-f0aba1997047
keywords:
- type_free_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4c192e30ec4f18d70d6e694e6097cb77ee7a2338230868730dc37c1c3207010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016581"
---
# <a name="the-type_free_xmit-function"></a>Funzione \_ \_ xmit libera dal tipo

Gli stub chiamano la **funzione \_ \_ xmit** di tipo free per liberare la memoria associata ai dati trasmessi. Dopo che [il tipo dalla funzione \_ \_ xmit](the-type-from-xmit-function.md) converte i dati trasmessi nel tipo presentato, la memoria non è più necessaria. La funzione è definita come:

``` syntax
void __RPC_USER <type>_free_xmit(<xmit_type> __RPC_FAR *);
```

Il parametro è un puntatore alla memoria che contiene il tipo trasmesso.

In questo esempio la memoria contiene una matrice che si trova in una singola struttura . La funzione DOUBLE LINK TYPE free xmit usa la funzione fornita dall'utente \_ \_ \_ \_ midl \_ user free per liberare \_ la memoria:

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_free_xmit( 
     DOUBLE_XMIT_TYPE __RPC_FAR * pArray)
{
     midl_user_free(pArray);
}
```

 

 




