---
description: Una funzione di aggregazione esegue un calcolo su un set di valori e restituisce un valore. In questo modo è possibile generare statistiche di riepilogo per i gruppi multi-livello con un sovraccarico minimo.
ms.assetid: 82a93f57-8273-45bf-81d7-50a673845ae1
title: Funzioni di aggregazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d504a9343116bc23e847728716eeaa79fc2d26d993e962dd81ccd43669e22a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094957"
---
# <a name="aggregate-functions"></a>Funzioni di aggregazione

Una funzione di aggregazione esegue un calcolo su un set di valori e restituisce un valore. In questo modo è possibile generare statistiche di riepilogo per i gruppi multi-livello con un sovraccarico minimo.

## <a name="about-aggregate-functions"></a>Informazioni sulle funzioni di aggregazione

Le funzioni di aggregazione Windows ricerca Structured Query Language (SQL) hanno la sintassi seguente:


```
AGGREGATE <function> [AS <label>] [,<function> [AS <label>]]*
```



La parte della funzione può includere una delle funzioni e della sintassi seguenti:



| Funzione                                                              | Descrizione                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AVG( <column> )                                                   | Restituisce la media dei valori in un gruppo. Si applica solo ai numeri.                                                                                                                                      |
| BYFREQUENCY( <column> , <N> )                                | Restituisce i valori di colonna N più frequenti dai risultati nel gruppo. Include anche il numero di volte in cui si è verificato ogni valore e gli identificatori di documento per i risultati che contengono ogni valore restituito. |
| CHILDCOUNT()                                                          | Restituisce il numero di elementi in un gruppo (esclusi i sottogruppi). Se sono presenti più livelli di raggruppamento, viene restituito il numero di gruppi figlio immediati.                                                  |
| COUNT()                                                               | Restituisce il numero di elementi in un gruppo e in tutti i sottogruppi.                                                                                                                                                   |
| DATERANGE( <column> )                                             | Restituisce i limiti inferiore e superiore dei valori di colonna trovati nel gruppo di risultati del gruppo. Valido solo per le proprietà filetime.                                                                               |
| FIRST( <column> , <N> )                                      | Restituisce i primi N valori di colonna dai risultati foglia trovati in un gruppo.                                                                                                                                       |
| MAX( <column> )                                                   | Restituisce il valore massimo dell'espressione. Si applica solo a numeri o date.                                                                                                                              |
| MIN( <column> )                                                   | Restituisce il valore minimo nell'espressione. Si applica solo a numeri o date.                                                                                                                              |
| REPRESENTATIVEOF( <column> , <idRepresentative> , <N> ) | Restituisce N valori idRepresentative, ognuno selezionato da uno dei subset di risultati con un valore di colonna univoco. Ogni valore viene restituito anche con un identificatore di documento con il valore idRepresentative. |
| SUM( <column> )                                                   | Restituisce la somma dei valori in un gruppo. Si applica solo ai numeri.                                                                                                                                          |



 

 

> [!Note]  
> Le aggregazioni vengono restituite come singole colonne. Sono per lo più tipi semplici, ad eccezione di ByFrequency, First, DateRange e RepresentativeOf, che vengono restituiti come tipi composti.

 

È possibile utilizzare qualsiasi colonna numerica o di data per le aggregazioni e non solo quelle presenti nella clausola SELECT. Non è tuttavia possibile eseguire il raggruppamento in base alle aggregazioni. Se l'argomento di colonna passato non è di tipo numerico o di data, viene restituito un errore di sintassi.

La parte dell'etichetta è facoltativa e fornisce un alias più leggibile per l'etichetta. Se non si include un'etichetta alias, Windows ricerca trasforma la funzione e il nome della colonna in un'etichetta. Ad esempio, MAX(System.Document. WordCount) diventa MAX \_ SystemDocumentWordCount.

## <a name="multi-level-groups-and-counting"></a>Gruppi e conteggi multi-livello

Le aggregazioni vengono definite su foglia e vengono duplicate. Un'aggregazione accetta come input le foglia del gruppo che lo definisce (documenti), anziché i sottogruppi dei relativi elementi figlio. Questa funzionalità è detta raggruppamento multi-livello.

Oltre a essere definite su foglia e duplicate, le aggregazioni vengono conteggiate una sola volta. Anche se lo stesso documento può essere rappresentato più volte in un gruppo, le aggregazioni lo considererebbe una sola volta. Il grafico seguente illustra questo concetto.

![diagramma che mostra che le aggregazioni sono definite su foglia e duplicate e vengono conteggiate una sola volta](images/aggregates.png)

## <a name="aggregate-examples"></a>Esempi di aggregazione

Di seguito sono riportati esempi di funzioni di aggregazione all'interno della clausola GROUP ON:


```
GROUP ON System.Sender ['d','m','r'] 
    AGGREGATE COUNT() as 'Total',
              MAX(System.Size) as 'Max Size',
              MIN(System.Size) as 'Min Size'
    OVER (SELECT System.Subject FROM systemindex)
              
GROUP ON System.Sender ['d', 'm', 'r']
      AGGREGATE MAX(System.Search.Rank) as 'MaxRank', 
                MIN(System.Search.Rank) as 'MinRank'
      OVER (GROUP ON system.conversationID
                  OVER (SELECT workid, System.ItemUrl FROM systemindex
                        WHERE CONTAINS (*, 'sometext')
                        ORDER BY System.DateCreated))
               
GROUP ON System.FileName [before('a'),before('z')] 
      AGGREGATE MAX(System.Size) as 'maxsize', MIN(System.Size) as 'MinSize' 
      OVER (SELECT System.FileName FROM systemindex
            ORDER BY System.FileName)      
            
GROUP ON System.author 
      AGGREGATE MAX(System.size) as 'maxsize' 
      ORDER BY min(System.Size) 
      OVER (GROUP ON System.DateCreated 
                  AGGREGATE Count() 
                  ORDER BY MAX(System.size) 
                  OVER (SELECT filename, System.DateCreated, System.Size FROM systemindex
                        WHERE CONTAINS('text')))
```



## <a name="return-value"></a>Valore restituito

Il valore restituito è una variante trovata nel set di righe come proprietà personalizzata, come alias specificati o come "Aggregates" se non viene specificata alcuna etichetta alias.

 

 



