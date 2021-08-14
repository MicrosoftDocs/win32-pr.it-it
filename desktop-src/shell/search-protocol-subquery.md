---
description: Informazioni sull'argomento SUBQUERY in Windows Shell. Una sottoquery è un file di ricerca salvato che è possibile usare come filtro per una nuova query.
title: Argomento SUBQUERY (shell Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2d97b891-ba62-4009-bc6a-9f42e6dbbb34
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: fc478c9aff21b20566ffcd8d10580abaf8affa8eb36c39adb8c3c75486ca999d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452867"
---
# <a name="subquery-argument-the-windows-shell"></a>Argomento SUBQUERY (shell Windows)

Una sottoquery è un file di ricerca salvato (con estensione search-ms) che è possibile usare come filtro \* per una nuova query. I risultati della sottoquery vengono utilizzati come origine per la nuova query. Si supponga, ad esempio, di avere diversi file di ricerca salvati che limitano una query in base alla lista di distribuzione di posta elettronica: mydepartment.search-ms, teamproject.search-ms e corporatewide.search-ms. L'uso `subquery` dell'argomento consente di limitare le ricerche tramite posta elettronica a una o a tutte queste ricerche salvate.

## <a name="example"></a>Esempio


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a>Informazioni sugli argomenti



|                              | Valore                                   |
|------------------------------|-----------------------------------------|
| **Sistema operativo minimo** | Windows Vista con Service Pack 1 (SP1) |



 

 

 



