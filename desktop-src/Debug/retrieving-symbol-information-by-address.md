---
description: Nel codice seguente viene illustrato come chiamare la funzione SymFromAddr.
ms.assetid: 63dfadea-b0c4-4050-add8-d1f3aef7a495
title: Recupero delle informazioni sui simboli per indirizzo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ad9d2879dbfd5820c4aa6c2e7563a1575ebe1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126432"
---
# <a name="retrieving-symbol-information-by-address"></a><span data-ttu-id="d1a73-103">Recupero delle informazioni sui simboli per indirizzo</span><span class="sxs-lookup"><span data-stu-id="d1a73-103">Retrieving Symbol Information by Address</span></span>

<span data-ttu-id="d1a73-104">Nel codice seguente viene illustrato come chiamare la funzione [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) .</span><span class="sxs-lookup"><span data-stu-id="d1a73-104">The following code demonstrates how to call the [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) function.</span></span> <span data-ttu-id="d1a73-105">Questa funzione compila una struttura di [**\_ informazioni sui simboli**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) .</span><span class="sxs-lookup"><span data-stu-id="d1a73-105">This function fills in a [**SYMBOL\_INFO**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) structure.</span></span> <span data-ttu-id="d1a73-106">Poiché il nome è di lunghezza variabile, è necessario specificare un buffer sufficientemente grande da mantenere il nome archiviato alla fine della struttura delle informazioni sui **simboli \_** .</span><span class="sxs-lookup"><span data-stu-id="d1a73-106">Because the name is variable in length, you must supply a buffer that is large enough to hold the name stored at the end of the **SYMBOL\_INFO** structure.</span></span> <span data-ttu-id="d1a73-107">Inoltre, il membro **MaxNameLen** deve essere impostato sul numero di byte riservati per il nome.</span><span class="sxs-lookup"><span data-stu-id="d1a73-107">Also, the **MaxNameLen** member must be set to the number of bytes reserved for the name.</span></span> <span data-ttu-id="d1a73-108">In questo esempio, *dwAddress* è l'indirizzo di cui eseguire il mapping a un simbolo.</span><span class="sxs-lookup"><span data-stu-id="d1a73-108">In this example, *dwAddress* is the address to be mapped to a symbol.</span></span> <span data-ttu-id="d1a73-109">La funzione **SymFromAddr** archivia un offset all'inizio del simbolo nell'indirizzo in *dwDisplacement*.</span><span class="sxs-lookup"><span data-stu-id="d1a73-109">The **SymFromAddr** function will store an offset to the beginning of the symbol to the address in *dwDisplacement*.</span></span> <span data-ttu-id="d1a73-110">Nell'esempio si presuppone che sia stato inizializzato il gestore di simboli utilizzando il codice nell' [inizializzazione del gestore di simboli](initializing-the-symbol-handler.md).</span><span class="sxs-lookup"><span data-stu-id="d1a73-110">The example assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


```C++
DWORD64  dwDisplacement = 0;
DWORD64  dwAddress = SOME_ADDRESS;

char buffer[sizeof(SYMBOL_INFO) + MAX_SYM_NAME * sizeof(TCHAR)];
PSYMBOL_INFO pSymbol = (PSYMBOL_INFO)buffer;

pSymbol->SizeOfStruct = sizeof(SYMBOL_INFO);
pSymbol->MaxNameLen = MAX_SYM_NAME;

if (SymFromAddr(hProcess, dwAddress, &dwDisplacement, pSymbol))
{
    // SymFromAddr returned success
}
else
{
    // SymFromAddr failed
    DWORD error = GetLastError();
    printf("SymFromAddr returned error : %d\n", error);
}
```



<span data-ttu-id="d1a73-111">Per recuperare il numero di riga del codice sorgente per un indirizzo specificato, un'applicazione può usare [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr).</span><span class="sxs-lookup"><span data-stu-id="d1a73-111">To retrieve the source code line number for a specified address, an application can use [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr).</span></span> <span data-ttu-id="d1a73-112">Questa funzione richiede un puntatore a una struttura [**Imagehlp \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) per ricevere il nome del file di origine e il numero di riga corrispondente a un indirizzo di codice specificato.</span><span class="sxs-lookup"><span data-stu-id="d1a73-112">This function requires a pointer to an [**IMAGEHLP\_LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) structure to receive the source file name and line number corresponding to a specified code address.</span></span> <span data-ttu-id="d1a73-113">Si noti che il gestore di simboli può recuperare le informazioni sul numero di riga solo quando le **\_ \_ linee di caricamento SYMOPT** vengono impostate tramite la funzione [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) .</span><span class="sxs-lookup"><span data-stu-id="d1a73-113">Note that the symbol handler can retrieve line number information only when **SYMOPT\_LOAD\_LINES** is set using the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function.</span></span> <span data-ttu-id="d1a73-114">È necessario impostare questa opzione prima di caricare il modulo.</span><span class="sxs-lookup"><span data-stu-id="d1a73-114">This option must be set before loading the module.</span></span> <span data-ttu-id="d1a73-115">Il parametro dwAddress contiene l'indirizzo del codice per il quale verrà individuato il nome del file di origine e il numero di riga.</span><span class="sxs-lookup"><span data-stu-id="d1a73-115">The dwAddress parameter contains the code address for which the source file name and line number will be located.</span></span>


```C++
DWORD64  dwAddress;
DWORD  dwDisplacement;
IMAGEHLP_LINE64 line;

SymSetOptions(SYMOPT_LOAD_LINES);

line.SizeOfStruct = sizeof(IMAGEHLP_LINE64);
dwAddress = 0x1000000; // Address you want to check on.

if (SymGetLineFromAddr64(hProcess, dwAddress, &dwDisplacement, &line))
{
    // SymGetLineFromAddr64 returned success
}
else
{
    // SymGetLineFromAddr64 failed
    DWORD error = GetLastError();
    _tprintf(TEXT("SymGetLineFromAddr64 returned error : %d\n"), error);
}
```



 

 



