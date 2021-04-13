---
title: attributo partial_ignore
description: L'attributo ACF \ partial \_ Ignore \ definisce una versione specializzata di \ Unique \ puntatori che fornisce la semantica facoltativa.
ms.assetid: 8a8f88b0-4a12-496d-bf77-ee57241b577b
keywords:
- attributo partial_ignore MIDL
topic_type:
- apiref
api_name:
- partial_ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82d133275ca77032341d160b51b95b20235c8f2a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397923"
---
# <a name="partial_ignore-attribute"></a>\_attributo parziale ignore

L'attributo ACF **\[ partial \_ Ignore \]** definisce una versione specializzata di puntatori **\[ univoci \]** che fornisce la semantica facoltativa.

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ partial_ignore [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="remarks"></a>Commenti

Quando si crea una funzione, è comune consentire agli utenti di specificare un puntatore non **null** ai dati restituiti facoltativi, spesso definito come un puntatore out facoltativo. Non è in genere necessario inizializzare la memoria a cui fa riferimento l'utente. Questa tecnica rappresenta un problema quando la funzione viene utilizzata tramite RPC.

Se il puntatore facoltativo-out è valido, ma punta a dati non inizializzati, RPC tenta di effettuare il marshalling dei dati e di inviarli al server, il che può causare la mancata riuscita del marshalling e l'interruzione della chiamata. Anche in caso di esito positivo del marshalling, una quantità potenzialmente elevata di dati inutili viene inviata al server.

Questi problemi vengono risolti contrassegnando il puntatore come **\[ in, out, Unique, partial \_ Ignore \]**. Devono essere presenti tutti e quattro gli attributi. Quando viene effettuato il marshalling di un puntatore di **\[ \_ Ignora \] parziale** sul lato client, gli unici dati inviati al server sono un indicatore che indica se il puntatore è **null**. Se il puntatore è diverso da **null**, la routine lato server riceve un puntatore valido a un blocco di memoria inizializzato con zeri. Se il puntatore è **null**, la routine lato server riceve un puntatore **null** .

In questa situazione, la dimensione massima del puntatore deve essere definita correttamente in fase di compilazione o in base ai parametri di input, perché il server deve allocare spazio per la posizione di memoria a cui punta. Un puntatore di **\[ stringa \]** semplice, ad esempio, non ha una dimensione ben definita perché la stringa viene terminata in modo implicito da un carattere null. In questo caso, se **\[ \_ si \]** specificano le dimensioni massime della stringa aggiungendo una dimensione, l'attributo otterrà il requisito di dimensione ben definito.

## <a name="examples"></a>Esempi

``` syntax
/* The MoveLeft function will move one position to the left and optionally return the previous position */
void MoveLeft([in, out, unique, partial_ignore] long *pPrevPosition);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**unico**](unique.md)
</dt> </dl>

 

 




