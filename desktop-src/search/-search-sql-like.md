---
description: Il predicato LIKE esegue il confronto dei criteri di ricerca sulla colonna specificata.
ms.assetid: d4bcf406-1253-4e56-b770-79edd4a98205
title: Predicato LIKE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba042fb2fe3005e062e7961a048a81a64c0c144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306124"
---
# <a name="like-predicate"></a>Predicato LIKE

Il predicato LIKE esegue il confronto dei criteri di ricerca sulla colonna specificata. Viene usata la sintassi seguente:


```
...WHERE <column> LIKE '<wildcard_literal>'
```



<column>Può essere un [identificatore](-search-sql-identifiers.md)regolare o delimitato. La colonna è limitata alle proprietà dell'archivio delle proprietà.

Il \_ valore letterale carattere jolly <> è un valore letterale stringa. È racchiuso tra virgolette e, facoltativamente, può contenere caratteri jolly. Se necessario, la stringa di corrispondenza può contenere più caratteri jolly. Nella tabella seguente vengono descritti i caratteri jolly riconosciuti dal predicato LIKE.



| Wildcard (Carattere jolly)                | Descrizione                                                                                                                                                                                     | Esempio                                                                                                                                                                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| % (percentuale)             | Trova la corrispondenza di zero o più caratteri.                                                                                                                                                         | "comp% r" corrisponde a "comp" seguito da zero o più caratteri, terminando con un r.                                                                                                                                  |
| \_ sottolineatura         | Individua un qualsiasi singolo carattere.                                                                                                                                                                   | "Comp \_ ter" corrisponde a "comp" seguito da un carattere qualsiasi, seguito da "ter".                                                                                                                              |
| \[\](parentesi quadre) | Corrisponde a qualsiasi carattere singolo compreso nell'intervallo o nel set specificato. Ad esempio, \[ a-z \] specifica un intervallo; \[ aeiou \] specifica il set di vocali.                                                  | "Comp \[ a-z \] re" corrisponde a "comp" seguito da un singolo carattere compreso tra a e z, seguito da' s'. "Comp \[ Ao \] " corrisponde a "comp" seguito da un singolo carattere che deve essere un oggetto o un o.<br/> |
| \[^ \] cursore          | Corrisponde a qualsiasi carattere singolo non compreso nell'intervallo o nel set specificato. Ad esempio, \[ ^ a-z \] specifica un intervallo che esclude dalla a alla z; \[ ^ aeiou \] specifica un set che esclude le vocali. | "Comp \[ ^ u \] " corrisponde a "comp" seguito da un singolo carattere diverso da u.                                                                                                                                        |



 

Se si creano predicati con più intervalli, è necessario che gli intervalli siano in ordine.

> [!Note]  
> Per trovare la corrispondenza con i caratteri jolly come caratteri letterali per la corrispondenza e non come caratteri jolly, inserire il carattere tra parentesi quadre. Ad esempio, per trovare la corrispondenza con il segno di percentuale, usare ' \[ % \] '

 

## <a name="examples"></a>Esempio


```
...WHERE System.ItemNameDisplay LIKE 'financ%'
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Confronto di valori letterali](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[Confronti multivalore (matrice)](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

[Predicato NULL](-search-sql-null.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Predicati full-text](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicati non full-text](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 




