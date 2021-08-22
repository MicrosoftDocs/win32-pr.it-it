---
title: Funzione named_type_to_local
description: Gli stub chiamano il tipo denominato nella funzione locale per convertire i dati da un tipo trasmesso al tipo \_ \_ che presentano \_ all'applicazione.
ms.assetid: c272cc1f-e47b-4d5a-a4e2-cefeaeb8c175
keywords:
- named_type_to_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59fc1d45545c920ef19eb4c230045e62322833d3ef38e765357c29b20a48589c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924061"
---
# <a name="the-named_type_to_local-function"></a>Il tipo \_ denominato per la funzione \_ \_ locale

Gli stub chiamano il **tipo \_ denominato \_ \_** nella funzione locale per convertire i dati da un tipo trasmesso al tipo che presentano all'applicazione. La funzione è definita come:

``` syntax
void __RPC_USER <named_type>_to_local( 
    <named_type> __RPC_FAR * _RPC_FAR * , 
    <local_type> __RPC_FAR * );
```

Il primo parametro punta ai dati trasmessi. La funzione imposta il secondo parametro in modo che punti ai dati presentati.

Il **tipo denominato per la \_ \_ \_ funzione** locale deve gestire la memoria per il tipo presentato. La funzione deve allocare memoria per l'intera struttura di dati che inizia in corrispondenza dell'indirizzo indicato dal secondo parametro, ad eccezione del parametro stesso (lo stub alloca memoria per il nodo radice e lo passa alla funzione). Il valore del secondo parametro non può cambiare durante la chiamata. La funzione può modificare il contenuto in corrispondenza di tale indirizzo.

 

 




