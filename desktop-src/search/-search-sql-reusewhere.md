---
description: La clausola WHERE in una query specifica un set di elementi in base ai quali confrontare i risultati.
ms.assetid: ed51edd5-6edc-4fcd-a69b-cb48c399ba7c
title: ReuseWhere (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16bb5af4c3acd4637b27a2b3c9c7e14436eabb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306114"
---
# <a name="reusewhere-function"></a><span data-ttu-id="ea31f-103">ReuseWhere (funzione)</span><span class="sxs-lookup"><span data-stu-id="ea31f-103">ReuseWhere Function</span></span>

<span data-ttu-id="ea31f-104">La clausola WHERE in una query specifica un set di elementi in base ai [quali](-search-sql-where.md) confrontare i risultati.</span><span class="sxs-lookup"><span data-stu-id="ea31f-104">The [WHERE](-search-sql-where.md) clause in a query specifies a set of items to match results against.</span></span> <span data-ttu-id="ea31f-105">Le query successive possono condividere il lavoro eseguito per una query precedente utilizzando la funzione ReuseWhere in una nuova clausola WHERE della query.</span><span class="sxs-lookup"><span data-stu-id="ea31f-105">Subsequent queries can share the work performed for a previous query by using the ReuseWhere function in a new query WHERE clause.</span></span> <span data-ttu-id="ea31f-106">Le query che sfruttano i vantaggi di questa funzione vengono eseguite più velocemente.</span><span class="sxs-lookup"><span data-stu-id="ea31f-106">Queries that take advantage of this function execute faster.</span></span>

## <a name="examples"></a><span data-ttu-id="ea31f-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="ea31f-107">Examples</span></span>

<span data-ttu-id="ea31f-108">Nello scenario seguente viene illustrato come utilizzare la funzione ReuseWhere:</span><span class="sxs-lookup"><span data-stu-id="ea31f-108">The following scenario shows how to use the ReuseWhere function:</span></span>

1.  <span data-ttu-id="ea31f-109">Eseguire la query seguente:</span><span class="sxs-lookup"><span data-stu-id="ea31f-109">You issue the following query:</span></span>
    ```
    SELECT System.ItemName FROM SystemIndex 
    WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5'
    ```

    

2.  <span data-ttu-id="ea31f-110">Dal set di righe restituito si ottiene un [ID where](-search-sql-rowset-properties.md), *Query1WhereID*.</span><span class="sxs-lookup"><span data-stu-id="ea31f-110">From the returned rowset, you get a [Where ID](-search-sql-rowset-properties.md), *Query1WhereID*.</span></span>

    <span data-ttu-id="ea31f-111">Il dove ID è una proprietà del set di righe con propset {aa6ee6b0-e828-11D0-B2-3e-00-AA-00-47-FC-01}, PROPID 8 e il tipo UI4.</span><span class="sxs-lookup"><span data-stu-id="ea31f-111">The Where ID is a rowset property with PROPSET {aa6ee6b0-e828-11d0-b2-3e-00-aa-00-47-fc-01 }, PROPID 8, and type UI4.</span></span>

3.  <span data-ttu-id="ea31f-112">Viene eseguita una seconda query con la funzione ReuseWhere, passando il *Query1WhereID* dal passaggio 2:</span><span class="sxs-lookup"><span data-stu-id="ea31f-112">You issue a second query with the ReuseWhere function, passing in the *Query1WhereID* from step 2:</span></span>
    ```
    SELECT System.ItemUrl FROM SystemIndex 
    WHERE ReuseWhere(Query1WhereID) AND SCOPE='file:'
    ```

    

<span data-ttu-id="ea31f-113">La seconda query è equivalente alla seguente:</span><span class="sxs-lookup"><span data-stu-id="ea31f-113">The second query is equivalent to the following:</span></span>


```
SELECT System.ItemUrl, System.ItemName FROM SystemIndex 
WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5' AND Scope='file:'
```



<span data-ttu-id="ea31f-114">La funzione ReuseWhere può essere utilizzata nella clausola [where](-search-sql-where.md) .</span><span class="sxs-lookup"><span data-stu-id="ea31f-114">The ReuseWhere function can be used anwhere in the [WHERE](-search-sql-where.md) clause.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea31f-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ea31f-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ea31f-116">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="ea31f-116">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ea31f-117">Clausola WHERE</span><span class="sxs-lookup"><span data-stu-id="ea31f-117">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

[<span data-ttu-id="ea31f-118">Proprietà del set di righe</span><span class="sxs-lookup"><span data-stu-id="ea31f-118">Rowset Properties</span></span>](-search-sql-rowset-properties.md)
</dt> </dl>

 

 



