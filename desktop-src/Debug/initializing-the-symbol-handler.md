---
description: Nel codice seguente viene illustrato come inizializzare il gestore dei simboli.
ms.assetid: e8c8f648-c3b0-4595-ac07-f508dd576d9f
title: Inizializzazione del gestore dei simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f1da864c4550232d278b6bfb9b2006a6d56956e363dcf4fbd72ed0e6b9685d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956980"
---
# <a name="initializing-the-symbol-handler"></a>Inizializzazione del gestore dei simboli

Nel codice seguente viene illustrato come inizializzare il gestore dei simboli. La [**funzione SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) rinvia il caricamento dei simboli fino a quando non vengono richieste le informazioni sui simboli. Il codice carica i simboli per ogni modulo nel processo specificato passando il valore **TRUE** per il *parametro bInvade* della [**funzione SymInitialize.**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) Questa funzione chiama la funzione [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) per ogni modulo di cui è stato eseguito il mapping del processo nel relativo spazio indirizzi.

Se il processo specificato non è il processo che ha chiamato [**SymInitialize,**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)il codice passa un identificatore di processo come primo parametro di **SymInitialize.**

Se si **specifica NULL** come secondo parametro di [**SymInitialize,**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) il gestore dei simboli deve usare il percorso di ricerca predefinito per individuare i file di simboli. Per informazioni dettagliate su come il gestore dei simboli individua i file di simboli o su come un'applicazione può specificare un percorso di ricerca dei simboli, vedere [Percorsi dei simboli.](symbol-paths.md)


```C++
DWORD  error;
HANDLE hProcess;

SymSetOptions(SYMOPT_UNDNAME | SYMOPT_DEFERRED_LOADS);

hProcess = GetCurrentProcess();

if (!SymInitialize(hProcess, NULL, TRUE))
{
    // SymInitialize failed
    error = GetLastError();
    printf("SymInitialize returned error : %d\n", error);
    return FALSE;
}
```



 

 



