---
description: Il termine FORMSOF esegue le corrispondenze usando altre forme linguistiche della parola.
ms.assetid: b705b8bc-dc2c-4cee-8306-f494b0f96cbf
title: Termine FORMSOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1ffcbd832833a506db99236bf26921a4b0145ffe5bfccaed8fff59103370291
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863444"
---
# <a name="formsof-term"></a>Termine FORMSOF

Il termine FORMSOF esegue le corrispondenze usando altre forme linguistiche della parola. Di seguito è riportata la sintassi del termine FORMSOF:


```
FORMSOF (<generation_type>,<match_words>)
```



Il tipo di generazione specifica in che modo Microsoft Windows ricerca sceglie le forme di parola alternative. Il **valore INFLECTIONAL** sceglie forme di inflezione alternative per le parole corrispondenti. Se la parola è un verbo, vengono usati tempi alternativi. Se la parola è un sostantivo, vengono usate le forme singolare, plurale e possessiva per rilevare le corrispondenze.

Il valore \_ delle parole di corrispondenza è una o più parole, separate da virgole.

## <a name="examples"></a>Esempio

Nell'esempio seguente vengono cercate corrispondenze flesse per la parola "run". Questo esempio corrisponde a documenti contenenti "run", "running" o "ran".


```
...CONTAINS('FORMSOF(INFLECTIONAL,"run")')
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Predicato FREETEXT](-search-sql-freetext.md)
</dt> <dt>

[Clausola WHERE](-search-sql-where.md)
</dt> </dl>

 

 



