---
description: Nel codice seguente viene illustrato come inizializzare il gestore di simboli.
ms.assetid: e8c8f648-c3b0-4595-ac07-f508dd576d9f
title: Inizializzazione del gestore di simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d5a7ba79a71a389f185a5e18065af818223d4cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965945"
---
# <a name="initializing-the-symbol-handler"></a>Inizializzazione del gestore di simboli

Nel codice seguente viene illustrato come inizializzare il gestore di simboli. La funzione [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) rinvia il caricamento dei simboli fino a quando non vengono richieste informazioni sui simboli. Il codice carica i simboli per ogni modulo nel processo specificato passando il valore **true** per il parametro *BInvade* della funzione [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) . Questa funzione chiama la funzione [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) per ogni modulo a cui è stato eseguito il mapping del processo nello spazio degli indirizzi.

Se il processo specificato non è il processo che ha chiamato [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize), il codice passa un identificatore di processo come primo parametro di **SymInitialize**.

Se si specifica **null** come secondo parametro di [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) , il gestore di simboli deve utilizzare il percorso di ricerca predefinito per individuare i file di simboli. Per informazioni dettagliate sul modo in cui il gestore di simboli individua i file di simboli o su come un'applicazione può specificare un percorso di ricerca dei simboli, vedere [percorsi](symbol-paths.md)dei simboli.


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



 

 



