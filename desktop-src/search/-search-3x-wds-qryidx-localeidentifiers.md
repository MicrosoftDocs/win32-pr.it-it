---
description: Gli identificatori InputLocale e keywordlocale consentono al motore di ricerca di utilizzare i Word breaker corretti identificando la lingua delle query immesse dall'utente e la lingua delle parole chiave della sintassi di query avanzate.
ms.assetid: dc610f49-5106-47f9-b29b-84949dd2c42b
title: Argomenti dell'identificatore delle impostazioni locali (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea1549a550e4bf6b8099241a6f3d2275860a983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878825"
---
# <a name="locale-identifier-arguments-windows-search"></a><span data-ttu-id="cabd6-103">Argomenti dell'identificatore delle impostazioni locali (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="cabd6-103">Locale Identifier Arguments (Windows Search)</span></span>

<span data-ttu-id="cabd6-104">Gli `inputlocale` `keywordlocale` identificatori e consentono al motore di ricerca di utilizzare i Word breaker corretti identificando la lingua delle query immesse dall'utente e la lingua delle parole chiave della sintassi di query avanzate.</span><span class="sxs-lookup"><span data-stu-id="cabd6-104">The `inputlocale` and `keywordlocale` identifiers help the search engine use the correct word breakers by identifying the language of user-entered queries and the language the of Advanced Query Syntax keywords.</span></span> <span data-ttu-id="cabd6-105">Questi non sono sempre gli stessi identificatori di codice lingua (LCID) perché Windows Search è disponibile in diverse versioni internazionali e include anche MUI Pack per altre lingue.</span><span class="sxs-lookup"><span data-stu-id="cabd6-105">These are not always the same language code identifiers (LCIDs) because Windows Search is offered in a number of international versions and also includes MUI packs for more languages.</span></span> <span data-ttu-id="cabd6-106">InputLocale identifica l'identificatore LCID per il linguaggio con cui gli utenti immetteranno la query di ricerca in, mentre keywordlocale identifica il LCID utilizzato dal motore di ricerca per le parole chiave.</span><span class="sxs-lookup"><span data-stu-id="cabd6-106">The inputlocale identifies the LCID for the language users input their search query in, while the keywordlocale identifies the LCID the search engine uses for keywords.</span></span>

<span data-ttu-id="cabd6-107">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="cabd6-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="cabd6-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="cabd6-108">Example</span></span>](#example)
-   [<span data-ttu-id="cabd6-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cabd6-109">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="cabd6-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="cabd6-110">Example</span></span>


```
 search-ms:query=matthew&inputlocale=2072&keywordlocale=1033
```



## <a name="related-topics"></a><span data-ttu-id="cabd6-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cabd6-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cabd6-112">Introduzione con argomenti di Parameter-Value</span><span class="sxs-lookup"><span data-stu-id="cabd6-112">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="cabd6-113">Argomento BRICIOLo</span><span class="sxs-lookup"><span data-stu-id="cabd6-113">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[<span data-ttu-id="cabd6-114">Argomento della sintassi</span><span class="sxs-lookup"><span data-stu-id="cabd6-114">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="cabd6-115">Argomento STACKEDBY</span><span class="sxs-lookup"><span data-stu-id="cabd6-115">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[<span data-ttu-id="cabd6-116">Argomento SOTTOQUERY</span><span class="sxs-lookup"><span data-stu-id="cabd6-116">SUBQUERY Argument</span></span>](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 



