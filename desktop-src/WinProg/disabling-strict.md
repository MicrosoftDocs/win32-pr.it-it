---
title: Disabilitazione di STRICT
description: Per disabilitare il controllo RIGOROSo dei tipi, definire il nome del simbolo senza \_ strict. In Visual C/C++ è anche possibile specificare questa definizione nella riga di comando o in un makefile specificando/DNO \_ strict come opzione del compilatore.
ms.assetid: 57b01d2e-1f64-4ac0-b4f0-624c241899d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bfdfef2aa7988576aa4c1e17f002639de98121
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711977"
---
# <a name="disabling-strict"></a>Disabilitazione di STRICT

Per disabilitare il controllo **rigoroso** dei tipi, definire il nome del simbolo **senza \_ strict**. In Visual C/C++ è anche possibile specificare questa definizione nella riga di comando o in un makefile specificando **/dno \_ strict** come opzione del compilatore.

Per definire **Nessuna \_ restrizione** in base a file, inserire un'istruzione **\# define** prima di includere Windows. h:


```C++
#define NO_STRICT
#include <windows.h>
```



Per ottenere risultati ottimali, è necessario impostare anche il livello di avviso per i messaggi di errore su almeno **/W3**. Questa operazione è sempre consigliabile con le applicazioni per Windows, perché una procedura di codifica che genera un avviso, ad esempio il passaggio di un numero errato di parametri, causa in genere un errore irreversibile in fase di esecuzione se non viene corretto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Abilitazione di STRICT](enabling-strict.md)
</dt> <dt>

[Conformità RIGOROSa](strict-compliance.md)
</dt> </dl>

 

 




