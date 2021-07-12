---
description: Informazioni sull'argomento SUBQUERY in Windows Shell. Una sottoquery è un file di ricerca salvato che è possibile usare come filtro per una nuova query.
title: Argomento SUBQUERY (Windows Shell)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2d97b891-ba62-4009-bc6a-9f42e6dbbb34
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c27ce11d4d2e6ac36792f3ce47c053e9646d9903
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581599"
---
# <a name="subquery-argument-the-windows-shell"></a>Argomento SUBQUERY (Windows Shell)

Una sottoquery è un file di ricerca salvato (con estensione search-ms) che è possibile usare come filtro \* per una nuova query. I risultati della sottoquery vengono usati come origine per la nuova query. Ad esempio, si supponga di avere diversi file di ricerca salvati che limitano una query in base alla lista di distribuzione di posta elettronica: mydepartment.search-ms, teamproject.search-ms e corporatewide.search-ms. L'uso `subquery` dell'argomento consente di limitare le ricerche di posta elettronica a una o a tutte queste ricerche salvate.

## <a name="example"></a>Esempio


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a>Informazioni sugli argomenti



|                              | Valore                                   |
|------------------------------|-----------------------------------------|
| **Sistema operativo minimo** | Windows Vista con Service Pack 1 (SP1) |



 

 

 



