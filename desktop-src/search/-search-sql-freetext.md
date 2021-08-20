---
description: Il predicato FREETEXT fa parte della clausola WHERE e supporta la ricerca di parole e frasi nelle colonne di testo.
ms.assetid: 8afc95d1-25cd-4448-8bee-d132c2da22b3
title: Predicato FREETEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f9fb3d65c1b9dc72ef74c8c6862ccfb778ebbd4149b9e5bf5aca4d36674045
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863407"
---
# <a name="freetext-predicate"></a>Predicato FREETEXT

Il predicato FREETEXT fa parte della [clausola WHERE](-search-sql-where.md) e supporta la ricerca di parole e frasi nelle colonne di testo. Usare il predicato FREETEXT per trovare i documenti contenenti combinazioni di parole di ricerca distribuite nel contenuto o nelle colonne specificate. Per ottenere il valore di classificazione, includere System.Search.Rank, ovvero una classificazione di relevence, come colonna nell'istruzione SELECT.

Il predicato FREETEXT ha la sintassi seguente:


```
FREETEXT
(["<fulltext_column>",]'<freetext_condition>'[,<LCID>])...
```



Il riferimento alla colonna full-text è facoltativo. È possibile specificare una singola colonna o un alias di [raggruppamento](-search-sql-with-as.md) di colonne in base al quale viene testato il predicato FREETEXT. Quando la colonna full-text viene specificata come "ALL" o "", viene cercata tutte le proprietà del testo \* indicizzato. Anche se la colonna non deve essere una proprietà di testo, i risultati potrebbero non avere significato se la colonna è un altro tipo di dati. Il nome della colonna può essere [](-search-sql-identifiers.md)un identificatore normale o delimitato ed è necessario separarlo dalla condizione con una virgola. Se non viene specificata alcuna condizione full-text, viene usata la colonna Contents, ovvero il corpo del documento.

È possibile specificare le impostazioni locali di ricerca per identificare il word breaker e i moduli gonfiali appropriati per la query di ricerca. I valori delle impostazioni locali validi sono Windows LCID (Standard Language Code Identifier). Ad esempio, 1033 è l'LCID per Stati Uniti-inglese. Inserire l'LCID come ultimo elemento all'interno delle parentesi della clausola FREETEXT. Per informazioni importanti sulla ricerca e sulle lingue, vedere [Uso delle ricerche localizzate.](-search-sql-usinglocsearches.md)

> [!Note]  
> Le impostazioni locali di ricerca predefinite sono le impostazioni locali predefinite del sistema.

 

È necessario racchiudere la parte relativa alla condizione freetext tra virgolette singole e deve essere costituita da uno o più termini di ricerca. Il predicato FREETEXT non supporta operazioni logiche. Per cercare una frase come se fosse una singola parola, racchiuderla tra virgolette doppie.

Quando si usa il predicato FREETEXT, i risultati della query di ricerca restituiscono documenti contenenti tutti i termini di ricerca. Non è necessario che i termini vengano visualizzati in un ordine specifico. I documenti che contengono più termini di ricerca hanno valori di colonna di rango più elevati.

## <a name="examples"></a>Esempio

Nell'esempio seguente vengono cercati documenti contenenti "computer", "software", "hardware" o combinazioni di queste parole:


```
WHERE FREETEXT('computer software hardware')
```



> [!Note]  
> Non è possibile usare sia la corrispondenza a parola singola che la corrispondenza di frasi nello stesso predicato FREETEXT.

 

Quando si eseguono query con contrazioni, è necessario usare l'escape delle virgolette nella contrazione quando si usa FREETEXT, ma non quando si usa CONTAINS.

Ad esempio, la sintassi seguente non riesce:


```
WHERE FREETEXT(*,'"We'll meet next week"')
```



La sintassi corretta include due virgolette singole, non le virgolette doppie.

La sintassi seguente ha esito positivo:


```
WHERE FREETEXT(*,'"We''ll meet next week"')
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Predicato CONTAINS](-search-sql-contains.md)
</dt> <dt>

[Clausola WHERE](-search-sql-where.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Predicati non full-text](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



