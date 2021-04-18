---
description: Dopo la restituzione di un risultato da una query, è possibile accedere a diverse proprietà per il set di righe.
ms.assetid: 71aa0ad6-ef34-47ee-945f-04bda20bf8a4
title: Proprietà del set di righe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e498c701224a879c09653d6f265151297d2ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306113"
---
# <a name="rowset-properties"></a><span data-ttu-id="791ca-103">Proprietà del set di righe</span><span class="sxs-lookup"><span data-stu-id="791ca-103">Rowset Properties</span></span>

<span data-ttu-id="791ca-104">Dopo la restituzione di un risultato da una query, è possibile accedere a diverse proprietà per il set di righe.</span><span class="sxs-lookup"><span data-stu-id="791ca-104">After a result is returned from a query, you can access several properties for the rowset.</span></span>

<span data-ttu-id="791ca-105">Oltre alle proprietà standard del set di righe OLE-DB, Windows Search SQL offre le quattro proprietà personalizzate seguenti.</span><span class="sxs-lookup"><span data-stu-id="791ca-105">In addition to the standard OLE-DB rowset properties, Windows Search SQL offers the following four custom properties.</span></span> <span data-ttu-id="791ca-106">Il GUID per questo set di proprietà è {AA6EE6B0E828-11D0-B23E-00AA0047FC01}.</span><span class="sxs-lookup"><span data-stu-id="791ca-106">The GUID for this property set is {AA6EE6B0E828-11D0-B23E-00AA0047FC01}.</span></span>

<span data-ttu-id="791ca-107">Windows Search supporta la proprietà OLE-DB standard DBPROP \_ CommandTimeout del set di proprietà del set di [ \_ righe DBPROPSET](/previous-versions//ms691738(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="791ca-107">Windows Search supports the standard OLE-DB property DBPROP\_COMMANDTIMEOUT of the [DBPROPSET\_ROWSET](/previous-versions//ms691738(v=vs.85)) property set.</span></span>



| <span data-ttu-id="791ca-108">Nome proprietà</span><span class="sxs-lookup"><span data-stu-id="791ca-108">Property name</span></span>                  | <span data-ttu-id="791ca-109">PROPID/tipo</span><span class="sxs-lookup"><span data-stu-id="791ca-109">PROPID/type</span></span> | <span data-ttu-id="791ca-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="791ca-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="791ca-111">DONOTCOMPUTEEXPENSIVEPROPS</span><span class="sxs-lookup"><span data-stu-id="791ca-111">DONOTCOMPUTEEXPENSIVEPROPS</span></span>     | <span data-ttu-id="791ca-112">15/VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="791ca-112">15/VT\_BOOL</span></span> | <span data-ttu-id="791ca-113">Se si imposta questa proprietà su true, viene impedito il calcolo di proprietà dispendiose, ad esempio risultati trovati e numero massimo di dimensioni che richiedono la valutazione dell'intera query quando si accede a una</span><span class="sxs-lookup"><span data-stu-id="791ca-113">Setting this to true prevents computing expensive properties like Results Found and Max Rank that require evaluating the whole query when any rowset property is accessed.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="791ca-114">Rango massimo (MAX \_ Rank)</span><span class="sxs-lookup"><span data-stu-id="791ca-114">Maximum Rank (MAX\_RANK)</span></span>       | <span data-ttu-id="791ca-115">6/VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="791ca-115">6/VT\_I4</span></span>    | <span data-ttu-id="791ca-116">Rango più alto calcolato per tutti i risultati.</span><span class="sxs-lookup"><span data-stu-id="791ca-116">The highest rank computed for any result.</span></span>                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="791ca-117">Risultati trovati (risultati \_ trovati)</span><span class="sxs-lookup"><span data-stu-id="791ca-117">Results Found (RESULTS\_FOUND)</span></span> | <span data-ttu-id="791ca-118">7/VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="791ca-118">7/VT\_I4</span></span>    | <span data-ttu-id="791ca-119">Numero totale di elementi univoci per la query.</span><span class="sxs-lookup"><span data-stu-id="791ca-119">The total number of unique items for this query.</span></span> <span data-ttu-id="791ca-120">Per una query SELECT, questo è il numero di elementi nel set di righe.</span><span class="sxs-lookup"><span data-stu-id="791ca-120">For a SELECT query, this is the number of items in the rowset.</span></span> <span data-ttu-id="791ca-121">Per un gruppo in una query, questo è il numero di elementi foglia univoci.</span><span class="sxs-lookup"><span data-stu-id="791ca-121">For a GROUP ON query, this is the number of unique leaf items.</span></span> <span data-ttu-id="791ca-122">Questa proprietà non identifica il numero di righe nel set di righe di primo livello (il numero di gruppi di livello superiore).</span><span class="sxs-lookup"><span data-stu-id="791ca-122">This property does not identify the number of rows in the top-level rowset (the number of top-level groups).</span></span>                                                        |
| <span data-ttu-id="791ca-123">ID Where (WHEREID)</span><span class="sxs-lookup"><span data-stu-id="791ca-123">Where ID (WHEREID)</span></span>             | <span data-ttu-id="791ca-124">8/VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="791ca-124">8/VT\_I4</span></span>    | <span data-ttu-id="791ca-125">Identificatore per le restrizioni utilizzate per una query.</span><span class="sxs-lookup"><span data-stu-id="791ca-125">The identifier for the restrictions used for a query.</span></span> <span data-ttu-id="791ca-126">Se un set di righe è aperto quando viene eseguita una nuova query, la nuova query può riutilizzare le restrizioni della query precedente, sfruttando in tal modo il lavoro già completato.</span><span class="sxs-lookup"><span data-stu-id="791ca-126">If a rowset is open when a new query is executed, the new query can reuse the restrictions from the older query, thereby taking advantage of the work already completed.</span></span> <span data-ttu-id="791ca-127">Per ulteriori informazioni sul riutilizzo delle restrizioni WHERE, vedere la [funzione ReuseWhere](-search-sql-reusewhere.md).</span><span class="sxs-lookup"><span data-stu-id="791ca-127">For more information on reusing WHERE restrictions, refer to the [ReuseWhere function](-search-sql-reusewhere.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="791ca-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="791ca-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="791ca-129">Indicizzazione delle priorità e degli eventi del set di righe in Windows 7</span><span class="sxs-lookup"><span data-stu-id="791ca-129">Indexing Prioritization and Rowset Events in Windows 7</span></span>](indexing-prioritization-and-rowset-events.md)
</dt> </dl>

 

 
