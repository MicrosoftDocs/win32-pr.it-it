---
title: Funzione named_type_from_local
description: Gli stub chiamano il \_ tipo denominato \_ dalla \_ funzione locale.
ms.assetid: ba35e2fb-957e-4e62-b0d4-ae76e30fa343
keywords:
- named_type_from_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94606a197f3763770db8e0d455a9d0b09f5dab0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329124"
---
# <a name="the-named_type_from_local-function"></a>Il \_ tipo denominato \_ della \_ funzione locale

Gli stub chiamano il \_ tipo denominato \_ dalla \_ funzione locale. Converte il tipo utilizzato dall'applicazione nel tipo in cui vengono trasmessi gli stub attraverso la rete. La funzione è definita come segue:

``` syntax
void __RPC_USER <named_type>_from_local ( 
    <local_type> __RPC_FAR *, <named_type> __RPC_FAR * __RPC_FAR *);
```

Il primo parametro è un puntatore ai dati dell'applicazione. Il secondo parametro è un puntatore a un puntatore. La funzione la punta ai dati trasmessi. La funzione deve allocare memoria per il tipo trasmesso.

 

 




