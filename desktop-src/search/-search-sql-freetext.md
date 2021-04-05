---
description: Il predicato FREETEXT fa parte della clausola WHERE e supporta la ricerca di parole e frasi nelle colonne di testo.
ms.assetid: 8afc95d1-25cd-4448-8bee-d132c2da22b3
title: Predicato FREETEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc78be4d5ac75f892c82c6dad390e4583876856f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750386"
---
# <a name="freetext-predicate"></a>Predicato FREETEXT

Il predicato FREETEXT fa parte della clausola [where](-search-sql-where.md) e supporta la ricerca di parole e frasi nelle colonne di testo. Usare il predicato FREETEXT per trovare documenti contenenti combinazioni di parole di ricerca distribuite in tutto il contenuto o le colonne specificate. Per ottenere il valore di pertinenza, includere System. search. Rank, che è un rango di rilevanza, come colonna nell'istruzione SELECT.

Il predicato FREETEXT presenta la sintassi seguente:


```
FREETEXT
(["<fulltext_column>",]'<freetext_condition>'[,<LCID>])...
```



Il riferimento alla colonna full-text è facoltativo. Con esso, è possibile specificare una singola colonna o un [alias di raggruppamento di colonne](-search-sql-with-as.md) su cui viene testato il predicato FREETEXT. Quando la colonna full-text viene specificata come "ALL" o " \* ", viene eseguita la ricerca di tutte le proprietà di testo indicizzato. Sebbene non sia necessario che la colonna sia una proprietà di testo, i risultati potrebbero non essere significativi se la colonna è un altro tipo di dati. Il nome della colonna può essere un [identificatore](-search-sql-identifiers.md)regolare o delimitato ed è necessario separarlo dalla condizione con una virgola. Se non viene specificata alcuna condizione full-text, viene usata la colonna Contents, che è il corpo del documento.

È possibile specificare le impostazioni locali di ricerca per identificare il Word breaker e i moduli flessivi appropriati per la query di ricerca. I valori delle impostazioni locali validi sono un identificatore del codice lingua (LCID) di Windows standard. Ad esempio, 1033 è il LCID per Stati Uniti-English. Posizionare il LCID come ultimo elemento all'interno delle parentesi della clausola FREETEXT. Per informazioni importanti sulla ricerca e sui linguaggi, vedere [uso delle ricerche localizzate](-search-sql-usinglocsearches.md).

> [!Note]  
> Le impostazioni locali di ricerca predefinite sono le impostazioni locali predefinite del sistema.

 

È necessario racchiudere la parte della condizione FREETEXT tra virgolette singole e deve essere costituita da uno o più termini di ricerca. Il predicato FREETEXT non supporta le operazioni logiche. Per cercare una frase come se fosse una singola parola, racchiudere la frase tra virgolette doppie.

Quando si usa il predicato FREETEXT, i risultati della query di ricerca restituiscono documenti contenenti tutti i termini di ricerca. I termini non devono essere visualizzati in un ordine particolare. I documenti che contengono più termini di ricerca hanno valori di colonna di rango superiore.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene eseguita la ricerca di documenti contenenti "computer", "software", "hardware" o combinazioni di queste parole:


```
WHERE FREETEXT('computer software hardware')
```



> [!Note]  
> Non è possibile usare la corrispondenza con una sola parola e la corrispondenza di frasi nello stesso predicato FREETEXT.

 

Quando si eseguono query con contrazioni, è necessario utilizzare caratteri di escape per le virgolette durante la contrazione quando si utilizza FREETEXT, ma non quando si utilizza CONTAINs.

La sintassi seguente, ad esempio, ha esito negativo:


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

[CONTIENE predicato](-search-sql-contains.md)
</dt> <dt>

[Clausola WHERE](-search-sql-where.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Predicati non full-text](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



