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
# <a name="subquery-argument-the-windows-shell"></a><span data-ttu-id="96dc5-103">Argomento SOTTOQUERY (shell di Windows)</span><span class="sxs-lookup"><span data-stu-id="96dc5-103">SUBQUERY Argument (The Windows Shell)</span></span>

<span data-ttu-id="96dc5-104">Una sottoquery è un file di ricerca salvato ( \* . search-ms) che può essere utilizzato come filtro per una nuova query.</span><span class="sxs-lookup"><span data-stu-id="96dc5-104">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="96dc5-105">I risultati della sottoquery vengono usati come origine per la nuova query.</span><span class="sxs-lookup"><span data-stu-id="96dc5-105">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="96dc5-106">Si immagini, ad esempio, di avere diversi file di ricerca salvati che limitano una query tramite la lista di distribuzione di posta elettronica: reparto. search-ms, TeamProject. search-ms e corporatewide. search-ms.</span><span class="sxs-lookup"><span data-stu-id="96dc5-106">For example, say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="96dc5-107">L'uso dell' `subquery` argomento consente di limitare la ricerca di messaggi di posta elettronica a una o a tutte le ricerche salvate.</span><span class="sxs-lookup"><span data-stu-id="96dc5-107">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

## <a name="example"></a><span data-ttu-id="96dc5-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="96dc5-108">Example</span></span>


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a><span data-ttu-id="96dc5-109">Informazioni argomento</span><span class="sxs-lookup"><span data-stu-id="96dc5-109">Argument Information</span></span>



|                          |                                         |
|--------------------------|-----------------------------------------|
| <span data-ttu-id="96dc5-110">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="96dc5-110">Minimum Operating System</span></span> | <span data-ttu-id="96dc5-111">Windows Vista con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="96dc5-111">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 



