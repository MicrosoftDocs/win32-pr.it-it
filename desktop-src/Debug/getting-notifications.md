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
# <a name="getting-notifications"></a><span data-ttu-id="2024e-103">Ricezione di notifiche</span><span class="sxs-lookup"><span data-stu-id="2024e-103">Getting Notifications</span></span>

<span data-ttu-id="2024e-104">Nel codice seguente viene illustrato come ottenere e segnalare informazioni dettagliate sullo stato dal gestore di simboli per la ricerca e il caricamento dei moduli e dei file di simboli corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="2024e-104">The following code shows how to obtain and report verbose status information from the symbol handler about searching for and loading of modules and the corresponding symbol files.</span></span>

<span data-ttu-id="2024e-105">Molti esperti del debugger WinDbg possono ricordare un comando denominato "! sym noisy".</span><span class="sxs-lookup"><span data-stu-id="2024e-105">Many familiar with the WinDbg debugger may remember a command called "!sym noisy".</span></span> <span data-ttu-id="2024e-106">Questo comando viene usato dall'utente per determinare il motivo per cui WinDbg è o non è in grado di caricare i file di simboli.</span><span class="sxs-lookup"><span data-stu-id="2024e-106">This command is used by the user to determine why WinDbg is or is not able to load symbol files.</span></span> <span data-ttu-id="2024e-107">Mostra un elenco dettagliato di tutti gli elementi tentati dal gestore di simboli.</span><span class="sxs-lookup"><span data-stu-id="2024e-107">It shows a verbose listing of everything the symbol handler tries.</span></span>

<span data-ttu-id="2024e-108">Questo stesso elenco è disponibile anche per tutti gli utenti che sviluppano un client nel gestore di simboli DbgHelp.</span><span class="sxs-lookup"><span data-stu-id="2024e-108">This same listing is also available to anyone developing a client to the DbgHelp symbol handler.</span></span>

<span data-ttu-id="2024e-109">Prima di tutto, chiamare [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) con **SYMOPT \_ debug**.</span><span class="sxs-lookup"><span data-stu-id="2024e-109">First, call [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) with **SYMOPT\_DEBUG**.</span></span> <span data-ttu-id="2024e-110">Questo fa in modo che DbgHelp accenda le notifiche di debug.</span><span class="sxs-lookup"><span data-stu-id="2024e-110">This causes DbgHelp to turn on debug notifications.</span></span>

<span data-ttu-id="2024e-111">Dopo la chiamata a [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize), utilizzare [**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback) per registrare una funzione di callback che dbghelp chiamerà ogni volta che si verifica un evento interessante.</span><span class="sxs-lookup"><span data-stu-id="2024e-111">After calling [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize), use [**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback) to register a callback function that DbgHelp will call whenever an interesting event occurs.</span></span> <span data-ttu-id="2024e-112">In questo esempio, la funzione di callback è denominata [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback).</span><span class="sxs-lookup"><span data-stu-id="2024e-112">In this example, the callback function is called [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback).</span></span> <span data-ttu-id="2024e-113">Alle funzioni di callback dei simboli viene passata un'ampia gamma di codici di azione che è possibile gestire in base al tipo.</span><span class="sxs-lookup"><span data-stu-id="2024e-113">Symbol callback functions are passed an assortment of action codes that they can handle according to type.</span></span> <span data-ttu-id="2024e-114">In questo esempio viene gestito solo il codice dell'azione dell' **\_ evento CBA** .</span><span class="sxs-lookup"><span data-stu-id="2024e-114">In this example, we are handling only the **CBA\_EVENT** action code.</span></span> <span data-ttu-id="2024e-115">Questa funzione passa una stringa che contiene informazioni dettagliate su un evento che si è verificato nel processo di caricamento di un simbolo.</span><span class="sxs-lookup"><span data-stu-id="2024e-115">This function passes a string containing verbose information about an event that occurred in the process of loading a symbol.</span></span> <span data-ttu-id="2024e-116">Questo evento potrebbe essere un tentativo di leggere i dati all'interno di un'immagine eseguibile nella posizione corretta di un file di simboli.</span><span class="sxs-lookup"><span data-stu-id="2024e-116">This event could be anything from an attempt to read the data within an executable image to the successful location of a symbol file.</span></span> <span data-ttu-id="2024e-117">**SymRegisterCallbackProc64** Visualizza tale stringa e restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="2024e-117">**SymRegisterCallbackProc64** displays that string and returns **TRUE**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2024e-118">Assicurarsi di restituire **false** a ogni codice di azione che non si gestisce. in caso contrario, è possibile che si verifichi un comportamento non definito.</span><span class="sxs-lookup"><span data-stu-id="2024e-118">Make sure you return **FALSE** to every action code that you do not handle, otherwise you may experience undefined behavior.</span></span> <span data-ttu-id="2024e-119">Vedere [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback) per un elenco di tutti i codici di azione e le relative implicazioni.</span><span class="sxs-lookup"><span data-stu-id="2024e-119">Refer to [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback) for a list of all the action codes and their implications.</span></span>

 

<span data-ttu-id="2024e-120">Ora che il callback è registrato, è possibile caricare il modulo specificato nella riga di comando chiamando [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex).</span><span class="sxs-lookup"><span data-stu-id="2024e-120">Now that the callback is registered, it is time to load the module specified on the command line by calling [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex).</span></span>

<span data-ttu-id="2024e-121">Infine, chiamare [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) prima di uscire.</span><span class="sxs-lookup"><span data-stu-id="2024e-121">Lastly, call [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) before exiting.</span></span>


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



<span data-ttu-id="2024e-122">Se si specifica **null** come secondo parametro di [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) , il gestore di simboli deve utilizzare il percorso di ricerca predefinito per individuare i file di simboli.</span><span class="sxs-lookup"><span data-stu-id="2024e-122">Specifying **NULL** as the second parameter of [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) indicates that the symbol handler should use the default search path to locate symbol files.</span></span> <span data-ttu-id="2024e-123">Per informazioni dettagliate sul modo in cui il gestore di simboli individua i file di simboli o su come un'applicazione può specificare un percorso di ricerca dei simboli, vedere [percorsi](symbol-paths.md)dei simboli.</span><span class="sxs-lookup"><span data-stu-id="2024e-123">For detailed information on how the symbol handler locates symbol files or how an application can specify a symbol search path, see [Symbol Paths](symbol-paths.md).</span></span>

<span data-ttu-id="2024e-124">L'esecuzione di questo programma Mostra come viene elaborato il percorso dei simboli.</span><span class="sxs-lookup"><span data-stu-id="2024e-124">Running this program shows how the symbol path is processed.</span></span> <span data-ttu-id="2024e-125">Quando DbgHelp esamina il percorso dei simboli per trovare il file di simboli, chiama ripetutamente [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback) che, a sua volta, Visualizza le stringhe seguenti passate da dbghelp.</span><span class="sxs-lookup"><span data-stu-id="2024e-125">As DbgHelp looks through the symbol path to find the symbol file, it repeatedly calls [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback) which, in turn, displays the following strings being passed by DbgHelp.</span></span>

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

 

 



