---
description: Comprendere gli argomenti inputlocale e keywordlocale nell'interfaccia utente della shell di Windows, che consente al motore di ricerca di usare i word breaker corretti.
title: Argomenti dell'identificatore delle impostazioni locali (shell di Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 881ce3a6-6cf6-45be-9a1e-148b9053d7c4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 34eab39e7ed956bf68048d9ce5861c12eedbbe7a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403594"
---
# <a name="locale-identifier-arguments-the-windows-shell"></a><span data-ttu-id="cbc1c-103">Argomenti dell'identificatore delle impostazioni locali (shell di Windows)</span><span class="sxs-lookup"><span data-stu-id="cbc1c-103">Locale Identifier Arguments (The Windows Shell)</span></span>

<span data-ttu-id="cbc1c-104">Gli identificatori e consentono al motore di ricerca di usare i word breaker corretti identificando la lingua delle query immesse dall'utente e la lingua delle parole chiave `inputlocale` `keywordlocale` advanced query syntax.</span><span class="sxs-lookup"><span data-stu-id="cbc1c-104">The `inputlocale` and `keywordlocale` identifiers help the search engine use the correct word breakers by identifying the language of user-entered queries and the language the of Advanced Query Syntax keywords.</span></span> <span data-ttu-id="cbc1c-105">Questi non sono sempre gli stessi identificatori di codice lingua (CID) perché Windows Search è disponibile in diverse versioni internazionali e include anche i pacchetti interfaccia utente multilingue (MUI) per più lingue.</span><span class="sxs-lookup"><span data-stu-id="cbc1c-105">These are not always the same language code identifiers (LCIDs) because Windows Search is offered in a number of international versions and also includes Multilingual User Interface (MUI) packs for more languages.</span></span> <span data-ttu-id="cbc1c-106">identifica l'LCID per la lingua in cui gli utenti immettere la query di ricerca, mentre identifica l'LCID utilizzato dal motore di `inputlocale` ricerca per le parole `keywordlocale` chiave.</span><span class="sxs-lookup"><span data-stu-id="cbc1c-106">The `inputlocale` identifies the LCID for the language users input their search query in, while the `keywordlocale` identifies the LCID the search engine uses for keywords.</span></span>

## <a name="example"></a><span data-ttu-id="cbc1c-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="cbc1c-107">Example</span></span>


```
search:query=matthew&inputlocale=2072&keywordlocale=1033
```



### <a name="argument-information"></a><span data-ttu-id="cbc1c-108">Informazioni sugli argomenti</span><span class="sxs-lookup"><span data-stu-id="cbc1c-108">Argument Information</span></span>



|                              | <span data-ttu-id="cbc1c-109">Valore</span><span class="sxs-lookup"><span data-stu-id="cbc1c-109">Value</span></span>                                   |
|------------------------------|-----------------------------------------|
| <span data-ttu-id="cbc1c-110">**Sistema operativo minimo**</span><span class="sxs-lookup"><span data-stu-id="cbc1c-110">**Minimum Operating System**</span></span> | <span data-ttu-id="cbc1c-111">Windows Vista con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="cbc1c-111">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 



