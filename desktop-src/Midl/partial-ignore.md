---
title: partial_ignore attributo
description: L'attributo ACF \ partial ignore\ definisce una versione specializzata dei \_ puntatori \ unique\ che fornisce una semantica facoltativa.
ms.assetid: 8a8f88b0-4a12-496d-bf77-ee57241b577b
keywords:
- partial_ignore attributo MIDL
topic_type:
- apiref
api_name:
- partial_ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac751e5b3bdb4a93c003e170333af8956048c9793630419fff0857d61f8c1f2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641974"
---
# <a name="partial_ignore-attribute"></a>attributo \_ partial ignore

L'attributo ACF **\[ partial \_ ignore \]** definisce una versione specializzata di **\[ puntatori univoci \]** che fornisce semantica facoltativa.

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ partial_ignore [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="remarks"></a>Commenti

Quando si crea una funzione, è comune consentire agli utenti di specificare un puntatore non **NULL** ai dati restituiti facoltativi, spesso definiti puntatori facoltativi out. Non è in genere necessario inizializzare la memoria a cui punta l'utente. Questa tecnica rappresenta un problema quando la funzione viene usata su RPC.

Se il puntatore optional-out è valido, ma punta a dati non inizializzati, RPC tenta di effettuare il marshalling dei dati e di inviarli al server, causando l'esito negativo del marshalling e l'interruzione della chiamata. Anche se il marshalling ha esito positivo, al server viene inviata una quantità potenzialmente grande di dati inutili.

Questi problemi vengono risolti contrassegnando il puntatore **\[ come in, out, unique, partial \_ ignore \]**. Tutti e quattro gli attributi devono essere presenti. Quando viene **\[ effettuato \_ il \]** marshalling di un puntatore ignore parziale sul lato client, gli unici dati inviati al server sono un indicatore che indica se il puntatore è **NULL.** Se il puntatore non è **NULL,** la routine sul lato server riceve un puntatore valido a un blocco di memoria inizializzato con zeri. Se il puntatore è **NULL,** la routine sul lato server riceve un **puntatore NULL.**

In questo caso, le dimensioni massime del puntatore devono essere ben definite in fase di compilazione o in base ai parametri di input, perché il server deve allocare spazio per il percorso di memoria a cui punta. Ad esempio, un **\[ puntatore di stringa \]** semplice non ha una dimensione ben definita perché la stringa viene terminata in modo implicito da un carattere NULL. In questo caso, se si specificano le dimensioni massime della stringa aggiungendo un attributo **\[ size \_ is \]** si o ottiene il requisito di dimensioni ben definito.

## <a name="examples"></a>Esempi

``` syntax
/* The MoveLeft function will move one position to the left and optionally return the previous position */
void MoveLeft([in, out, unique, partial_ignore] long *pPrevPosition);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**Unico**](unique.md)
</dt> </dl>

 

 




