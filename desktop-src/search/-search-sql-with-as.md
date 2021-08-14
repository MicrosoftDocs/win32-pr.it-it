---
description: Gli alias dei gruppi di colonne consentono di utilizzare nomi più brevi al posto del nome di una colonna o di un gruppo di colonne. Il predicato dell'alias di gruppo facoltativo fa parte della clausola WHERE.
ms.assetid: 7782ac24-ea6c-4a97-b1b6-982f276fcefc
title: WITH -- Predicato alias del gruppo AS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ed77072c83d1c28dcc3ec63396b46a21a57c4a97d9c6dcd70259bd861d19762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226734"
---
# <a name="with----as-group-alias-predicate"></a>WITH -- Predicato alias del gruppo AS

Gli alias dei gruppi di colonne consentono di utilizzare nomi più brevi al posto del nome di una colonna o di un gruppo di colonne. Il predicato dell'alias di gruppo facoltativo fa parte della clausola WHERE. La sintassi è la seguente:


```
...WHERE[ WITH(<columns>) AS #<alias_name>]
[,WITH(<columns>) AS #<alias_name>]
```



È possibile specificare più alias di gruppo, separando with... Predicati AS con virgole.

Quando si fa riferimento a un alias di gruppo in un predicato della clausola WHERE, la condizione viene applicata a ogni colonna del gruppo. I valori logici risultanti dalla corrispondenza di ogni colonna vengono combinati usando l'operatore **LOGICO OR.**

Un alias deve essere definito prima di poter essere usato e può essere usato solo all'interno della clausola WHERE. Il nome dell'alias deve essere un identificatore regolare preceduto da un simbolo di cancelletto ( \# ).

L'identificatore di colonna può contenere uno o più identificatori di colonna, separati da virgole. L'elenco di colonne deve essere racchiuso tra parentesi ed è possibile assegnare la ponderazione a ognuna. Ogni colonna ha la sintassi seguente:


```
<column_identifier> [<weight_assignment>]
```



Per informazioni sulla specifica dei pesi delle colonne, vedere [Predicato FREETEXT](-search-sql-freetext.md) e [Predicato CONTAINS.](-search-sql-contains.md)

L'identificatore di colonna può essere regolare o delimitato.

## <a name="examples"></a>Esempio

Gli esempi di clausola WHERE seguenti illustrano quando e come è possibile usare il predicato alias di gruppo. Nel primo esempio viene illustrata una clausola WHERE più ripetitiva che non usa l'aliasing di gruppo.


```
...WHERE
    FREETEXT("System.ItemNameDisplay",'"computer software"')
    OR
    FREETEXT("System.Title",'"computer software"')
    OR 
    FREETEXT("System.Keywords",'"computer software"')
```



L'esempio precedente può essere semplificato usando un alias di gruppo, come illustrato nell'esempio seguente.


```
...WHERE
    WITH("System.ItemNameDisplay","System.Title","System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



Di seguito è riportato un esempio di ponderazione positiva in cui alla **proprietà Title** viene assegnato un peso maggiore per determinare la classificazione relativa.


```
...WHERE
    WITH("System.Title":0.8,*:0.5,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



Di seguito è riportato un esempio di ponderazione negativa in cui la **proprietà Title** con peso 0 non viene considerata.


```
...WHERE
    WITH("System.Title":0,*:1.0,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Predicato FREETEXT](-search-sql-freetext.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Predicati full-text](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicati non full-text](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



