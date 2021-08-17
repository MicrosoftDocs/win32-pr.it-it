---
description: I risultati di una query includono sia le righe restituite dalla query che un valore di rango per ogni riga se la colonna rank è inclusa nella clausola SELECT.
ms.assetid: 8655eec4-5151-4f82-b485-4dbef947df0d
title: Clausola RANK BY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33daf4865b0f7f08689802822d8c0d5b4d38702a1cb1f813563564e001811a6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462440"
---
# <a name="rank-by-clause"></a>Clausola RANK BY

I risultati di una query includono sia le righe restituite dalla query che un valore di rango per ogni riga se la colonna rank è inclusa nella clausola SELECT. I valori di classificazione vengono calcolati dal motore di ricerca e restituiti come numeri interi nell'intervallo da zero a 1000. Per rendere più significativi i risultati della classificazione, la query può controllare il modo in cui i valori di classificazione non elaborati vengono calcolati nella clausola RANK BY.

Questo argomento è organizzato come segue:

-   [Clausola RANK BY](#rank-by-clause)
-   [Funzione WEIGHT](#weight-function)
-   [Funzione COERCION](#coercion-function)

## <a name="rank-by-clause"></a>Clausola RANK BY

La sintassi per la clausola RANK BY è la seguente:


```
WHERE ( <search_condition> ) 
RANK BY [ ( ] <rank_specification> [ ) ]
```



La clausola RANK BY viene applicata alla condizione di ricerca immediatamente precedente, specificando in modo efficace un rango inferiore o superiore per le righe restituite da tale condizione di ricerca rispetto alle righe restituite da un'altra \_ condizione di ricerca. Le parentesi che circondano la \_ condizione di ricerca sono obbligatorie. Le parentesi che circondano la specifica di classificazione sono facoltative.

È possibile applicare più clausole RANK BY a una singola condizione. È possibile includere clausole RANK BY aggiuntive una dopo l'altra usando le parentesi.

> [!Note]  
> I predicati full-text restituiscono valori di rango nell'intervallo compreso tra 0 e 1000. I valori di classificazione per tutti i documenti corrispondenti a un predicato non full-text sono 1000. Le modifiche ai valori di classificazione devono prendere in considerazione queste informazioni.

 

La parte \_ relativa alla specifica di classificazione della clausola RANKBY identifica una o più funzioni da applicare ai valori di classificazione. La funzione WEIGHT applica un moltiplicatore al valore di rango non elaborato per una riga restituita. Minore è il moltiplicatore, minore è il valore di rango risultante. La funzione COERCION può essere usata per moltiplicare, aggiungere o impostare un valore di rango specifico per una riga restituita. Ogni specifica di classificazione può includere zero o una funzione WEIGHT e zero o più funzioni COERCION. Se entrambe le funzioni WEIGHT e COERCION sono incluse in una clausola RANK BY, la funzione WEIGHT deve essere la prima.

## <a name="weight-function"></a>Funzione WEIGHT

La sintassi della funzione WEIGHT è:


```
WEIGHT ( <weight_multipler> ) 
```



Il moltiplicatore deve essere un numero decimale da 0,001 a 1,000. Il valore di rango non elaborato restituito dal predicato della condizione di ricerca viene moltiplicato per il moltiplicatore di peso per impostare un nuovo valore di rango.

Nell'esempio seguente la funzione WEIGHT fornisce i documenti con la parola "Theresa" nel System.Document. Campo LastAuthor metà del valore di classificazione dei documenti con "Theresa" nel campo System.Author:


```
WHERE CONTAINS ( System.Author,'"Theresa"' ) 
         RANK BY WEIGHT ( 1.000 )
      OR
      CONTAINS ( System.Document.LastAuthor,'"Theresa"' ) 
         RANK BY WEIGHT ( 0.500 ) 
```



 

> [!Note]  
> Le funzionalità di ponderazione della colonna del predicato CONTAINS e FREETEXT supportano un formato abbreviato usando i due punti tra il termine di ricerca e il moltiplicatore ("software":0.25). La clausola RANK BY non supporta la forma abbreviata.

 

Quando si usa RANK BY WEIGHT, esiste una limitazione: non funziona con clausole CONTAINS che usano condizioni booleane. Ad esempio, l'esempio seguente non è consentito:


```
CONTAINS ( System.Author,'"Theresa" OR "Teresa"' ) RANK BY WEIGHT ( 0.400 )
```



## <a name="coercion-function"></a>Funzione COERCION

La funzione di coercizione rank può essere usata per modificare il valore di rango restituito per addizione o moltiplicazione o assegnando un valore specifico.

La sintassi della funzione COERCION è:


```
COERCION ( <coercion_operation> , <coercion_value> )
```



Il valore di coercizione è un valore intero.

Nella tabella seguente vengono descritte le impostazioni delle operazioni di coercizione disponibili.



| Operazione di coercizione | Descrizione                                                                                    | Intervallo di valori  |
|--------------------|------------------------------------------------------------------------------------------------|--------------|
| ABSOLUTE           | Il valore di rango restituito è il valore specificato nel valore di coercizione.                          | Da 0 a 1000    |
| ADD                | Il valore di rango restituito è la somma del valore di rango non elaborato e del valore di coercizione specificato.     | Da 0,001 a 1,0 |
| Moltiplicazione           | Il valore di rango restituito è il prodotto del valore di rango non elaborato e del valore di coercizione specificato. | Da 0,001 a 1,0 |



 

 

> [!IMPORTANT]
> La ricerca può restituire valori di classificazione solo nell'intervallo compreso tra 0 e 1000.

 

 

L'esempio seguente usa la funzione COERCION per impostare tutti i documenti con "computer" nel titolo in modo che abbia una classificazione di 1000, riducendo di un quarto la classificazione dei documenti contenenti sia "computer" che "software" nel titolo.


```
WHERE CONTAINS ( System.Title, 'computer' )
        RANK BY COERCION ( ABSOLUTE , 1000 )
        OR 
       CONTAINS ( System.Title, '"computer" AND "software"' )
        RANK BY COERCION ( MULTIPLY, 0.750 ) 
```



 

 



