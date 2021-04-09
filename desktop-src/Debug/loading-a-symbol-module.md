---
description: Se un'applicazione non chiama la funzione SymInitialize con il parametro fInvadeProcess impostato su TRUE, deve caricare i simboli per un modulo quando sono necessari.
ms.assetid: 01cee812-d1f2-4459-acee-bce8719a85b2
title: Caricamento di un modulo dei simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5182322e62b450333a064069ea5f5de2aa95e912
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125973"
---
# <a name="loading-a-symbol-module"></a>Caricamento di un modulo dei simboli

Se un'applicazione non chiama la funzione [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) con il parametro *FInvadeProcess* impostato su **true**, deve caricare i simboli per un modulo quando sono necessari. Per caricare un modulo di simboli su richiesta, l'applicazione può chiamare la funzione [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) con il percorso completo di un nome di modulo. Quando il modulo viene caricato, il gestore di simboli caricherà immediatamente i simboli o rinvia il carico, a seconda delle opzioni impostate mediante la funzione [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) .

Il codice seguente carica un modulo dei simboli. Si noti che si presuppone che sia stato inizializzato il gestore di simboli utilizzando il codice nell' [inizializzazione del gestore di simboli](initializing-the-symbol-handler.md).


```C++
TCHAR  szImageName[MAX_PATH] = TEXT("foo.dll");
DWORD64 dwBaseAddr = 0;

if (SymLoadModuleEx(hProcess,    // target process 
                    NULL,        // handle to image - not used
                    szImageName, // name of image file
                    NULL,        // name of module - not required
                    dwBaseAddr,  // base address - not required
                    0,           // size of image - not required
                    NULL,        // MODLOAD_DATA used for special cases 
                    0))          // flags - not required
{
    // SymLoadModuleEx returned success
}
else
{
    // SymLoadModuleEx failed
    DWORD error = GetLastError();
    printf("SymLoadModuleEx returned error : %d\n", error);
}
```



Si noti che *szImageName* può essere un percorso di qualsiasi modulo eseguibile con informazioni di debug (. exe,. dll,. drv,. sys,. SCR,. cpl,. com). Inoltre, *dwBaseAddr* è l'indirizzo di base del modulo dei simboli da caricare. Se questo valore è 0, il gestore di simboli otterrà l'indirizzo di base dal modulo dei simboli specificato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scaricamento di un modulo di simboli](unloading-a-symbol-module.md)
</dt> </dl>

 

 



