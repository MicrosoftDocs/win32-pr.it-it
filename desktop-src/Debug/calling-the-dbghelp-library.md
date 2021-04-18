---
description: Sebbene DbgHelp.dll venga fornito con tutte le versioni di Windows, i chiamanti devono prendere in considerazione l'uso di una delle versioni più recenti di questa DLL come indicato nel pacchetto strumenti di debug per Windows. Per informazioni dettagliate sulla distribuzione di DbgHelp, vedere versioni di DbgHelp.
ms.assetid: 4e615e75-5ab8-4155-a3d3-b96313b37e9b
title: Chiamata della libreria DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70cc06f6a0e28f163d80490647ee8f33754c249b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482749"
---
# <a name="calling-the-dbghelp-library"></a><span data-ttu-id="0b3a9-104">Chiamata della libreria DbgHelp</span><span class="sxs-lookup"><span data-stu-id="0b3a9-104">Calling the DbgHelp Library</span></span>

<span data-ttu-id="0b3a9-105">Sebbene DbgHelp.dll venga fornito con tutte le versioni di Windows, i chiamanti devono prendere in considerazione l'uso di una delle versioni più recenti di questa DLL come indicato nel pacchetto [strumenti di debug per Windows](https://www.microsoft.com/?ref=go) .</span><span class="sxs-lookup"><span data-stu-id="0b3a9-105">Although DbgHelp.dll ships with all versions of Windows, callers should consider using one of the more recent versions of this DLL as found in the [Debugging Tools For Windows](https://www.microsoft.com/?ref=go) package.</span></span> <span data-ttu-id="0b3a9-106">Per informazioni dettagliate sulla distribuzione di DbgHelp, vedere [versioni di dbghelp](dbghelp-versions.md).</span><span class="sxs-lookup"><span data-stu-id="0b3a9-106">For details on distribution of DbgHelp, see [DbgHelp Versions](dbghelp-versions.md).</span></span>

<span data-ttu-id="0b3a9-107">Quando si usa DbgHelp, la strategia migliore consiste nell'installare una copia della libreria dal pacchetto degli [strumenti di debug per Windows](https://www.microsoft.com/?ref=go) nella directory dell'applicazione in modo logico adiacente al software che lo chiama.</span><span class="sxs-lookup"><span data-stu-id="0b3a9-107">When using DbgHelp, the best strategy is to install a copy of the library from the [Debugging Tools For Windows](https://www.microsoft.com/?ref=go) package in the application directory logically adjacent to the software that calls it.</span></span> <span data-ttu-id="0b3a9-108">Se sono necessari anche il server di simboli e il server di origine, è necessario installare sia SymSrv.dll che SrcSrv.dll nella stessa directory del DbgHelp.dll, perché DbgHelp chiamerà solo queste dll se condividono la stessa directory.</span><span class="sxs-lookup"><span data-stu-id="0b3a9-108">If Symbol Server and Source Server are also needed, then both SymSrv.dll and SrcSrv.dll must be installed in the same directory as DbgHelp.dll, as DbgHelp will only call these DLLs if they share the same directory with it.</span></span> <span data-ttu-id="0b3a9-109">Si noti che DbgHelp non chiamerà queste due dll dal percorso di ricerca standard. Ciò consente di evitare l'utilizzo di dll non corrispondenti; allo stesso modo, migliora anche la sicurezza complessiva.</span><span class="sxs-lookup"><span data-stu-id="0b3a9-109">(Note that DbgHelp will not call these two DLLs from the standard search path.) This helps prevent the usage of mismatched DLLs; likewise, it also improves security overall.</span></span>

<span data-ttu-id="0b3a9-110">Il codice seguente viene estratto dall'origine DbgHelp.</span><span class="sxs-lookup"><span data-stu-id="0b3a9-110">The following code is extracted from the DbgHelp source.</span></span> <span data-ttu-id="0b3a9-111">Mostra in che modo DbgHelp carica solo le versioni di SymSrv.dll e SrcSrv.dll dalla stessa directory in cui risiede DbgHelp.dll.</span><span class="sxs-lookup"><span data-stu-id="0b3a9-111">It shows how DbgHelp only loads versions of SymSrv.dll and SrcSrv.dll from the same directory that DbgHelp.dll resides in.</span></span>


```C++
HINSTANCE ghinst;

// For calculating the size of arrays for safe string functions.

#ifndef cch
 #define ccht(Array, EltType) (sizeof(Array) / sizeof(EltType))
 #define cch(Array) ccht(Array, (Array)[0])
#endif

//
// LoadLibrary() a DLL, using the same directory as dbghelp.dll.
//

HMODULE 
LoadDLL(
    __in PCWSTR filename
    )
{
    WCHAR drive[10] = L"";
    WCHAR dir[MAX_PATH + 1] = L"";
    WCHAR file[MAX_PATH + 1] = L"";
    WCHAR ext[MAX_PATH + 1] = L"";
    WCHAR path[MAX_PATH + 1] = L"";
    HMODULE hm;
    
    // Chop up 'filename' into its elements.
    
    _wsplitpath_s(filename, drive, cch(drive), dir, cch(dir), file, cch(file), ext, cch(ext));

    // If 'filename' contains no path information, then get the path to our module and 
    // use it to create a fully qualified path to the module we are loading.  Then load it.
    
    if (!*drive && !*dir) 
    {
        // ghinst is the HINSTANCE of this module, initialized in DllMain or WinMain
         
        if (GetModuleFileNameW(ghinst, path, MAX_PATH)) 
        {
            _wsplitpath_s(path, drive, cch(drive), dir, cch(dir), NULL, 0, NULL, 0);
            if (*drive || *dir) 
            {
                swprintf_s(path, cch(path), L"%s%s%s%s", drive, dir, file, ext);
                hm = LoadLibrary(path);
                if (hm)
                    return hm;
            }
        }
    }
    else
    {
        // If we wanted to, we could have LoadDLL also support directories being specified
        // in 'filename'.  We could pass the path here.  The result is if no path is specified,
        // the module path is used as above, otherwise the path in 'filename' is specified.
        // But the standard search logic of LoadLibrary is still avoided.
        
        /*
        hm = LoadLibrary(path);
        if (hm)
            return hm;
        */
    }
    
    return 0;
}
```



<span data-ttu-id="0b3a9-112">Dopo il caricamento di queste due dll, DbgHelp chiama [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per ottenere le funzioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="0b3a9-112">After loading these two DLLs, DbgHelp calls [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) to obtain the functions it needs from them.</span></span>

<span data-ttu-id="0b3a9-113">In genere, il codice che chiama DbgHelp.dll garantisce che venga caricata la versione corretta installando DbgHelp.dll nella stessa directory dell'applicazione che ha avviato il processo corrente.</span><span class="sxs-lookup"><span data-stu-id="0b3a9-113">Normally, code that calls DbgHelp.dll ensures that the correct version is loaded by installing DbgHelp.dll in the same directory as the application that initiated the current process.</span></span> <span data-ttu-id="0b3a9-114">Se il codice chiamante si trova in una DLL e non dispone dell'accesso o della conoscenza della posizione del processo iniziale, DbgHelp.dll necessario installare insieme alla DLL chiamante e scrivere codice simile a LoadDLL di DbgHelp.</span><span class="sxs-lookup"><span data-stu-id="0b3a9-114">If the calling code is in a DLL and does not have access to or knowledge of the location of the initial process, then DbgHelp.dll must be installed alongside the calling DLL and code similar to DbgHelp's LoadDLL should be used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b3a9-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0b3a9-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b3a9-116">Versioni di DbgHelp</span><span class="sxs-lookup"><span data-stu-id="0b3a9-116">DbgHelp Versions</span></span>](dbghelp-versions.md)
</dt> <dt>

[<span data-ttu-id="0b3a9-117">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="0b3a9-117">**LoadLibrary**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="0b3a9-118">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="0b3a9-118">**GetProcAddress**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="0b3a9-119">**GetModuleFileName**</span><span class="sxs-lookup"><span data-stu-id="0b3a9-119">**GetModuleFileName**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> </dl>

 

 
