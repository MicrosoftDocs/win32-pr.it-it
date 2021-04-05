---
description: Gli alias dei gruppi di colonne consentono di utilizzare nomi più brevi al posto del nome di una colonna o di un gruppo di colonne. Il predicato alias del gruppo facoltativo fa parte della clausola WHERE.
ms.assetid: 7782ac24-ea6c-4a97-b1b6-982f276fcefc
title: CON il predicato alias gruppo AS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29218e11fbffe5f47128eeefba3a7fe847a5b21d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750367"
---
# <a name="with----as-group-alias-predicate"></a>CON il predicato alias gruppo AS

Gli alias dei gruppi di colonne consentono di utilizzare nomi più brevi al posto del nome di una colonna o di un gruppo di colonne. Il predicato alias del gruppo facoltativo fa parte della clausola WHERE. La sintassi è la seguente:


```
...WHERE[ WITH(<columns>) AS #<alias_name>]
[,WITH(<columns>) AS #<alias_name>]
```



È possibile specificare più di un alias di gruppo, separando con... COME predicati per virgole.

Quando si fa riferimento a un alias di gruppo in un predicato della clausola WHERE, la condizione viene applicata a ogni colonna del gruppo. I valori logici risultanti dalla corrispondenza di ogni colonna vengono combinati utilizzando l'operatore logico **or** .

È necessario definire un alias per poterlo utilizzare e utilizzarlo solo all'interno della clausola WHERE. Il nome dell'alias deve essere un identificatore regolare preceduto da un simbolo di cancelletto obbligatorio ( \# ).

L'identificatore di colonna può contenere uno o più identificatori di colonna separati da virgole. L'elenco di colonne deve essere racchiuso tra parentesi e la ponderazione può essere assegnata a ciascuna. Ogni colonna presenta la sintassi seguente:


```
<column_identifier> [<weight_assignment>]
```



Per informazioni su come specificare i pesi delle colonne, vedere [predicato FREETEXT](-search-sql-freetext.md) e [predicato CONTAINS](-search-sql-contains.md).

L'identificatore di colonna può essere regolare o delimitato.

## <a name="examples"></a>Esempio

Negli esempi di clausole WHERE seguenti viene illustrato quando e come è possibile utilizzare il predicato alias di gruppo. Nel primo esempio viene illustrata una clausola WHERE più ripetitiva che non utilizza l'aliasing del gruppo.


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



Di seguito è riportato un esempio di ponderazione positiva, in cui la proprietà **title** viene assegnata più peso alla determinazione della classificazione relativa.


```
...WHERE
    WITH("System.Title":0.8,*:0.5,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



Di seguito è riportato un esempio di ponderazione negativa in cui la proprietà **title** con peso 0 non viene considerata.


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

 

 



