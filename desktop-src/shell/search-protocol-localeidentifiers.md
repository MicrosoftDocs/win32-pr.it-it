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
# <a name="locale-identifier-arguments-the-windows-shell"></a>Argomenti dell'identificatore delle impostazioni locali (shell di Windows)

Gli identificatori e consentono al motore di ricerca di usare i word breaker corretti identificando la lingua delle query immesse dall'utente e la lingua delle parole chiave `inputlocale` `keywordlocale` advanced query syntax. Questi non sono sempre gli stessi identificatori di codice lingua (CID) perché Windows Search è disponibile in diverse versioni internazionali e include anche i pacchetti interfaccia utente multilingue (MUI) per più lingue. identifica l'LCID per la lingua in cui gli utenti immettere la query di ricerca, mentre identifica l'LCID utilizzato dal motore di `inputlocale` ricerca per le parole `keywordlocale` chiave.

## <a name="example"></a>Esempio


```
search:query=matthew&inputlocale=2072&keywordlocale=1033
```



### <a name="argument-information"></a>Informazioni sugli argomenti



|                              | Valore                                   |
|------------------------------|-----------------------------------------|
| **Sistema operativo minimo** | Windows Vista con Service Pack 1 (SP1) |



 

 

 



