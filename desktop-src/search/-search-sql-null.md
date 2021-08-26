---
description: Il predicato NULL indica se il documento ha un valore per la colonna indicata.
ms.assetid: 078ffd99-2020-4da2-8968-301dba8cc436
title: Predicato NULL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bd80ea6cba2009b398c8cdd0a2926240e3ce78309ca3f8511fb6ba286f44a64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058121"
---
# <a name="null-predicate"></a>Predicato NULL

Il predicato **NULL** indica se il documento ha un valore per la colonna indicata.

Il predicato **NULL** ha la sintassi seguente:


```
...WHERE <column> IS [NOT] NULL
```



La parola chiave NOT facoltativa nega il risultato. La colonna può essere un identificatore regolare o [delimitato.](-search-sql-identifiers.md)

> [!IMPORTANT]
> Per verificare se una colonna ha il **valore NULL,** è necessario usare il **predicato NULL.** Non è valido usare il valore **NULL** in un predicato di confronto. "WHERE column IS **NULL"** è corretto. "WHERE column = **NULL**" non è valido.

 

## <a name="example"></a>Esempio

Nell'esempio seguente vengono restituiti documenti che non hanno un valore System.Video.Director.


```
...WHERE System.Video.Director IS NULL
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Predicato LIKE](-search-sql-like.md)
</dt> <dt>

[Confronto tra valori letterali](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[Confronti multivalore (ARRAY)](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Predicati full-text](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicati non full-text](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



