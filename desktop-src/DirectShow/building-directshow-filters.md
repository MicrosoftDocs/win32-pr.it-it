---
description: Creazione di filtri DirectShow
ms.assetid: fb907263-e7f3-42d6-80f9-a9f16fc21033
title: Creazione di filtri DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5553c4358f97809214ebbdea23c129aa7c214e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747071"
---
# <a name="building-directshow-filters"></a>Creazione di filtri DirectShow

Le classi base di DirectShow sono consigliate per l'implementazione di filtri DirectShow. Per compilare con le classi base, seguire questa procedura, oltre ai passaggi elencati in [configurazione dell'ambiente di compilazione](setting-up-the-build-environment.md):

-   Compilare la libreria di classi di base, disponibile nella directory Samples \\ Multimedia \\ DirectShow \\ BaseClasses, nella directory radice dell'SDK. Sono disponibili due versioni della libreria: una versione definitiva (Strmbase. lib) e una versione di debug (Strmbasd. lib).
-   Includere il file di intestazione Streams. h.
-   Usare la \_ \_ convenzione di chiamata stdcall.
-   Utilizzare la libreria di runtime C con multithreading (debug o retail, a seconda dei casi).
-   Includere un file di definizione (def) che esporta le funzioni DLL. Di seguito è riportato un esempio di un file di definizione. Si presuppone che il file di output sia denominato MyFilter.dll.
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

    |              |                                      |
    |--------------|--------------------------------------|
    | Compilazione di debug  | Strmbasd. lib, msvcrtd. lib, winmm. lib |
    | Compilazione al dettaglio | Strmbase. lib, Msvcrt. lib, winmm. lib  |

    

     

-   Scegliere l'opzione "Ignora librerie predefinite" nelle impostazioni del linker.
-   Dichiarare il punto di ingresso della DLL nel codice sorgente, come indicato di seguito:
    ```C++
    extern "C" BOOL WINAPI DllEntryPoint(HINSTANCE, ULONG, LPVOID);
    BOOL APIENTRY DllMain(HANDLE hModule, DWORD dwReason, LPVOID lpReserved)
    {
        return DllEntryPoint((HINSTANCE)(hModule), dwReason, lpReserved);
    }
    ```

    

Versioni precedenti

Per le versioni della libreria di classi di base prima di DirectShow 9,0, è necessario eseguire anche le operazioni seguenti:

-   Per le compilazioni di debug, definire il flag del preprocessore DEBUG.

Questo passaggio non è necessario per la versione della libreria di classi di base disponibile in DirectShow 9,0 e versioni successive.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Classi base di DirectShow](directshow-base-classes.md)
</dt> <dt>

[Scrittura di filtri DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



