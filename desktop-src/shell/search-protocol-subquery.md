---
description: Informazioni sull'argomento SUBQUERY nella shell di Windows. Una sottoquery è un file di ricerca salvato che è possibile usare come filtro per una nuova query.
title: Argomento SUBQUERY (shell di Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2d97b891-ba62-4009-bc6a-9f42e6dbbb34
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ef0b37c0f473f2b86c85c18a99124be3b366f447
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010664"
---
# <a name="subquery-argument-the-windows-shell"></a>Argomento SUBQUERY (shell di Windows)

Una sottoquery è un file di ricerca salvato (con estensione search-ms) che è possibile usare come filtro \* per una nuova query. I risultati della sottoquery vengono usati come origine per la nuova query. Ad esempio, si supponga di avere diversi file di ricerca salvati che limitano una query in base alla lista di distribuzione di posta elettronica: mydepartment.search-ms, teamproject.search-ms e corporatewide.search-ms. L'uso `subquery` dell'argomento consente di limitare le ricerche di posta elettronica a una o a tutte queste ricerche salvate.

## <a name="example"></a>Esempio


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a>Informazioni sugli argomenti



|                          |                                         |
|--------------------------|-----------------------------------------|
| Sistema operativo minimo | Windows Vista con Service Pack 1 (SP1) |



 

 

 



