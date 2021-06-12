---
description: Informazioni sull'argomento SUBQUERY in Windows Search. Una sottoquery è un file di ricerca salvato che è possibile usare come filtro per una nuova query.
ms.assetid: a92c774f-310b-4c40-be1c-0c2b0cac907b
title: Argomento SUBQUERY (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b23028d0bddcc674714f51f8b31883052431bd
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011034"
---
# <a name="subquery-argument-windows-search"></a><span data-ttu-id="31fb2-104">Argomento SUBQUERY (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="31fb2-104">SUBQUERY Argument (Windows Search)</span></span>

<span data-ttu-id="31fb2-105">Una sottoquery è un file di ricerca salvato (con estensione search-ms) che è possibile usare come filtro \* per una nuova query.</span><span class="sxs-lookup"><span data-stu-id="31fb2-105">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="31fb2-106">I risultati della sottoquery vengono usati come origine per la nuova query.</span><span class="sxs-lookup"><span data-stu-id="31fb2-106">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="31fb2-107">Si supponga, ad esempio, di avere diversi file di ricerca salvati che limitano una query in base alla lista di distribuzione di posta elettronica: mydepartment.search-ms, teamproject.search-ms e corporatewide.search-ms.</span><span class="sxs-lookup"><span data-stu-id="31fb2-107">For example, let's say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="31fb2-108">L'uso `subquery` dell'argomento consente di limitare le ricerche di posta elettronica a una o a tutte queste ricerche salvate.</span><span class="sxs-lookup"><span data-stu-id="31fb2-108">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

<span data-ttu-id="31fb2-109">Questo argomento è organizzato come segue:</span><span class="sxs-lookup"><span data-stu-id="31fb2-109">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="31fb2-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="31fb2-110">Example</span></span>](#example)
-   [<span data-ttu-id="31fb2-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="31fb2-111">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="31fb2-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="31fb2-112">Example</span></span>


```
 search-ms:query=vacation&subquery=mydepartment.search-ms
```



## <a name="related-topics"></a><span data-ttu-id="31fb2-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="31fb2-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31fb2-114">Attività iniziali con Parameter-Value argomenti</span><span class="sxs-lookup"><span data-stu-id="31fb2-114">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="31fb2-115">Argomenti dell'identificatore delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="31fb2-115">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[<span data-ttu-id="31fb2-116">Argomento CRUMB</span><span class="sxs-lookup"><span data-stu-id="31fb2-116">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[<span data-ttu-id="31fb2-117">Argomento SYNTAX</span><span class="sxs-lookup"><span data-stu-id="31fb2-117">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="31fb2-118">Argomento STACKEDBY</span><span class="sxs-lookup"><span data-stu-id="31fb2-118">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> </dl>

 

 



