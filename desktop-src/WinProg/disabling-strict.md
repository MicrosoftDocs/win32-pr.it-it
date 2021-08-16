---
title: Disabilitazione di STRICT
description: Per disabilitare il controllo dei tipi STRICT, definire il nome del simbolo NO \_ STRICT. In Visual C/C++, è anche possibile specificare questa definizione nella riga di comando o in un makefile specificando /DNO STRICT come opzione \_ del compilatore.
ms.assetid: 57b01d2e-1f64-4ac0-b4f0-624c241899d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078361b5cc3fd4916ac2ab4f7207752e869568b8781c9ef3dd8e38427d252592
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743657"
---
# <a name="disabling-strict"></a>Disabilitazione di STRICT

Per disabilitare il controllo dei tipi **STRICT,** definire il nome del **simbolo NO \_ STRICT.** In Visual C/C++, è anche possibile specificare questa definizione nella riga di comando o in un makefile specificando **/DNO \_ STRICT** come opzione del compilatore.

Per definire **NO \_ STRICT** file per file, inserire un'istruzione **\# define** prima di includere Windows.h:


```C++
#define NO_STRICT
#include <windows.h>
```



Per ottenere risultati ottimali, è necessario impostare anche il livello di avviso per i messaggi di errore su **almeno /W3**. Questo è sempre consigliabile con le applicazioni per Windows, perché una procedura di scrittura del codice che causa un avviso (ad esempio, il passaggio di un numero errato di parametri) causa in genere un errore irreversibile in fase di esecuzione se non viene corretto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Abilitazione di STRICT](enabling-strict.md)
</dt> <dt>

[Conformità STRICT](strict-compliance.md)
</dt> </dl>

 

 




