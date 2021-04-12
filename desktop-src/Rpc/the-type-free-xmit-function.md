---
title: Funzione type_free_xmit
description: Gli stub chiamano il tipo \_ Free \_ Xmit Function per liberare la memoria associata ai dati trasmessi.
ms.assetid: f15ce25b-d36c-4ee5-b796-f0aba1997047
keywords:
- type_free_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b33d5cb8079d50923de2161b0384550829a5f22f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221508"
---
# <a name="the-type_free_xmit-function"></a>\_Funzione Xmit gratuita del tipo \_

Gli stub chiamano il **tipo \_ Free \_ Xmit** Function per liberare la memoria associata ai dati trasmessi. Quando il [tipo della funzione \_ \_ Xmit](the-type-from-xmit-function.md) converte i dati trasmessi nel tipo presentato, la memoria non è più necessaria. La funzione è definita come segue:

``` syntax
void __RPC_USER <type>_free_xmit(<xmit_type> __RPC_FAR *);
```

Il parametro è un puntatore alla memoria che contiene il tipo trasmesso.

In questo esempio la memoria contiene una matrice che si trova in una singola struttura. Il \_ tipo di collegamento doppia della funzione \_ \_ \_ Xmit Free USA la funzione fornita dall'utente MIDL \_ User \_ Free per liberare la memoria:

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_free_xmit( 
     DOUBLE_XMIT_TYPE __RPC_FAR * pArray)
{
     midl_user_free(pArray);
}
```

 

 




