---
description: Una funzione di aggregazione esegue un calcolo su un set di valori e restituisce un valore. In questo modo è possibile generare statistiche di riepilogo per i gruppi a più livelli con un sovraccarico ridotto.
ms.assetid: 82a93f57-8273-45bf-81d7-50a673845ae1
title: Funzioni di aggregazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da68ad1104c93e8ae04f7ec37cbbde5020109336
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104562917"
---
# <a name="aggregate-functions"></a>Funzioni di aggregazione

Una funzione di aggregazione esegue un calcolo su un set di valori e restituisce un valore. In questo modo è possibile generare statistiche di riepilogo per i gruppi a più livelli con un sovraccarico ridotto.

## <a name="about-aggregate-functions"></a>Informazioni sulle funzioni di aggregazione

Le funzioni di aggregazione in Windows Search Structured Query Language (SQL) hanno la sintassi seguente:


```
AGGREGATE <function> [AS <label>] [,<function> [AS <label>]]*
```



La parte della funzione può includere le funzioni e la sintassi seguenti:



| Funzione                                                              | Descrizione                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AVG ( <column> )                                                   | Restituisce la media dei valori in un gruppo. Si applica solo ai numeri.                                                                                                                                      |
| BYFREQUENCY ( <column> , <N> )                                | Restituisce i valori di colonna N più frequenti dai risultati nel gruppo. Include inoltre un conteggio del numero di volte in cui ogni valore si è verificato e degli identificatori del documento per i risultati che contengono ogni valore restituito. |
| CHILDCOUNT ()                                                          | Restituisce il numero di elementi in un gruppo (esclusi i sottogruppi). Se sono presenti più livelli di raggruppamento, restituisce il numero di gruppi figlio immediati.                                                  |
| CONTEGGIO ()                                                               | Restituisce il numero di elementi in un gruppo e in tutti i sottogruppi.                                                                                                                                                   |
| DATERANGE ( <column> )                                             | Restituisce i limiti inferiore e superiore dei valori di colonna trovati nel gruppo di risultati del gruppo. Valido solo per le proprietà FILETIME.                                                                               |
| PRIMO ( <column> , <N> )                                      | Restituisce i primi valori di colonna N dai risultati foglia trovati in un gruppo.                                                                                                                                       |
| MAX ( <column> )                                                   | Restituisce il valore massimo dell'espressione. Si applica solo a numeri o date.                                                                                                                              |
| MIN ( <column> )                                                   | Restituisce il valore minimo nell'espressione. Si applica solo a numeri o date.                                                                                                                              |
| REPRESENTATIVEOF ( <column> , <idRepresentative> , <N> ) | Restituisce N valori idRepresentative, ognuno selezionato da uno dei subset di risultati con un valore di colonna univoco. Ogni valore viene restituito anche con un identificatore del documento con il valore idRepresentative. |
| SUM ( <column> )                                                   | Restituisce la somma dei valori in un gruppo. Si applica solo ai numeri.                                                                                                                                          |



 

 

> [!Note]  
> Le aggregazioni vengono restituite come singole colonne. Sono principalmente tipi semplici, ad eccezione di ByFrequency, First, DateRange e RepresentativeOf, che vengono restituiti come tipi composti.

 

È possibile utilizzare qualsiasi colonna numerica o data per le aggregazioni e non solo quelle presenti nella clausola SELECT. Tuttavia, non è possibile raggruppare le aggregazioni. Se l'argomento della colonna passato non è un tipo numerico o di data, viene restituito un errore di sintassi.

La parte dell'etichetta è facoltativa e fornisce un alias più leggibile per l'etichetta. Se non si include un'etichetta alias, Windows Search trasforma il nome della funzione e della colonna in un'etichetta. Ad esempio, MAX (System.Document. WordCount) diventa il numero massimo di \_ SystemDocumentWordCount.

## <a name="multi-level-groups-and-counting"></a>Gruppi e conteggio a più livelli

Le aggregazioni sono definite sulle foglie e vengono duplicate. Un'aggregazione accetta come input le foglie del gruppo che lo definisce (Documents), anziché i sottogruppi dei relativi elementi figlio. Questa funzionalità viene definita raggruppamento a più livelli.

Oltre ad aggregazioni definite su foglie e duplicate, vengono conteggiate una sola volta. Sebbene lo stesso documento possa essere rappresentato più volte in un gruppo, le aggregazioni lo considerano una sola volta. Questo concetto è illustrato nell'immagine seguente.

![diagramma che mostra che le aggregazioni sono definite sulle foglie e duplicate e vengono conteggiate una sola volta](images/aggregates.png)

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

Il valore restituito è un VARIANT trovato nel set di righe come proprietà personalizzata, come alias specificati o come "aggregazioni" se non è specificata alcuna etichetta alias.

 

 



