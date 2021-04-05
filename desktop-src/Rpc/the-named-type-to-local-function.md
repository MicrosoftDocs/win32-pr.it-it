---
title: Funzione named_type_to_local
description: Gli stub chiamano il \_ tipo denominato \_ nella \_ funzione locale per convertire i dati da un tipo trasmesso al tipo che sono presenti nell'applicazione.
ms.assetid: c272cc1f-e47b-4d5a-a4e2-cefeaeb8c175
keywords:
- named_type_to_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746cbdd01ea657408b1bf355f41b3b9dfba673a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044713"
---
# <a name="the-named_type_to_local-function"></a>Tipo denominato \_ \_ per la \_ funzione locale

Gli stub chiamano il **tipo denominato nella funzione \_ \_ \_ locale** per convertire i dati da un tipo trasmesso al tipo che sono presenti nell'applicazione. La funzione è definita come segue:

``` syntax
void __RPC_USER <named_type>_to_local( 
    <named_type> __RPC_FAR * _RPC_FAR * , 
    <local_type> __RPC_FAR * );
```

Il primo parametro punta ai dati trasmessi. La funzione imposta il secondo parametro in modo che punti ai dati presentati.

Il **\_ tipo denominato \_ per \_** la funzione locale deve gestire la memoria per il tipo presentato. La funzione deve allocare memoria per l'intera struttura di dati che inizia dall'indirizzo indicato dal secondo parametro, ad eccezione del parametro stesso (lo stub alloca memoria per il nodo radice e la passa alla funzione). Il valore del secondo parametro non può essere modificato durante la chiamata. La funzione può modificare il contenuto in corrispondenza di tale indirizzo.

 

 




