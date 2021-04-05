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
# <a name="locale-identifier-arguments-windows-search"></a>Argomenti dell'identificatore delle impostazioni locali (Windows Search)

Gli `inputlocale` `keywordlocale` identificatori e consentono al motore di ricerca di utilizzare i Word breaker corretti identificando la lingua delle query immesse dall'utente e la lingua delle parole chiave della sintassi di query avanzate. Questi non sono sempre gli stessi identificatori di codice lingua (LCID) perché Windows Search è disponibile in diverse versioni internazionali e include anche MUI Pack per altre lingue. InputLocale identifica l'identificatore LCID per il linguaggio con cui gli utenti immetteranno la query di ricerca in, mentre keywordlocale identifica il LCID utilizzato dal motore di ricerca per le parole chiave.

Questo argomento è organizzato nel modo seguente:

-   [Esempio](#example)
-   [Argomenti correlati](#related-topics)

## <a name="example"></a>Esempio


```
 search-ms:query=matthew&inputlocale=2072&keywordlocale=1033
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione con argomenti di Parameter-Value](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Argomento BRICIOLo](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[Argomento della sintassi](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[Argomento STACKEDBY](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[Argomento SOTTOQUERY](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 



