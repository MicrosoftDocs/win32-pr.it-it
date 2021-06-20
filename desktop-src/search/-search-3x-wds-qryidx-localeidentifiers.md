---
description: Comprendere gli argomenti inputlocale e keywordlocale in Windows Search, che consente al motore di ricerca di usare i word breaker corretti.
ms.assetid: dc610f49-5106-47f9-b29b-84949dd2c42b
title: Argomenti dell'identificatore delle impostazioni locali (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe4c56e9c3fb5a84938d4779c7a3ebeb849b0787
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403754"
---
# <a name="locale-identifier-arguments-windows-search"></a><span data-ttu-id="fdee3-103">Argomenti dell'identificatore delle impostazioni locali (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="fdee3-103">Locale Identifier Arguments (Windows Search)</span></span>

<span data-ttu-id="fdee3-104">Gli identificatori e consentono al motore di ricerca di usare i word breaker corretti identificando la lingua delle query immesse dall'utente e la lingua delle parole chiave `inputlocale` `keywordlocale` advanced query syntax.</span><span class="sxs-lookup"><span data-stu-id="fdee3-104">The `inputlocale` and `keywordlocale` identifiers help the search engine use the correct word breakers by identifying the language of user-entered queries and the language the of Advanced Query Syntax keywords.</span></span> <span data-ttu-id="fdee3-105">Questi non sono sempre gli stessi identificatori di codice lingua (CID) perché Windows Search è disponibile in diverse versioni internazionali e include anche MUI Pack per più lingue.</span><span class="sxs-lookup"><span data-stu-id="fdee3-105">These are not always the same language code identifiers (LCIDs) because Windows Search is offered in a number of international versions and also includes MUI packs for more languages.</span></span> <span data-ttu-id="fdee3-106">Inputlocale identifica l'identificatore LCID per la lingua in cui gli utenti immettere la query di ricerca, mentre la parola chiavelocale identifica l'LCID utilizzato dal motore di ricerca per le parole chiave.</span><span class="sxs-lookup"><span data-stu-id="fdee3-106">The inputlocale identifies the LCID for the language users input their search query in, while the keywordlocale identifies the LCID the search engine uses for keywords.</span></span>

<span data-ttu-id="fdee3-107">Questo argomento è organizzato come segue:</span><span class="sxs-lookup"><span data-stu-id="fdee3-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="fdee3-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="fdee3-108">Example</span></span>](#example)
-   [<span data-ttu-id="fdee3-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fdee3-109">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="fdee3-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="fdee3-110">Example</span></span>


```
 search-ms:query=matthew&inputlocale=2072&keywordlocale=1033
```



## <a name="related-topics"></a><span data-ttu-id="fdee3-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fdee3-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdee3-112">Attività iniziali con Parameter-Value argomenti</span><span class="sxs-lookup"><span data-stu-id="fdee3-112">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="fdee3-113">Argomento CRUMB</span><span class="sxs-lookup"><span data-stu-id="fdee3-113">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[<span data-ttu-id="fdee3-114">Argomento SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fdee3-114">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="fdee3-115">Argomento STACKEDBY</span><span class="sxs-lookup"><span data-stu-id="fdee3-115">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[<span data-ttu-id="fdee3-116">Argomento SUBQUERY</span><span class="sxs-lookup"><span data-stu-id="fdee3-116">SUBQUERY Argument</span></span>](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 



