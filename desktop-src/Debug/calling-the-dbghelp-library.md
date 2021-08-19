---
description: Anche DbgHelp.dll viene fornito con tutte le versioni di Windows, i chiamanti devono prendere in considerazione l'uso di una delle versioni più recenti di questa DLL, come illustrato nel pacchetto Debugging Tools For Windows. Per informazioni dettagliate sulla distribuzione di DbgHelp, vedere Versioni di DbgHelp.
ms.assetid: 4e615e75-5ab8-4155-a3d3-b96313b37e9b
title: Chiamata della libreria DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4d6a111da8b0874a0c66fa08840e1ea4edeabf539afab2e9decf0eb19372db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957160"
---
# <a name="calling-the-dbghelp-library"></a>Chiamata della libreria DbgHelp

Anche DbgHelp.dll viene fornito con tutte le versioni di Windows, i chiamanti devono prendere in considerazione l'uso di una delle versioni più recenti di questa DLL, come illustrato nel pacchetto [Debugging Tools For Windows.](https://www.microsoft.com/?ref=go) Per informazioni dettagliate sulla distribuzione di DbgHelp, vedere [Versioni di DbgHelp.](dbghelp-versions.md)

Quando si usa DbgHelp, la strategia migliore consiste nell'installare una copia della libreria dal pacchetto debugging [tools for Windows](https://www.microsoft.com/?ref=go) nella directory dell'applicazione logicamente adiacente al software che la chiama. Se sono necessari anche il server di simboli e il server di origine, sia SymSrv.dll che SrcSrv.dll devono essere installati nella stessa directory di DbgHelp.dll, perché DbgHelp chiamerà queste DLL solo se condividono la stessa directory. Si noti che DbgHelp non chiamerà queste due DLL dal percorso di ricerca standard. Ciò consente di evitare l'utilizzo di DLL non corrispondenti. allo stesso modo, migliora anche la sicurezza complessiva.

Il codice seguente viene estratto dall'origine DbgHelp. Viene illustrato come DbgHelp carica solo le versioni di SymSrv.dll e SrcSrv.dll dalla stessa directory in cui DbgHelp.dll risiede.


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



Dopo aver caricato queste due DLL, DbgHelp chiama [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per ottenere le funzioni necessarie.

In genere, il codice che chiama DbgHelp.dll assicura che la versione corretta sia caricata installando DbgHelp.dll nella stessa directory dell'applicazione che ha avviato il processo corrente. Se il codice chiamante si trova in una DLL e non dispone dell'accesso o della conoscenza del percorso del processo iniziale, è necessario installare DbgHelp.dll insieme alla DLL chiamante e usare codice simile a LoadDLL di DbgHelp.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Versioni di DbgHelp](dbghelp-versions.md)
</dt> <dt>

[**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> </dl>

 

 
