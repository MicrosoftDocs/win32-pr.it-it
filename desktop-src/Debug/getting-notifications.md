---
description: Nel codice seguente viene illustrato come ottenere e segnalare informazioni dettagliate sullo stato dal gestore di simboli per la ricerca e il caricamento dei moduli e dei file di simboli corrispondenti.
ms.assetid: 1dd8af0e-280b-4fc4-bf75-45c5c7517365
title: Ricezione di notifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bebaed2683f329fa267bdc926063d0b763190400
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225782"
---
# <a name="getting-notifications"></a>Ricezione di notifiche

Nel codice seguente viene illustrato come ottenere e segnalare informazioni dettagliate sullo stato dal gestore di simboli per la ricerca e il caricamento dei moduli e dei file di simboli corrispondenti.

Molti esperti del debugger WinDbg possono ricordare un comando denominato "! sym noisy". Questo comando viene usato dall'utente per determinare il motivo per cui WinDbg è o non è in grado di caricare i file di simboli. Mostra un elenco dettagliato di tutti gli elementi tentati dal gestore di simboli.

Questo stesso elenco è disponibile anche per tutti gli utenti che sviluppano un client nel gestore di simboli DbgHelp.

Prima di tutto, chiamare [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) con **SYMOPT \_ debug**. Questo fa in modo che DbgHelp accenda le notifiche di debug.

Dopo la chiamata a [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize), utilizzare [**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback) per registrare una funzione di callback che dbghelp chiamerà ogni volta che si verifica un evento interessante. In questo esempio, la funzione di callback è denominata [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback). Alle funzioni di callback dei simboli viene passata un'ampia gamma di codici di azione che è possibile gestire in base al tipo. In questo esempio viene gestito solo il codice dell'azione dell' **\_ evento CBA** . Questa funzione passa una stringa che contiene informazioni dettagliate su un evento che si è verificato nel processo di caricamento di un simbolo. Questo evento potrebbe essere un tentativo di leggere i dati all'interno di un'immagine eseguibile nella posizione corretta di un file di simboli. **SymRegisterCallbackProc64** Visualizza tale stringa e restituisce **true**.

> [!IMPORTANT]
> Assicurarsi di restituire **false** a ogni codice di azione che non si gestisce. in caso contrario, è possibile che si verifichi un comportamento non definito. Vedere [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback) per un elenco di tutti i codici di azione e le relative implicazioni.

 

Ora che il callback è registrato, è possibile caricare il modulo specificato nella riga di comando chiamando [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex).

Infine, chiamare [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) prima di uscire.


```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>

#ifdef UNICODE
 #define DBGHELP_TRANSLATE_TCHAR
#endif
#include <dbghelp.h>

// Here is an implementation of a Symbol Callback function.

BOOL 
CALLBACK 
SymRegisterCallbackProc64(
    __in HANDLE hProcess,
    __in ULONG ActionCode,
    __in_opt ULONG64 CallbackData,
    __in_opt ULONG64 UserContext
    )
{
    UNREFERENCED_PARAMETER(hProcess);
    UNREFERENCED_PARAMETER(UserContext);
    
    PIMAGEHLP_CBA_EVENT evt;

    // If SYMOPT_DEBUG is set, then the symbol handler will pass
    // verbose information on its attempt to load symbols.
    // This information be delivered as text strings.
    
    switch (ActionCode)
    {
    case CBA_EVENT:
        evt = (PIMAGEHLP_CBA_EVENT)CallbackData;
        _tprintf(_T("%s"), (PTSTR)evt->desc);
        break;

    // CBA_DEBUG_INFO is the old ActionCode for symbol spew.
    // It still works, but we use CBA_EVENT in this example.
#if 0
    case CBA_DEBUG_INFO:
        _tprintf(_T("%s"), (PTSTR)CallbackData);
        break;
#endif

    default:
        // Return false to any ActionCode we don't handle
        // or we could generate some undesirable behavior.
        return FALSE;
    }

    return TRUE;
}

// Main code.

int __cdecl
#ifdef UNICODE
_tmain(
#else
main(
#endif
    __in int argc,
    __in_ecount(argc) PCTSTR argv[]
    )
{
    BOOL status;
    int rc = -1;
    HANDLE hProcess;
    DWORD64 module;
    
    if (argc < 2)
    {
        _tprintf(_T("You must specify an executable image to load.\n"));
        return rc;
    }

    // If we want to se debug spew, we need to set this option.
        
    SymSetOptions(SYMOPT_DEBUG);
    
    // We are not debugging an actual process, so lets use a placeholder
    // value of 1 for hProcess just to ID these calls from any other
    // series we may want to load.  For this simple case, anything will do.
    
    hProcess = (HANDLE)1;
    
    // Initialize the symbol handler.  No symbol path.  
    // Just let dbghelp use _NT_SYMBOL_PATH
    
    status = SymInitialize(hProcess, NULL, false);
    if (!status)
    {
        _tprintf(_T("Error 0x%x calling SymInitialize.\n"), GetLastError());
        return rc;
    }
     
    // Now register our callback.
    
    status = SymRegisterCallback64(hProcess, SymRegisterCallbackProc64, NULL);
    if (!status)
    {
        _tprintf(_T("Error 0x%x calling SymRegisterCallback64.\n"), GetLastError());
        goto cleanup;
    }
    
    // Go ahead and load a module for testing.
    
    module = SymLoadModuleEx(hProcess,  // our unique id
                             NULL,      // no open file handle to image
                             argv[1],   // name of image to load
                             NULL,      // no module name - dbghelp will get it
                             0,         // no base address - dbghelp will get it
                             0,         // no module size - dbghelp will get it
                             NULL,      // no special MODLOAD_DATA structure
                             0);        // flags
    if (!module)
    {
        _tprintf(_T("Error 0x%x calling SymLoadModuleEx.\n"), GetLastError());
        goto cleanup;
    }
    rc = 0;
    
cleanup:
    SymCleanup(hProcess);
    
    return rc;    
}
```



Se si specifica **null** come secondo parametro di [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) , il gestore di simboli deve utilizzare il percorso di ricerca predefinito per individuare i file di simboli. Per informazioni dettagliate sul modo in cui il gestore di simboli individua i file di simboli o su come un'applicazione può specificare un percorso di ricerca dei simboli, vedere [percorsi](symbol-paths.md)dei simboli.

L'esecuzione di questo programma Mostra come viene elaborato il percorso dei simboli. Quando DbgHelp esamina il percorso dei simboli per trovare il file di simboli, chiama ripetutamente [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback) che, a sua volta, Visualizza le stringhe seguenti passate da dbghelp.

``` syntax
d:\load.exe c:\home\dbghelp.dll
DBGHELP: No header for c:\home\dbghelp.dll.  Searching for image on disk
DBGHELP: c:\home\dbghelp.dll - OK
DBGHELP: .\dbghelp.pdb - file not found
DBGHELP: .\dll\dbghelp.pdb - file not found
DBGHELP: .\symbols\dll\dbghelp.pdb - file not found
DBGHELP: .\symbols\dll\dbghelp.pdb - file not found
DBGHELP: cache*c:\symbols\dbghelp.pdb - file not found
DBGHELP: cache*c:\symbols\dll\dbghelp.pdb - file not found
DBGHELP: cache*c:\symbols\symbols\dll\dbghelp.pdb - file not found
DBGHELP: d:\nt.binaries.amd64chk\symbols.pri\dbg\dbghelp.pdb - file not found
DBGHELP: dbghelp - private symbols & lines
         dbghelp.pdb
```

 

 



