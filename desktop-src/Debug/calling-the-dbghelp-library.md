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
# <a name="calling-the-dbghelp-library"></a>Chiamata della libreria DbgHelp

Sebbene DbgHelp.dll venga fornito con tutte le versioni di Windows, i chiamanti devono prendere in considerazione l'uso di una delle versioni più recenti di questa DLL come indicato nel pacchetto [strumenti di debug per Windows](https://www.microsoft.com/?ref=go) . Per informazioni dettagliate sulla distribuzione di DbgHelp, vedere [versioni di dbghelp](dbghelp-versions.md).

Quando si usa DbgHelp, la strategia migliore consiste nell'installare una copia della libreria dal pacchetto degli [strumenti di debug per Windows](https://www.microsoft.com/?ref=go) nella directory dell'applicazione in modo logico adiacente al software che lo chiama. Se sono necessari anche il server di simboli e il server di origine, è necessario installare sia SymSrv.dll che SrcSrv.dll nella stessa directory del DbgHelp.dll, perché DbgHelp chiamerà solo queste dll se condividono la stessa directory. Si noti che DbgHelp non chiamerà queste due dll dal percorso di ricerca standard. Ciò consente di evitare l'utilizzo di dll non corrispondenti; allo stesso modo, migliora anche la sicurezza complessiva.

Il codice seguente viene estratto dall'origine DbgHelp. Mostra in che modo DbgHelp carica solo le versioni di SymSrv.dll e SrcSrv.dll dalla stessa directory in cui risiede DbgHelp.dll.


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



Dopo il caricamento di queste due dll, DbgHelp chiama [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per ottenere le funzioni necessarie.

In genere, il codice che chiama DbgHelp.dll garantisce che venga caricata la versione corretta installando DbgHelp.dll nella stessa directory dell'applicazione che ha avviato il processo corrente. Se il codice chiamante si trova in una DLL e non dispone dell'accesso o della conoscenza della posizione del processo iniziale, DbgHelp.dll necessario installare insieme alla DLL chiamante e scrivere codice simile a LoadDLL di DbgHelp.

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

 

 
