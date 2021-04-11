---
description: Nel codice seguente viene illustrato come chiamare la funzione SymFromName.
ms.assetid: d3a9d73e-fb77-4be3-a881-c258bcc587fe
title: Recupero delle informazioni sui simboli per nome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f5f4477be4f494383c7d9c1ca462f3beb69690
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126429"
---
# <a name="retrieving-symbol-information-by-name"></a><span data-ttu-id="768c1-103">Recupero delle informazioni sui simboli per nome</span><span class="sxs-lookup"><span data-stu-id="768c1-103">Retrieving Symbol Information by Name</span></span>

<span data-ttu-id="768c1-104">Nel codice seguente viene illustrato come chiamare la funzione [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) .</span><span class="sxs-lookup"><span data-stu-id="768c1-104">The following code demonstrates how to call the [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) function.</span></span> <span data-ttu-id="768c1-105">Questa funzione compila una struttura di [**\_ informazioni sui simboli**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) .</span><span class="sxs-lookup"><span data-stu-id="768c1-105">This function fills in a [**SYMBOL\_INFO**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) structure.</span></span> <span data-ttu-id="768c1-106">Poiché il nome è di lunghezza variabile, è necessario specificare un buffer sufficientemente grande da mantenere il nome archiviato alla fine della struttura delle informazioni sui **simboli \_** .</span><span class="sxs-lookup"><span data-stu-id="768c1-106">Because the name is variable in length, you must supply a buffer that is large enough to hold the name stored at the end of the **SYMBOL\_INFO** structure.</span></span> <span data-ttu-id="768c1-107">Inoltre, il membro **MaxNameLen** deve essere impostato sul numero di byte riservati per il nome.</span><span class="sxs-lookup"><span data-stu-id="768c1-107">Also, the **MaxNameLen** member must be set to the number of bytes reserved for the name.</span></span> <span data-ttu-id="768c1-108">In questo esempio, szSymbolName è un buffer che archivia il nome del simbolo richiesto.</span><span class="sxs-lookup"><span data-stu-id="768c1-108">In this example, szSymbolName is a buffer that stores the name of the requested symbol.</span></span> <span data-ttu-id="768c1-109">Nell'esempio si presuppone che sia stato inizializzato il gestore di simboli utilizzando il codice nell' [inizializzazione del gestore di simboli](initializing-the-symbol-handler.md).</span><span class="sxs-lookup"><span data-stu-id="768c1-109">The example assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


```C++
TCHAR szSymbolName[MAX_SYM_NAME];
ULONG64 buffer[(sizeof(SYMBOL_INFO) +
    MAX_SYM_NAME * sizeof(TCHAR) +
    sizeof(ULONG64) - 1) /
    sizeof(ULONG64)];
PSYMBOL_INFO pSymbol = (PSYMBOL_INFO)buffer;

_tcscpy_s(szSymbolName, MAX_SYM_NAME, TEXT("WinMain"));
pSymbol->SizeOfStruct = sizeof(SYMBOL_INFO);
pSymbol->MaxNameLen = MAX_SYM_NAME;

if (SymFromName(hProcess, szSymbolName, pSymbol))
{
    // SymFromName returned success
}
else
{
    // SymFromName failed
    DWORD error = GetLastError();
    _tprintf(TEXT("SymFromName returned error : %d\n"), error);
}
```



<span data-ttu-id="768c1-110">Se un'applicazione dispone di un modulo o di un nome di file di origine e di informazioni sul numero di riga, può utilizzare [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) per recuperare un indirizzo di codice virtuale.</span><span class="sxs-lookup"><span data-stu-id="768c1-110">If an application has a module or source file name as well as line number information, it can use [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) to retrieve a virtual code address.</span></span> <span data-ttu-id="768c1-111">Questa funzione richiede un puntatore a una struttura [**Imagehlp \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) per ricevere l'indirizzo del codice virtuale.</span><span class="sxs-lookup"><span data-stu-id="768c1-111">This function requires a pointer to an [**IMAGEHLP\_LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) structure to receive the virtual code address.</span></span> <span data-ttu-id="768c1-112">Si noti che il gestore di simboli può recuperare informazioni sul numero di riga solo quando \_ \_ l'opzione SYMOPT Load Lines viene impostata tramite la funzione [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) .</span><span class="sxs-lookup"><span data-stu-id="768c1-112">Note that the symbol handler can retrieve line number information only when SYMOPT\_LOAD\_LINES option is set using the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function.</span></span> <span data-ttu-id="768c1-113">È necessario impostare questa opzione prima di caricare il modulo.</span><span class="sxs-lookup"><span data-stu-id="768c1-113">This option must be set before loading the module.</span></span> <span data-ttu-id="768c1-114">Il parametro szModuleName contiene il nome del modulo di origine; è facoltativo e può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="768c1-114">The szModuleName parameter contains the source module name; it is optional and can be **NULL**.</span></span> <span data-ttu-id="768c1-115">Il parametro szFileName deve contenere il nome del file di origine e il parametro dwLineNumber deve contenere il numero di riga per il quale verrà recuperato l'indirizzo virtuale.</span><span class="sxs-lookup"><span data-stu-id="768c1-115">The szFileName parameter should contain the source file name, and dwLineNumber parameter should contain the line number for which the virtual address will be retrieved.</span></span>


```C++
TCHAR  szModuleName[MAX_PATH];
TCHAR  szFileName[MAX_PATH];
DWORD  dwLineNumber;
LONG   lDisplacement;
IMAGEHLP_LINE64 line;

SymSetOptions(SYMOPT_LOAD_LINES);

line.SizeOfStruct = sizeof(IMAGEHLP_LINE64);
_tcscpy_s(szModuleName, MAX_PATH, TEXT("MyApp"));
_tcscpy_s(szFileName, MAX_PATH, TEXT("main.c"));
dwLineNumber = 248;

if (SymGetLineFromName64(hProcess, szModuleName, szFileName,
    dwLineNumber, &lDisplacement, &line))
{
    // SymGetLineFromName64 returned success
}
else
{
    // SymGetLineFromName64 failed
    DWORD error = GetLastError();
    _tprintf(TEXT("SymGetLineFromName64 returned error : %d\n"), error);
}
```



 

 



