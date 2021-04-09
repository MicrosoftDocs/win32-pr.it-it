---
description: In un database relazionale è necessario che le righe restituite da una query di ricerca soddisfino tutte le condizioni richiamate dalla query. Una query di ricerca di Windows, invece, può restituire i documenti che soddisfano le condizioni di ricerca a vari gradi.
ms.assetid: 9f37b494-9b7a-45a6-9ee4-6d582742cbd7
title: Informazioni sui valori di pertinenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a24c71ad523ad869c6ff05b81ff75367031ad38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878794"
---
# <a name="understanding-relevance-values"></a><span data-ttu-id="1544c-104">Informazioni sui valori di pertinenza</span><span class="sxs-lookup"><span data-stu-id="1544c-104">Understanding Relevance Values</span></span>

<span data-ttu-id="1544c-105">In un database relazionale è necessario che le righe restituite da una query di ricerca soddisfino tutte le condizioni richiamate dalla query.</span><span class="sxs-lookup"><span data-stu-id="1544c-105">In a relational database, rows that are returned by a search query must meet all the conditions called for by the query.</span></span> <span data-ttu-id="1544c-106">Una query di ricerca di Windows, invece, può restituire i documenti che soddisfano le condizioni di ricerca a vari gradi.</span><span class="sxs-lookup"><span data-stu-id="1544c-106">In contrast, a Windows Search query can return documents that meet the search conditions to varying degrees.</span></span>

<span data-ttu-id="1544c-107">Ad esempio, una ricerca del termine "programma" in un database relazionale produce record che contengono tale ortografia specifica della parola.</span><span class="sxs-lookup"><span data-stu-id="1544c-107">For example, a search for the term "program" in a relational database produces records that contain that specific spelling of the word.</span></span> <span data-ttu-id="1544c-108">Se un record contiene una o 100 istanze della parola non ha alcun effetto sui risultati.</span><span class="sxs-lookup"><span data-stu-id="1544c-108">Whether a record contains one or one hundred instances of the word has no impact on the results.</span></span> <span data-ttu-id="1544c-109">Al contrario, la ricerca di Windows restituisce un valore di pertinenza associato ai documenti corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="1544c-109">In contrast, Windows Search returns a relevance value associated with the matching documents.</span></span> <span data-ttu-id="1544c-110">La pertinenza dei documenti con "Program" nel titolo è superiore a quella che contengono la parola solo nell'ultimo paragrafo.</span><span class="sxs-lookup"><span data-stu-id="1544c-110">The relevance of documents having "program" in the title is higher than those that contain the word only in the last paragraph.</span></span> <span data-ttu-id="1544c-111">Analogamente, anche i documenti contenenti varianti del termine di ricerca, ad esempio "programmi" e "programmazione", corrispondono e vengono restituiti dalla query.</span><span class="sxs-lookup"><span data-stu-id="1544c-111">Similarly, documents containing variations of the search term, for example "programs" and "programming" also match and are returned by the query.</span></span>

<span data-ttu-id="1544c-112">Le query di ricerca di Windows restituiscono valori di pertinenza Integer nella colonna denominata "Rank".</span><span class="sxs-lookup"><span data-stu-id="1544c-112">Windows Search queries return integer relevance values in the column named "rank".</span></span>

<span data-ttu-id="1544c-113">Inoltre:</span><span class="sxs-lookup"><span data-stu-id="1544c-113">In addition:</span></span>

-   <span data-ttu-id="1544c-114">I valori di pertinenza restituiti dalla query sono numeri interi compresi tra 0 e 1000.</span><span class="sxs-lookup"><span data-stu-id="1544c-114">Rank values returned by the query are integers ranging from 0 to 1000.</span></span>
-   <span data-ttu-id="1544c-115">I valori di rango superiore indicano i documenti che soddisfano meglio le condizioni di ricerca.</span><span class="sxs-lookup"><span data-stu-id="1544c-115">Higher rank values indicate documents that better match the search conditions.</span></span>
-   <span data-ttu-id="1544c-116">I valori di pertinenza si applicano solo alla query corrente, quindi non possono essere confrontati per i risultati nelle query.</span><span class="sxs-lookup"><span data-stu-id="1544c-116">Rank values apply only to the current query, so they cannot be compared for results across queries.</span></span>
-   <span data-ttu-id="1544c-117">I valori di pertinenza sono relativi agli altri documenti corrispondenti alla query.</span><span class="sxs-lookup"><span data-stu-id="1544c-117">Rank values are relative to the other documents matching the query.</span></span> <span data-ttu-id="1544c-118">Pertanto, il valore di pertinenza di un determinato documento dipende dagli altri documenti che corrispondono anche alla query.</span><span class="sxs-lookup"><span data-stu-id="1544c-118">Therefore, the rank value of a particular document depends on the other documents that also match the query.</span></span>
-   <span data-ttu-id="1544c-119">I valori di pertinenza per gli elementi che corrispondono a un predicato puramente relazionale sono 1000.</span><span class="sxs-lookup"><span data-stu-id="1544c-119">Rank values for items matching a purely relational predicate are 1000.</span></span>

<span data-ttu-id="1544c-120">È possibile modificare i valori di rango restituiti usando i pesi delle colonne nei predicati [Contains](-search-sql-contains.md) e [FREETEXT](-search-sql-freetext.md) where e la clausola Rank by.</span><span class="sxs-lookup"><span data-stu-id="1544c-120">You can manipulate the returned rank values by using column weights in the [CONTAINS](-search-sql-contains.md) and [FREETEXT](-search-sql-freetext.md) WHERE clause predicates, and the RANK BY clause.</span></span>

 

 



