---
description: 'Altre informazioni su: clausola ORDER BY'
ms.assetid: e720cf0d-b034-48e2-a13e-e97dd23b2beb
title: Clausola ORDER BY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eaa3c834ca2fe04222ef2ae452a0119bf391b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128535"
---
# <a name="order-by-clause"></a><span data-ttu-id="6f9e9-103">Clausola ORDER BY</span><span class="sxs-lookup"><span data-stu-id="6f9e9-103">ORDER BY Clause</span></span>

<span data-ttu-id="6f9e9-104">La clausola ORDER BY ordina i risultati in base al valore di una o più colonne specificate.</span><span class="sxs-lookup"><span data-stu-id="6f9e9-104">The ORDER BY clause sorts the results based on the value of one or more columns you specify.</span></span> <span data-ttu-id="6f9e9-105">Di seguito è riportata la sintassi della clausola ORDER BY:</span><span class="sxs-lookup"><span data-stu-id="6f9e9-105">Following is the syntax of the ORDER BY clause:</span></span>


```
ORDER BY <column> [<direction>] [,<column> [<direction>]]
```



<span data-ttu-id="6f9e9-106">L'identificatore di colonna deve essere una colonna valida.</span><span class="sxs-lookup"><span data-stu-id="6f9e9-106">The column specifier must be a valid column.</span></span> <span data-ttu-id="6f9e9-107">È possibile utilizzare l'identificatore di colonna per fare riferimento alle colonne in base all'ordine in cui sono visualizzate nella query.</span><span class="sxs-lookup"><span data-stu-id="6f9e9-107">You can use the column specifier to refer to columns by the order that they appear in the query.</span></span> <span data-ttu-id="6f9e9-108">La prima colonna della query è numerata 1.</span><span class="sxs-lookup"><span data-stu-id="6f9e9-108">The first column in the query is numbered 1.</span></span> <span data-ttu-id="6f9e9-109">È possibile includere più di una colonna nella clausola ORDER BY, separate da virgole.</span><span class="sxs-lookup"><span data-stu-id="6f9e9-109">You can include more than one column in the ORDER BY clause, separated by commas.</span></span>

<span data-ttu-id="6f9e9-110">L'identificatore di direzione facoltativo può essere "ASC" per l'ordine crescente (da basso a alto) o "DESC" per la decrescente (da alto a basso).</span><span class="sxs-lookup"><span data-stu-id="6f9e9-110">The optional direction specifier can be either "ASC" for ascending (low to high) or "DESC" for descending (high to low).</span></span> <span data-ttu-id="6f9e9-111">Se non si specifica un identificatore di direzione, viene usato il valore predefinito Ascending.</span><span class="sxs-lookup"><span data-stu-id="6f9e9-111">If you do not provide a direction specifier, the default, ascending, is used.</span></span> <span data-ttu-id="6f9e9-112">Se si specifica più di una colonna, ma non si specificano tutte le direzioni, la direzione specificata per ultima viene applicata a ogni colonna fino a quando non si modifica in modo esplicito la direzione.</span><span class="sxs-lookup"><span data-stu-id="6f9e9-112">If you specify more than one column, but do not specify all directions, the direction you specify last is applied to each column until you explicitly change the direction.</span></span>

<span data-ttu-id="6f9e9-113">Nella clausola ORDER BY seguente, ad esempio, le colonne A, B, C e G vengono ordinate in ordine crescente, mentre le colonne D, E e F sono ordinate in ordine decrescente.</span><span class="sxs-lookup"><span data-stu-id="6f9e9-113">For example, in the following ORDER BY clause, the columns A, B, C, and G are sorted in ascending order, while columns D, E, and F are sorted in descending order.</span></span>


```
ORDER BY A ASC, B, C, D DESC, E, F, G ASC
```



## <a name="related-topics"></a><span data-ttu-id="6f9e9-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6f9e9-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6f9e9-115">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="6f9e9-115">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6f9e9-116">Clausola FROM</span><span class="sxs-lookup"><span data-stu-id="6f9e9-116">FROM Clause</span></span>](-search-sql-from.md)
</dt> <dt>

[<span data-ttu-id="6f9e9-117">RANGO per clausola</span><span class="sxs-lookup"><span data-stu-id="6f9e9-117">RANK BY Clause</span></span>](-search-sql-rankby.md)
</dt> <dt>

[<span data-ttu-id="6f9e9-118">SELECT (istruzione)</span><span class="sxs-lookup"><span data-stu-id="6f9e9-118">SELECT Statement</span></span>](-search-sql-select.md)
</dt> <dt>

<span data-ttu-id="6f9e9-119">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="6f9e9-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6f9e9-120">Predicati full-text</span><span class="sxs-lookup"><span data-stu-id="6f9e9-120">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="6f9e9-121">Predicati non full-text</span><span class="sxs-lookup"><span data-stu-id="6f9e9-121">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



