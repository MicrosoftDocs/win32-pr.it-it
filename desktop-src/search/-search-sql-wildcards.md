---
description: Il predicato CONTAINs supporta l'utilizzo dell'asterisco ( \* ) come carattere jolly per rappresentare parole e frasi. È possibile aggiungere l'asterisco solo alla fine della parola o della frase. La presenza dell'asterisco Abilita la modalità di corrispondenza del prefisso.
ms.assetid: 9d141c7a-a721-416e-aa61-dabdb6533462
title: Utilizzo di caratteri jolly nel predicato CONTAINs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013e49f97cf23c7a00aca7bb287edd19951520f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128526"
---
# <a name="using-wildcard-characters-in-the-contains-predicate"></a>Utilizzo di caratteri jolly nel predicato CONTAINs

Il predicato CONTAINs supporta l'utilizzo dell'asterisco ( \* ) come carattere jolly per rappresentare parole e frasi. È possibile aggiungere l'asterisco solo alla fine della parola o della frase. La presenza dell'asterisco Abilita la modalità di corrispondenza del prefisso. In questa modalità vengono restituite corrispondenze se la colonna contiene la parola di ricerca specificata seguita da zero o più caratteri. Se viene specificata una frase, le corrispondenze vengono rilevate se la colonna contiene tutte le parole specificate con zero o più caratteri successivi alla parola finale.

## <a name="examples"></a>Esempio

Il primo esempio corrisponde ai documenti che contengono una parola nella colonna FileName che inizia con "serv". Le parole corrispondenti di esempio includono "Server", "Server" e "Service".


```
...WHERE CONTAINS(System.FileName, '"serv*"')
```



Il secondo esempio trova la corrispondenza dei documenti con qualsiasi frase nella colonna FileName che inizia con "comp" e in cui la parola successiva inizia con "serv". Le parole corrispondenti di esempio includono "comp server", "comp Servers" e "comp Service".


```
...WHERE CONTAINS(System.FileName, '"comp serv*"')
```



L'asterisco funziona solo per la corrispondenza dei prefissi e può essere inserito solo alla fine della parola o frase. non funziona per la corrispondenza dei suffissi. La sintassi seguente non è valida e non corrisponde ai documenti con alcuna parola nella colonna FileName che termina con "serve".


```
WHERE CONTAINS(System.FileName, '"*serve"')
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Predicato FREETEXT](-search-sql-freetext.md)
</dt> <dt>

[Clausola WHERE](-search-sql-where.md)
</dt> </dl>

 

 



