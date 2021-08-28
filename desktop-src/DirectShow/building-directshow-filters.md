---
description: Compilazione DirectShow filtri
ms.assetid: fb907263-e7f3-42d6-80f9-a9f16fc21033
title: Compilazione DirectShow filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d87d1983d3bfd42d1a1582ef696b6793acdd0856dde2bd2d589e809acc614314
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794322"
---
# <a name="building-directshow-filters"></a>Compilazione DirectShow filtri

Le DirectShow di base sono consigliate per l'implementazione DirectShow filtri. Per eseguire la compilazione con le classi di base, seguire questa procedura, oltre ai passaggi elencati in [Configurazione dell'ambiente di compilazione:](setting-up-the-build-environment.md)

-   Compilare la libreria di classi di base, che si trova nella directory \\ Samples Multimedia \\ DirectShow \\ BaseClasses, nella directory radice dell'SDK. Esistono due versioni della libreria: una versione definitiva (Strmbase.lib) e una versione di debug (Strmbasd.lib).
-   Includere il file di intestazione Flussi.h.
-   Usare la \_ \_ convenzione di chiamata stdcall.
-   Usare la libreria di runtime C multithreading (debug o retail, in base alle esigenze).
-   Includere un file di definizione (def) che esporta le funzioni DLL. Di seguito è riportato un esempio di file di definizione. Si presuppone che il file di output sia denominato MyFilter.dll.
    ```C++
    LIBRARY MYFILTER.DLL
    EXPORTS 
        DllMain             PRIVATE
        DllGetClassObject   PRIVATE
        DllCanUnloadNow     PRIVATE
        DllRegisterServer   PRIVATE
        DllUnregisterServer PRIVATE
    ```

    

-   Collegamento ai file lib seguenti.

| Etichetta | Valore |
    |--------------|--------------------------------------|
    | Eseguire il debug della compilazione  | Strmbasd.lib, Msvcrtd.lib, Winmm.lib |
    | Retail Build | Strmbase.lib, Msvcrt.lib, Winmm.lib  |

    

     

-   Scegliere l'opzione "Ignora librerie predefinite" nelle impostazioni del linker.
-   Dichiarare il punto di ingresso dll nel codice sorgente, come indicato di seguito:
    ```C++
    extern "C" BOOL WINAPI DllEntryPoint(HINSTANCE, ULONG, LPVOID);
    BOOL APIENTRY DllMain(HANDLE hModule, DWORD dwReason, LPVOID lpReserved)
    {
        return DllEntryPoint((HINSTANCE)(hModule), dwReason, lpReserved);
    }
    ```

    

Versioni precedenti

Per le versioni della libreria di classi di base DirectShow 9.0, è necessario eseguire anche le operazioni seguenti:

-   Per le compilazioni di debug, definire il flag del preprocessore DEBUG.

Questo passaggio non è necessario per la versione della libreria di classi base disponibile in DirectShow 9.0 e versioni successive.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Classi di base](directshow-base-classes.md)
</dt> <dt>

[Scrittura DirectShow filtri](writing-directshow-filters.md)
</dt> </dl>

 

 



