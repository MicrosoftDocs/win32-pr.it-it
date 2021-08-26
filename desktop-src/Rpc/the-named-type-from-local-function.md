---
title: Funzione named_type_from_local
description: Gli stub chiamano il tipo \_ denominato \_ dalla funzione \_ locale.
ms.assetid: ba35e2fb-957e-4e62-b0d4-ae76e30fa343
keywords:
- named_type_from_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c294398913a3bf6fe8b88eed5c42ceec84abf6b23ed994c85ff0fae8f21f2e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127621"
---
# <a name="the-named_type_from_local-function"></a>Tipo denominato \_ \_ dalla funzione \_ locale

Gli stub chiamano il tipo \_ denominato \_ dalla funzione \_ locale. Converte il tipo utilizzato dall'applicazione nel tipo che gli stub trasmettono attraverso la rete. La funzione è definita come:

``` syntax
void __RPC_USER <named_type>_from_local ( 
    <local_type> __RPC_FAR *, <named_type> __RPC_FAR * __RPC_FAR *);
```

Il primo parametro è un puntatore ai dati dell'applicazione. Il secondo parametro è un puntatore a un puntatore . La funzione punta ai dati trasmessi. La funzione deve allocare memoria per il tipo trasmesso.

 

 




