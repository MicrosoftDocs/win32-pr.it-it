---
description: Una sottoquery è un file di ricerca salvato ( \* . search-ms) che può essere utilizzato come filtro per una nuova query.
title: Argomento SOTTOQUERY (shell di Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2d97b891-ba62-4009-bc6a-9f42e6dbbb34
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 43e4a5b904d5e769eb43acad05aa5d8ce37ebde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995037"
---
# <a name="subquery-argument-the-windows-shell"></a>Argomento SOTTOQUERY (shell di Windows)

Una sottoquery è un file di ricerca salvato ( \* . search-ms) che può essere utilizzato come filtro per una nuova query. I risultati della sottoquery vengono usati come origine per la nuova query. Si immagini, ad esempio, di avere diversi file di ricerca salvati che limitano una query tramite la lista di distribuzione di posta elettronica: reparto. search-ms, TeamProject. search-ms e corporatewide. search-ms. L'uso dell' `subquery` argomento consente di limitare la ricerca di messaggi di posta elettronica a una o a tutte le ricerche salvate.

## <a name="example"></a>Esempio


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a>Informazioni argomento



|                          |                                         |
|--------------------------|-----------------------------------------|
| Sistema operativo minimo | Windows Vista con Service Pack 1 (SP1) |



 

 

 



