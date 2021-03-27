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
# <a name="locale-identifier-arguments-the-windows-shell"></a>Argomenti dell'identificatore delle impostazioni locali (shell di Windows)

Gli `inputlocale` `keywordlocale` identificatori e consentono al motore di ricerca di utilizzare i Word breaker corretti identificando la lingua delle query immesse dall'utente e la lingua delle parole chiave della sintassi di query avanzate. Questi non sono sempre gli stessi identificatori di codice lingua (LCID) perché Windows Search è disponibile in diverse versioni internazionali e include anche MUI (Multilingual User Interface) Pack per altre lingue. `inputlocale`Identifica il LCID per il linguaggio in base al quale gli utenti immetteranno la query di ricerca, mentre `keywordlocale` identifica il LCID utilizzato dal motore di ricerca per le parole chiave.

## <a name="example"></a>Esempio


```
search:query=matthew&inputlocale=2072&keywordlocale=1033
```



### <a name="argument-information"></a>Informazioni argomento



|                          |                                         |
|--------------------------|-----------------------------------------|
| Sistema operativo minimo | Windows Vista con Service Pack 1 (SP1) |



 

 

 



