---
description: I risultati di una query includono sia le righe restituite dalla query sia un valore di pertinenza per ogni riga se la colonna Rank è inclusa nella clausola SELECT.
ms.assetid: 8655eec4-5151-4f82-b485-4dbef947df0d
title: RANGO per clausola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5de7f7a63e33f43ba6387cbcea44a5f5b5ae8f99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225951"
---
# <a name="rank-by-clause"></a>RANGO per clausola

I risultati di una query includono sia le righe restituite dalla query sia un valore di pertinenza per ogni riga se la colonna Rank è inclusa nella clausola SELECT. I valori di pertinenza vengono calcolati dal motore di ricerca e vengono restituiti come numeri interi compresi tra 0 e 1000. Per rendere più significativi i risultati della classificazione, la query può controllare il modo in cui i valori di classificazione non elaborati vengono calcolati nella clausola RANK BY.

Questo argomento è organizzato nel modo seguente:

-   [RANGO per clausola](#rank-by-clause)
-   [WEIGHT (funzione)](#weight-function)
-   [Funzione di COERCIZIONe](#coercion-function)

## <a name="rank-by-clause"></a>RANGO per clausola

La sintassi per la clausola RANK BY è la seguente:


```
WHERE ( <search_condition> ) 
RANK BY [ ( ] <rank_specification> [ ) ]
```



La clausola RANK BY viene applicata alla condizione di ricerca \_ immediatamente precedente, specificando in modo efficace un rango inferiore o superiore per le righe restituite dalla condizione di ricerca rispetto alle righe restituite da un'altra condizione di ricerca. Sono necessarie le parentesi che racchiudono la condizione di ricerca \_ . Le parentesi che racchiudono la specifica di rango sono facoltative.

È possibile applicare più di una clausola RANK BY a una singola condizione. È possibile includere clausole ORDER BY aggiuntive una dopo l'altra usando le parentesi.

> [!Note]  
> I predicati full-text restituiscono valori di rango nell'intervallo compreso tra 0 e 1000. I valori di pertinenza per tutti i documenti corrispondenti a un predicato non full-text sono 1000. Le modifiche ai valori di pertinenza dovrebbero prendere in considerazione queste informazioni.

 

La \_ parte relativa alla specifica di rango della clausola RANKBY identifica una o più funzioni da applicare ai valori di rango. La funzione WEIGHT applica un moltiplicatore al valore di classificazione RAW per una riga restituita. Minore è il moltiplicatore, minore è il valore di pertinenza risultante. La funzione di COERCIZIONe può essere utilizzata per moltiplicare, aggiungere o impostare un valore di pertinenza specifico per una riga restituita. Ogni specifica di rango può includere una funzione di peso zero o una e zero o più funzioni di COERCIZIONe. Se in una clausola RANK BY sono incluse sia funzioni di PONDERAzione che di COERCIZIONe, la funzione WEIGHT deve essere prima.

## <a name="weight-function"></a>WEIGHT (funzione)

La sintassi della funzione WEIGHT è la seguente:


```
WEIGHT ( <weight_multipler> ) 
```



Il moltiplicatore deve essere un numero decimale compreso tra 0,001 e 1,000. Il valore di rango non elaborato restituito dal predicato della condizione di ricerca viene moltiplicato per il moltiplicatore di peso per impostare un nuovo valore di pertinenza.

Nell'esempio seguente la funzione WEIGHT assegna ai documenti la parola "Theresa" nel System.Document. Campo LastAuthor metà del valore di pertinenza dei documenti con "Theresa" nel campo System. Author:


```
WHERE CONTAINS ( System.Author,'"Theresa"' ) 
         RANK BY WEIGHT ( 1.000 )
      OR
      CONTAINS ( System.Document.LastAuthor,'"Theresa"' ) 
         RANK BY WEIGHT ( 0.500 ) 
```



 

> [!Note]  
> Le funzionalità di ponderazione delle colonne dei predicati CONTAINs e FREETEXT supportano un formato abbreviato utilizzando i due punti tra il termine di ricerca e il moltiplicatore ("software": 0,25). La clausola RANK BY non supporta il formato abbreviato.

 

Esiste una limitazione quando si usa RANK BY WEIGHT: non funziona con le clausole CONTAINs che usano condizioni booleane; ad esempio, l'esempio seguente non è consentito:


```
CONTAINS ( System.Author,'"Theresa" OR "Teresa"' ) RANK BY WEIGHT ( 0.400 )
```



## <a name="coercion-function"></a>Funzione di COERCIZIONe

La funzione di coercizione Rank può essere usata per modificare il valore di pertinenza restituito per addizione o moltiplicazione oppure assegnando un valore specifico.

La sintassi della funzione di COERCIZIONe è la seguente:


```
COERCION ( <coercion_operation> , <coercion_value> )
```



Il valore di coercizione è un valore intero.

Nella tabella seguente vengono descritte le impostazioni dell'operazione di coercizione disponibili.



| Operazione di coercizione | Descrizione                                                                                    | Intervallo di valori  |
|--------------------|------------------------------------------------------------------------------------------------|--------------|
| ABSOLUTE           | Il valore di pertinenza restituito è il valore specificato nel valore di coercizione.                          | da 0 a 1000    |
| ADD                | Il valore di pertinenza restituito è la somma del valore di rango non elaborato e del valore di coercizione specificato.     | da 0,001 a 1,0 |
| Moltiplicazione           | Il valore di pertinenza restituito è il prodotto del valore di classificazione non elaborato e il valore di coercizione specificato. | da 0,001 a 1,0 |



 

 

> [!IMPORTANT]
> La ricerca può restituire valori di rango solo nell'intervallo compreso tra 0 e 1000.

 

 

Nell'esempio seguente viene usata la funzione di COERCIZIONe per impostare tutti i documenti con "computer" nel titolo per avere un rango di 1000, riducendo di un trimestre il rango dei documenti che contengono sia "computer" che "software" nel titolo.


```
WHERE CONTAINS ( System.Title, 'computer' )
        RANK BY COERCION ( ABSOLUTE , 1000 )
        OR 
       CONTAINS ( System.Title, '"computer" AND "software"' )
        RANK BY COERCION ( MULTIPLY, 0.750 ) 
```



 

 



