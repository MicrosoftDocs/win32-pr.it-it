---
description: Gli identificatori InputLocale e keywordlocale consentono al motore di ricerca di utilizzare i Word breaker corretti identificando la lingua delle query immesse dall'utente e la lingua delle parole chiave della sintassi di query avanzate.
title: Argomenti dell'identificatore delle impostazioni locali (shell di Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 881ce3a6-6cf6-45be-9a1e-148b9053d7c4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 403e0338b61a4dedba37a620000e3fd82c91f383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233565"
---
# <a name="locale-identifier-arguments-the-windows-shell"></a><span data-ttu-id="bc699-103">Argomenti dell'identificatore delle impostazioni locali (shell di Windows)</span><span class="sxs-lookup"><span data-stu-id="bc699-103">Locale Identifier Arguments (The Windows Shell)</span></span>

<span data-ttu-id="bc699-104">Gli `inputlocale` `keywordlocale` identificatori e consentono al motore di ricerca di utilizzare i Word breaker corretti identificando la lingua delle query immesse dall'utente e la lingua delle parole chiave della sintassi di query avanzate.</span><span class="sxs-lookup"><span data-stu-id="bc699-104">The `inputlocale` and `keywordlocale` identifiers help the search engine use the correct word breakers by identifying the language of user-entered queries and the language the of Advanced Query Syntax keywords.</span></span> <span data-ttu-id="bc699-105">Questi non sono sempre gli stessi identificatori di codice lingua (LCID) perché Windows Search è disponibile in diverse versioni internazionali e include anche MUI (Multilingual User Interface) Pack per altre lingue.</span><span class="sxs-lookup"><span data-stu-id="bc699-105">These are not always the same language code identifiers (LCIDs) because Windows Search is offered in a number of international versions and also includes Multilingual User Interface (MUI) packs for more languages.</span></span> <span data-ttu-id="bc699-106">`inputlocale`Identifica il LCID per il linguaggio in base al quale gli utenti immetteranno la query di ricerca, mentre `keywordlocale` identifica il LCID utilizzato dal motore di ricerca per le parole chiave.</span><span class="sxs-lookup"><span data-stu-id="bc699-106">The `inputlocale` identifies the LCID for the language users input their search query in, while the `keywordlocale` identifies the LCID the search engine uses for keywords.</span></span>

## <a name="example"></a><span data-ttu-id="bc699-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="bc699-107">Example</span></span>


```
search:query=matthew&inputlocale=2072&keywordlocale=1033
```



### <a name="argument-information"></a><span data-ttu-id="bc699-108">Informazioni argomento</span><span class="sxs-lookup"><span data-stu-id="bc699-108">Argument Information</span></span>



|                          |                                         |
|--------------------------|-----------------------------------------|
| <span data-ttu-id="bc699-109">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="bc699-109">Minimum Operating System</span></span> | <span data-ttu-id="bc699-110">Windows Vista con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="bc699-110">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 



