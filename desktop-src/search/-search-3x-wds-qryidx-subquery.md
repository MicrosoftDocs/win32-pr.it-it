---
description: Una sottoquery è un file di ricerca salvato ( \* . search-ms) che può essere utilizzato come filtro per una nuova query.
ms.assetid: a92c774f-310b-4c40-be1c-0c2b0cac907b
title: Argomento SOTTOQUERY (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f673cf9c2a9867593fd6c8fdac83b5901f531257
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966537"
---
# <a name="subquery-argument-windows-search"></a><span data-ttu-id="3099a-103">Argomento SOTTOQUERY (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="3099a-103">SUBQUERY Argument (Windows Search)</span></span>

<span data-ttu-id="3099a-104">Una sottoquery è un file di ricerca salvato ( \* . search-ms) che può essere utilizzato come filtro per una nuova query.</span><span class="sxs-lookup"><span data-stu-id="3099a-104">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="3099a-105">I risultati della sottoquery vengono usati come origine per la nuova query.</span><span class="sxs-lookup"><span data-stu-id="3099a-105">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="3099a-106">Si immagini, ad esempio, di avere diversi file di ricerca salvati che limitano una query tramite la lista di distribuzione di posta elettronica: reparto. search-ms, TeamProject. search-ms e corporatewide. search-ms.</span><span class="sxs-lookup"><span data-stu-id="3099a-106">For example, let's say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="3099a-107">L'uso dell' `subquery` argomento consente di limitare la ricerca di messaggi di posta elettronica a una o a tutte le ricerche salvate.</span><span class="sxs-lookup"><span data-stu-id="3099a-107">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

<span data-ttu-id="3099a-108">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="3099a-108">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="3099a-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="3099a-109">Example</span></span>](#example)
-   [<span data-ttu-id="3099a-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3099a-110">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="3099a-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="3099a-111">Example</span></span>


```
 search-ms:query=vacation&subquery=mydepartment.search-ms
```



## <a name="related-topics"></a><span data-ttu-id="3099a-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3099a-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3099a-113">Introduzione con argomenti di Parameter-Value</span><span class="sxs-lookup"><span data-stu-id="3099a-113">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="3099a-114">Argomenti dell'identificatore delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="3099a-114">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[<span data-ttu-id="3099a-115">Argomento BRICIOLo</span><span class="sxs-lookup"><span data-stu-id="3099a-115">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[<span data-ttu-id="3099a-116">Argomento della sintassi</span><span class="sxs-lookup"><span data-stu-id="3099a-116">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="3099a-117">Argomento STACKEDBY</span><span class="sxs-lookup"><span data-stu-id="3099a-117">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> </dl>

 

 



