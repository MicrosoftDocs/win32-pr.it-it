---
description: Il termine FORMSOF esegue corrispondenze usando altre forme linguistiche della parola.
ms.assetid: b705b8bc-dc2c-4cee-8306-f494b0f96cbf
title: Termine FORMSOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20504a7a36c7f0cb9c69b9513f33446501641bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306129"
---
# <a name="formsof-term"></a>Termine FORMSOF

Il termine FORMSOF esegue corrispondenze usando altre forme linguistiche della parola. Di seguito è riportata la sintassi del termine FORMSOF:


```
FORMSOF (<generation_type>,<match_words>)
```



Il tipo di generazione specifica il modo in cui Microsoft Windows Search sceglie i moduli Word alternativi. Il valore **flessore** sceglie forme di flessione alternative per le parole di corrispondenza. Se la parola è un verbo, vengono usati i tempi alternativi. Se la parola è un sostantivo, le forme singolare, plurale e possessive vengono usate per rilevare le corrispondenze.

Il valore delle parole di ricerca corrisponde \_ a una o più parole, separate da virgole.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene eseguita la ricerca di corrispondenze flessori per la parola "Run". Questo esempio corrisponde ai documenti che contengono "Run", "Running" o "Ran".


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

 

 



