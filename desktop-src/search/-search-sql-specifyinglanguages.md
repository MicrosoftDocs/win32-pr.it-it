---
description: È possibile specificare la lingua usata nelle query di ricerca.
ms.assetid: 3a7ecf8f-38ae-41d1-be70-e9ab23977a01
title: Specifica delle lingue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50b3f65a41670989d41e235831ec8c008a6d8cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525477"
---
# <a name="specifying-languages"></a>Specifica delle lingue

È possibile specificare la lingua usata nelle query di ricerca. Sia FREETEXT che CONTAINs predicati nella clausola WHERE supportano la specifica di una lingua. È possibile indicare il linguaggio di query fornendo un identificatore del codice lingua (LCID) numerico nel predicato CONTAINs o FREETEXT. Questo LCID specifica il Word breaker da usare per analizzare la stringa di query. Viene usata la sintassi seguente:


```
CONTAINS | FREETEXT
([<column_identifier>,]'<content_search_condition>' [,LCID]) 
```



Per ulteriori informazioni, vedere la sintassi per i predicati [Contains](-search-sql-contains.md) e [FREETEXT](-search-sql-freetext.md) .

 

 



