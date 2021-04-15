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
# <a name="specifying-languages"></a><span data-ttu-id="62e3b-103">Specifica delle lingue</span><span class="sxs-lookup"><span data-stu-id="62e3b-103">Specifying Languages</span></span>

<span data-ttu-id="62e3b-104">È possibile specificare la lingua usata nelle query di ricerca.</span><span class="sxs-lookup"><span data-stu-id="62e3b-104">You can specify the language used in search queries.</span></span> <span data-ttu-id="62e3b-105">Sia FREETEXT che CONTAINs predicati nella clausola WHERE supportano la specifica di una lingua.</span><span class="sxs-lookup"><span data-stu-id="62e3b-105">Both the FREETEXT and CONTAINS predicates in the WHERE clause support specifying a language.</span></span> <span data-ttu-id="62e3b-106">È possibile indicare il linguaggio di query fornendo un identificatore del codice lingua (LCID) numerico nel predicato CONTAINs o FREETEXT.</span><span class="sxs-lookup"><span data-stu-id="62e3b-106">You can indicate the query language by providing a numeric language code identifier (LCID) in the CONTAINS or FREETEXT predicate.</span></span> <span data-ttu-id="62e3b-107">Questo LCID specifica il Word breaker da usare per analizzare la stringa di query.</span><span class="sxs-lookup"><span data-stu-id="62e3b-107">This LCID specifies which word breaker to use to parse the query string.</span></span> <span data-ttu-id="62e3b-108">Viene usata la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="62e3b-108">It uses the following syntax:</span></span>


```
CONTAINS | FREETEXT
([<column_identifier>,]'<content_search_condition>' [,LCID]) 
```



<span data-ttu-id="62e3b-109">Per ulteriori informazioni, vedere la sintassi per i predicati [Contains](-search-sql-contains.md) e [FREETEXT](-search-sql-freetext.md) .</span><span class="sxs-lookup"><span data-stu-id="62e3b-109">For more information, see the syntax for the [CONTAINS](-search-sql-contains.md) and [FREETEXT](-search-sql-freetext.md) predicates.</span></span>

 

 



