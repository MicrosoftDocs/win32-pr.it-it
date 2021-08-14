---
description: È possibile specificare la lingua usata nelle query di ricerca.
ms.assetid: 3a7ecf8f-38ae-41d1-be70-e9ab23977a01
title: Specifica delle lingue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ab2b5b5c5da4e9f71e49330d966895415467a671289bd4f5607e1265d22a7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226816"
---
# <a name="specifying-languages"></a>Specifica delle lingue

È possibile specificare la lingua usata nelle query di ricerca. Entrambi i predicati FREETEXT e CONTAINS nella clausola WHERE supportano la specifica di una lingua. È possibile indicare il linguaggio di query fornendo un identificatore LCID (Numeric Language Code Identifier) nel predicato CONTAINS o FREETEXT. Questo LCID specifica quale word breaker usare per analizzare la stringa di query. Viene usata la sintassi seguente:


```
CONTAINS | FREETEXT
([<column_identifier>,]'<content_search_condition>' [,LCID]) 
```



Per altre informazioni, vedere la sintassi per i predicati [CONTAINS](-search-sql-contains.md) e [FREETEXT.](-search-sql-freetext.md)

 

 



