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
# <a name="building-directshow-filters"></a><span data-ttu-id="166f8-103">Creazione di filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="166f8-103">Building DirectShow Filters</span></span>

<span data-ttu-id="166f8-104">Le classi base di DirectShow sono consigliate per l'implementazione di filtri DirectShow.</span><span class="sxs-lookup"><span data-stu-id="166f8-104">The DirectShow base classes are recommended for implementing DirectShow filters.</span></span> <span data-ttu-id="166f8-105">Per compilare con le classi base, seguire questa procedura, oltre ai passaggi elencati in [configurazione dell'ambiente di compilazione](setting-up-the-build-environment.md):</span><span class="sxs-lookup"><span data-stu-id="166f8-105">To build with the base classes, perform the following steps, in addition to the steps listed in [Setting Up the Build Environment](setting-up-the-build-environment.md):</span></span>

-   <span data-ttu-id="166f8-106">Compilare la libreria di classi di base, disponibile nella directory Samples \\ Multimedia \\ DirectShow \\ BaseClasses, nella directory radice dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="166f8-106">Build the base class library, located in the directory Samples\\Multimedia\\DirectShow\\BaseClasses, under the SDK root directory.</span></span> <span data-ttu-id="166f8-107">Sono disponibili due versioni della libreria: una versione definitiva (Strmbase. lib) e una versione di debug (Strmbasd. lib).</span><span class="sxs-lookup"><span data-stu-id="166f8-107">There are two versions of the library: a retail version (Strmbase.lib) and a debug version (Strmbasd.lib).</span></span>
-   <span data-ttu-id="166f8-108">Includere il file di intestazione Streams. h.</span><span class="sxs-lookup"><span data-stu-id="166f8-108">Include the header file Streams.h.</span></span>
-   <span data-ttu-id="166f8-109">Usare la \_ \_ convenzione di chiamata stdcall.</span><span class="sxs-lookup"><span data-stu-id="166f8-109">Use the \_\_stdcall calling convention.</span></span>
-   <span data-ttu-id="166f8-110">Utilizzare la libreria di runtime C con multithreading (debug o retail, a seconda dei casi).</span><span class="sxs-lookup"><span data-stu-id="166f8-110">Use the multithreaded C run-time library (debug or retail, as appropriate).</span></span>
-   <span data-ttu-id="166f8-111">Includere un file di definizione (def) che esporta le funzioni DLL.</span><span class="sxs-lookup"><span data-stu-id="166f8-111">Include a definition (.def) file that exports the DLL functions.</span></span> <span data-ttu-id="166f8-112">Di seguito è riportato un esempio di un file di definizione.</span><span class="sxs-lookup"><span data-stu-id="166f8-112">The following is an example of a definition file.</span></span> <span data-ttu-id="166f8-113">Si presuppone che il file di output sia denominato MyFilter.dll.</span><span class="sxs-lookup"><span data-stu-id="166f8-113">It assumes that the output file is named MyFilter.dll.</span></span>
    ```C++
    LIBRARY MYFILTER.DLL
    EXPORTS 
        DllMain             PRIVATE
        DllGetClassObject   PRIVATE
        DllCanUnloadNow     PRIVATE
        DllRegisterServer   PRIVATE
        DllUnregisterServer PRIVATE
    ```

    

-   <span data-ttu-id="166f8-114">Collegamento ai file lib seguenti.</span><span class="sxs-lookup"><span data-stu-id="166f8-114">Link to the following lib files.</span></span>

    |              |                                      |
    |--------------|--------------------------------------|
    | <span data-ttu-id="166f8-115">Compilazione di debug</span><span class="sxs-lookup"><span data-stu-id="166f8-115">Debug Build</span></span>  | <span data-ttu-id="166f8-116">Strmbasd. lib, msvcrtd. lib, winmm. lib</span><span class="sxs-lookup"><span data-stu-id="166f8-116">Strmbasd.lib, Msvcrtd.lib, Winmm.lib</span></span> |
    | <span data-ttu-id="166f8-117">Compilazione al dettaglio</span><span class="sxs-lookup"><span data-stu-id="166f8-117">Retail Build</span></span> | <span data-ttu-id="166f8-118">Strmbase. lib, Msvcrt. lib, winmm. lib</span><span class="sxs-lookup"><span data-stu-id="166f8-118">Strmbase.lib, Msvcrt.lib, Winmm.lib</span></span>  |

    

     

-   <span data-ttu-id="166f8-119">Scegliere l'opzione "Ignora librerie predefinite" nelle impostazioni del linker.</span><span class="sxs-lookup"><span data-stu-id="166f8-119">Choose the "ignore default libraries" option in the linker settings.</span></span>
-   <span data-ttu-id="166f8-120">Dichiarare il punto di ingresso della DLL nel codice sorgente, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="166f8-120">Declare the DLL entry point in your source code, as follows:</span></span>
    ```C++
    extern "C" BOOL WINAPI DllEntryPoint(HINSTANCE, ULONG, LPVOID);
    BOOL APIENTRY DllMain(HANDLE hModule, DWORD dwReason, LPVOID lpReserved)
    {
        return DllEntryPoint((HINSTANCE)(hModule), dwReason, lpReserved);
    }
    ```

    

<span data-ttu-id="166f8-121">Versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="166f8-121">Previous Versions</span></span>

<span data-ttu-id="166f8-122">Per le versioni della libreria di classi di base prima di DirectShow 9,0, è necessario eseguire anche le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="166f8-122">For versions of the base class library before DirectShow 9.0, you must also do the following:</span></span>

-   <span data-ttu-id="166f8-123">Per le compilazioni di debug, definire il flag del preprocessore DEBUG.</span><span class="sxs-lookup"><span data-stu-id="166f8-123">For debug builds, define the preprocessor flag DEBUG.</span></span>

<span data-ttu-id="166f8-124">Questo passaggio non è necessario per la versione della libreria di classi di base disponibile in DirectShow 9,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="166f8-124">This step is not required for the version of the base class library that is available in DirectShow 9.0 and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="166f8-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="166f8-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="166f8-126">Classi base di DirectShow</span><span class="sxs-lookup"><span data-stu-id="166f8-126">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> <dt>

[<span data-ttu-id="166f8-127">Scrittura di filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="166f8-127">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



