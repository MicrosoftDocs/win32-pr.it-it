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
# <a name="locale-identifier-arguments-windows-search"></a>Argomenti dell'identificatore delle impostazioni locali (Windows Search)

Gli identificatori e consentono al motore di ricerca di usare i word breaker corretti identificando la lingua delle query immesse dall'utente e la lingua delle parole chiave `inputlocale` `keywordlocale` advanced query syntax. Questi non sono sempre gli stessi identificatori di codice lingua (CID) perché Windows Search è disponibile in diverse versioni internazionali e include anche MUI Pack per più lingue. Inputlocale identifica l'identificatore LCID per la lingua in cui gli utenti immettere la query di ricerca, mentre la parola chiavelocale identifica l'LCID utilizzato dal motore di ricerca per le parole chiave.

Questo argomento è organizzato come segue:

-   [Esempio](#example)
-   [Argomenti correlati](#related-topics)

## <a name="example"></a>Esempio


```
 search-ms:query=matthew&inputlocale=2072&keywordlocale=1033
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività iniziali con Parameter-Value argomenti](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Argomento CRUMB](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[Argomento SYNTAX](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[Argomento STACKEDBY](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[Argomento SUBQUERY](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 



