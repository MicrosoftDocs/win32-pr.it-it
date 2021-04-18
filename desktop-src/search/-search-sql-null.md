---
description: Il predicato NULL indica se il documento contiene un valore per la colonna indicata.
ms.assetid: 078ffd99-2020-4da2-8968-301dba8cc436
title: Predicato NULL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea02a04313ac2b86afe809633bee5ad2cbcf764e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306117"
---
# <a name="null-predicate"></a>Predicato NULL

Il predicato **null** indica se il documento contiene un valore per la colonna indicata.

Il predicato **null** presenta la sintassi seguente:


```
...WHERE <column> IS [NOT] NULL
```



La parola chiave NOT facoltativa nega il risultato. La colonna può essere un [identificatore](-search-sql-identifiers.md)regolare o delimitato.

> [!IMPORTANT]
> Per verificare se una colonna ha il valore **null** , è necessario utilizzare il predicato **null** . L'utilizzo del valore **null** in un predicato di confronto non è valido. "WHERE column IS **null**" è corretto. "WHERE Column = **null**" non è valido.

 

## <a name="example"></a>Esempio

Nell'esempio seguente vengono restituiti i documenti privi di un valore System. video. Director.


```
...WHERE System.Video.Director IS NULL
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Predicato LIKE](-search-sql-like.md)
</dt> <dt>

[Confronto di valori letterali](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[Confronti multivalore (matrice)](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Predicati full-text](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicati non full-text](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



