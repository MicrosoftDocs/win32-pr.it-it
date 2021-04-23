---
description: Compilazione di DirectMostra filtri
ms.assetid: fb907263-e7f3-42d6-80f9-a9f16fc21033
title: Compilazione di DirectMostra filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7090eed702b1abe8ee863d5fa3ac9c1fd413690e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908619"
---
# <a name="building-directshow-filters"></a><span data-ttu-id="12816-103">Compilazione di DirectMostra filtri</span><span class="sxs-lookup"><span data-stu-id="12816-103">Building DirectShow Filters</span></span>

<span data-ttu-id="12816-104">Le classi di base DirectShow sono consigliate per l'implementazione di filtri DirectShow.</span><span class="sxs-lookup"><span data-stu-id="12816-104">The DirectShow base classes are recommended for implementing DirectShow filters.</span></span> <span data-ttu-id="12816-105">Per eseguire la compilazione con le classi di base, seguire questa procedura, oltre ai passaggi elencati in [Configurazione dell'ambiente di compilazione:](setting-up-the-build-environment.md)</span><span class="sxs-lookup"><span data-stu-id="12816-105">To build with the base classes, perform the following steps, in addition to the steps listed in [Setting Up the Build Environment](setting-up-the-build-environment.md):</span></span>

-   <span data-ttu-id="12816-106">Compilare la libreria di classi di base, che si trova nella directory \\ Samples Multimedia \\ DirectShow \\ BaseClasses, nella directory radice dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="12816-106">Build the base class library, located in the directory Samples\\Multimedia\\DirectShow\\BaseClasses, under the SDK root directory.</span></span> <span data-ttu-id="12816-107">Esistono due versioni della libreria: una versione definitiva (Strmbase.lib) e una versione di debug (Strmbasd.lib).</span><span class="sxs-lookup"><span data-stu-id="12816-107">There are two versions of the library: a retail version (Strmbase.lib) and a debug version (Strmbasd.lib).</span></span>
-   <span data-ttu-id="12816-108">Includere il file di intestazione Streams.h.</span><span class="sxs-lookup"><span data-stu-id="12816-108">Include the header file Streams.h.</span></span>
-   <span data-ttu-id="12816-109">Usare la \_ \_ convenzione di chiamata stdcall.</span><span class="sxs-lookup"><span data-stu-id="12816-109">Use the \_\_stdcall calling convention.</span></span>
-   <span data-ttu-id="12816-110">Usare la libreria di runtime C multithreading (debug o definitiva, in base alle esigenze).</span><span class="sxs-lookup"><span data-stu-id="12816-110">Use the multithreaded C run-time library (debug or retail, as appropriate).</span></span>
-   <span data-ttu-id="12816-111">Includere un file di definizione (def) che esporta le funzioni DLL.</span><span class="sxs-lookup"><span data-stu-id="12816-111">Include a definition (.def) file that exports the DLL functions.</span></span> <span data-ttu-id="12816-112">Di seguito è riportato un esempio di file di definizione.</span><span class="sxs-lookup"><span data-stu-id="12816-112">The following is an example of a definition file.</span></span> <span data-ttu-id="12816-113">Si presuppone che il file di output sia denominato MyFilter.dll.</span><span class="sxs-lookup"><span data-stu-id="12816-113">It assumes that the output file is named MyFilter.dll.</span></span>
    ```C++
    LIBRARY MYFILTER.DLL
    EXPORTS 
        DllMain             PRIVATE
        DllGetClassObject   PRIVATE
        DllCanUnloadNow     PRIVATE
        DllRegisterServer   PRIVATE
        DllUnregisterServer PRIVATE
    ```

    

-   <span data-ttu-id="12816-114">Collegamento ai file lib seguenti.</span><span class="sxs-lookup"><span data-stu-id="12816-114">Link to the following lib files.</span></span>

| <span data-ttu-id="12816-115">Label</span><span class="sxs-lookup"><span data-stu-id="12816-115">Label</span></span> | <span data-ttu-id="12816-116">Valore</span><span class="sxs-lookup"><span data-stu-id="12816-116">Value</span></span> |
    |--------------|--------------------------------------|
    | <span data-ttu-id="12816-117">Eseguire il debug della compilazione</span><span class="sxs-lookup"><span data-stu-id="12816-117">Debug Build</span></span>  | <span data-ttu-id="12816-118">Strmbasd.lib, Msvcrtd.lib, Winmm.lib</span><span class="sxs-lookup"><span data-stu-id="12816-118">Strmbasd.lib, Msvcrtd.lib, Winmm.lib</span></span> |
    | <span data-ttu-id="12816-119">Retail Build</span><span class="sxs-lookup"><span data-stu-id="12816-119">Retail Build</span></span> | <span data-ttu-id="12816-120">Strmbase.lib, Msvcrt.lib, Winmm.lib</span><span class="sxs-lookup"><span data-stu-id="12816-120">Strmbase.lib, Msvcrt.lib, Winmm.lib</span></span>  |

    

     

-   <span data-ttu-id="12816-121">Scegliere l'opzione "Ignora librerie predefinite" nelle impostazioni del linker.</span><span class="sxs-lookup"><span data-stu-id="12816-121">Choose the "ignore default libraries" option in the linker settings.</span></span>
-   <span data-ttu-id="12816-122">Dichiarare il punto di ingresso dll nel codice sorgente, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="12816-122">Declare the DLL entry point in your source code, as follows:</span></span>
    ```C++
    extern "C" BOOL WINAPI DllEntryPoint(HINSTANCE, ULONG, LPVOID);
    BOOL APIENTRY DllMain(HANDLE hModule, DWORD dwReason, LPVOID lpReserved)
    {
        return DllEntryPoint((HINSTANCE)(hModule), dwReason, lpReserved);
    }
    ```

    

<span data-ttu-id="12816-123">Versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="12816-123">Previous Versions</span></span>

<span data-ttu-id="12816-124">Per le versioni della libreria di classi di base precedenti a DirectShow 9.0, è necessario eseguire anche le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="12816-124">For versions of the base class library before DirectShow 9.0, you must also do the following:</span></span>

-   <span data-ttu-id="12816-125">Per le build di debug, definire il flag del preprocessore DEBUG.</span><span class="sxs-lookup"><span data-stu-id="12816-125">For debug builds, define the preprocessor flag DEBUG.</span></span>

<span data-ttu-id="12816-126">Questo passaggio non è necessario per la versione della libreria di classi di base disponibile in DirectShow 9.0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="12816-126">This step is not required for the version of the base class library that is available in DirectShow 9.0 and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12816-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="12816-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12816-128">Classi di base DirectShow</span><span class="sxs-lookup"><span data-stu-id="12816-128">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> <dt>

[<span data-ttu-id="12816-129">Scrittura di filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="12816-129">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



