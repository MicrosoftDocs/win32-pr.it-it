---
description: Il filtro di corrispondenza dei criteri di ricerca notifica al driver di accettare i frame con un modello specifico in corrispondenza di un offset specifico.
ms.assetid: 8ee354f6-385d-49fa-baef-f70f6b3bd6a1
title: Scrittura del filtro PATTERNMATCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f92623c1fd0e1c47339b182a086975d9458f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310779"
---
# <a name="writing-the-patternmatch-filter"></a>Scrittura del filtro PATTERNMATCH

Il filtro di corrispondenza dei criteri di ricerca notifica al driver di accettare i frame con un modello specifico in corrispondenza di un offset specifico. È possibile specificare un massimo di quattro corrispondenze dettagliate, che possono essere combinate in istruzioni AND o OR logiche per la valutazione del driver Network Monitor.

Per implementare le corrispondenze dei criteri, usare le strutture di Network Monitor seguenti:

-   [**ESPRESSIONE**](expression.md)
-   [**ANDEXP**](andexp.md)
-   [**PATTERNMATCH**](patternmatch.md)

Per valutare un'istruzione **o** , combinare due a quattro criteri corrisponde a una struttura [**ANDEXP**](andexp.md) (PatternMatch1 \| \| PatternMatch2 \| \| PatternMatch3). Per valutare un'istruzione AND, combinare una o quattro strutture **ANDEXP** e una struttura di [**espressioni**](expression.md) (AndExp1 && AndExp2).

## <a name="pattern-match-definitions"></a>Definizioni delle corrispondenze dei criteri

Una singola corrispondenza di criteri è definita dalla struttura [**PATTERNMATCH**](patternmatch.md) . Una singola corrispondenza può funzionare in due modi.

In genere, il driver prenderà la base di offset, che può essere OFFSET di \_ base \_ rispetto \_ a \_ frame, offset di base \_ \_ rispetto \_ al \_ \_ protocollo effettivo, offset \_ \_ di base rispetto \_ a \_ IPX o offset \_ \_ rispetto \_ a IP, \_ e iniziare a contare in tale posizione. Il driver conteggia i byte di offset da tale posizione e quindi corrisponde ai dati trovati con i primi byte di lunghezza in **PatternToMatch**. Se sono uguali e i flag di corrispondenza criterio \_ \_ non sono \_ impostati, questo modello viene passato. Se sono diversi e i flag di \_ corrispondenza dei criteri \_ non sono \_ stati impostati, il modello viene passato. In caso contrario, questo modello ha esito negativo.

Oppure:

Se \_ \_ viene impostata la porta flag di corrispondenza dei flag \_ \_ specificata e la base è impostata su offset \_ rispetto \_ a \_ \_ IPX o offset \_ \_ rispetto \_ a \_ IP, il confronto è più complesso. Innanzitutto, il driver garantisce che il protocollo di base dell'offset sia presente, quindi il driver verifica che la porta specificata corrisponda alla porta nel frame. Infine, il driver garantisce che il membro **PatternToMatch** corrisponda a quello precedente, con l'eccezione che l'offset è dalla fine di IP o IPX. Si noti che se la base non è una di queste due, il \_ flag di corrispondenza dei flag della \_ \_ porta \_ specificata verrà ignorato e il modello verrà valutato come sopra.

Per valutare una corrispondenza con un solo criterio, una struttura di [**espressioni**](expression.md) deve avere un solo membro **AndExp** contenente un singolo criterio di ricerca.

La creazione del filtro di corrispondenza dei criteri prevede la creazione di strutture [**PATTERNMATCH**](patternmatch.md) e la loro combinazione logica con le strutture [**Expression**](expression.md) e [**ANDEXP**](andexp.md) .

**Per scrivere un filtro PATTERNMATCH**

1.  Nella struttura [**ANDEXP**](andexp.md) compilare la matrice con le corrispondenze dei criteri.
2.  Popola la struttura dell' [**espressione**](expression.md) con una matrice di membri **AndExp** .
3.  Non superare un totale di quattro corrispondenze del criterio per il filtro di acquisizione.
4.  Nella struttura [**PATTERNMATCH**](patternmatch.md) selezionare un tipo di flag.
5.  Selezionare una base di offset.
6.  Enumerare un valore di porta.
7.  Definire il valore di offset.
8.  Definire la lunghezza del modello.
9.  Enumerare il valore del modello.

## <a name="patternmatch-examples"></a>Esempi di PATTERNMATCH

Questo frame rappresenta un offset standard.

![frame offset standard](images/offs-pat.png)

Il frammento di codice viene implementato come segue:

``` syntax
Basis  ->   IP
Offset ->   4 (bytes)
Length ->   2 (bytes)
PatternToMatch[ ] = {x00, x00}
```

Questo frame raffigura un offset specificato dalla porta (rispetto a IPX).

![frame offset specificato dalla porta](images/stan-pat.png)

Il codice di esempio viene implementato come segue:

``` syntax
Port   ->   544
Basis  ->   IPX
Offset ->   2 (bytes)
Length ->   2 (bytes)
PatternToMatch[ ] = {x00, x00}
```

 

 



