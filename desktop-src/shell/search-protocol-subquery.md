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
# <a name="subquery-argument-the-windows-shell"></a><span data-ttu-id="2c634-104">Argomento SUBQUERY (Windows Shell)</span><span class="sxs-lookup"><span data-stu-id="2c634-104">SUBQUERY Argument (The Windows Shell)</span></span>

<span data-ttu-id="2c634-105">Una sottoquery è un file di ricerca salvato (con estensione search-ms) che è possibile usare come filtro \* per una nuova query.</span><span class="sxs-lookup"><span data-stu-id="2c634-105">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="2c634-106">I risultati della sottoquery vengono usati come origine per la nuova query.</span><span class="sxs-lookup"><span data-stu-id="2c634-106">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="2c634-107">Ad esempio, si supponga di avere diversi file di ricerca salvati che limitano una query in base alla lista di distribuzione di posta elettronica: mydepartment.search-ms, teamproject.search-ms e corporatewide.search-ms.</span><span class="sxs-lookup"><span data-stu-id="2c634-107">For example, say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="2c634-108">L'uso `subquery` dell'argomento consente di limitare le ricerche di posta elettronica a una o a tutte queste ricerche salvate.</span><span class="sxs-lookup"><span data-stu-id="2c634-108">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

## <a name="example"></a><span data-ttu-id="2c634-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="2c634-109">Example</span></span>


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a><span data-ttu-id="2c634-110">Informazioni sugli argomenti</span><span class="sxs-lookup"><span data-stu-id="2c634-110">Argument Information</span></span>



|                              | <span data-ttu-id="2c634-111">Valore</span><span class="sxs-lookup"><span data-stu-id="2c634-111">Value</span></span>                                   |
|------------------------------|-----------------------------------------|
| <span data-ttu-id="2c634-112">**Sistema operativo minimo**</span><span class="sxs-lookup"><span data-stu-id="2c634-112">**Minimum Operating System**</span></span> | <span data-ttu-id="2c634-113">Windows Vista con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="2c634-113">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 



