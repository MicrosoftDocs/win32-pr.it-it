---
description: Il protocollo di applicazione search-ms è una convenzione per l'esecuzione di query sull'indice di ricerca di Windows.
ms.assetid: ab2695ed-4ef3-4687-81b0-416ca7086e5f
title: Esecuzione di query sull'indice con il protocollo search-ms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0d835b6db1c9b05b97d5d075b62158069d89029
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750418"
---
# <a name="querying-the-index-with-the-search-ms-protocol"></a><span data-ttu-id="ec052-103">Esecuzione di query sull'indice con il protocollo search-ms</span><span class="sxs-lookup"><span data-stu-id="ec052-103">Querying the Index with the search-ms Protocol</span></span>

<span data-ttu-id="ec052-104">Il [protocollo di applicazione](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) **search-ms** è una convenzione per l'esecuzione di query sull'indice di ricerca di Windows.  </span><span class="sxs-lookup"><span data-stu-id="ec052-104">The **search-ms**  [application protocol](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) is a convention for querying the Windows Search index.</span></span> <span data-ttu-id="ec052-105">Il protocollo consente alle applicazioni, ad esempio Esplora risorse, di eseguire query sull'indice con argomenti di valore parametro, inclusi argomenti di proprietà, ricerche salvate in precedenza, sintassi di query avanzate (AQS), sintassi di query naturale (NQS) e identificatori del codice lingua (LCID) per l'indicizzatore e la query stessa.</span><span class="sxs-lookup"><span data-stu-id="ec052-105">The protocol enables applications, like Windows Explorer, to query the index with parameter-value arguments, including property arguments, previously saved searches, Advanced Query Syntax (AQS), Natural Query Syntax (NQS), and language code identifiers (LCIDs) for both the indexer and the query itself.</span></span>

<span data-ttu-id="ec052-106">Questa sezione è organizzata nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="ec052-106">This section is organized as follows:</span></span>

-   [<span data-ttu-id="ec052-107">Introduzione con argomenti di Parameter-Value</span><span class="sxs-lookup"><span data-stu-id="ec052-107">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
-   [<span data-ttu-id="ec052-108">Argomenti dell'identificatore delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="ec052-108">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
-   [<span data-ttu-id="ec052-109">Argomento BRICIOLo</span><span class="sxs-lookup"><span data-stu-id="ec052-109">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
-   [<span data-ttu-id="ec052-110">Argomento della sintassi</span><span class="sxs-lookup"><span data-stu-id="ec052-110">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
-   [<span data-ttu-id="ec052-111">Argomento STACKEDBY</span><span class="sxs-lookup"><span data-stu-id="ec052-111">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
-   [<span data-ttu-id="ec052-112">Argomento SOTTOQUERY</span><span class="sxs-lookup"><span data-stu-id="ec052-112">SUBQUERY Argument</span></span>](-search-3x-wds-qryidx-subquery.md)

## <a name="related-topics"></a><span data-ttu-id="ec052-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ec052-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec052-114">Esecuzione di query sull'indice a livello di codice</span><span class="sxs-lookup"><span data-stu-id="ec052-114">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="ec052-115">Utilizzo degli approcci SQL e AQS per eseguire una query sull'indice</span><span class="sxs-lookup"><span data-stu-id="ec052-115">Using SQL and AQS Approaches to Query the Index</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="ec052-116">Esecuzione di query sull'indice con ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="ec052-116">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[<span data-ttu-id="ec052-117">Esecuzione di query sull'indice con la sintassi SQL di ricerca di Windows</span><span class="sxs-lookup"><span data-stu-id="ec052-117">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
</dt> <dt>

[<span data-ttu-id="ec052-118">Uso della sintassi avanzata delle query a livello di codice</span><span class="sxs-lookup"><span data-stu-id="ec052-118">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)
</dt> </dl>

 

 
