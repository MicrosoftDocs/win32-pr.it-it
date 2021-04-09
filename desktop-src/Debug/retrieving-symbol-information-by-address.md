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
# <a name="retrieving-symbol-information-by-address"></a>Recupero delle informazioni sui simboli per indirizzo

Nel codice seguente viene illustrato come chiamare la funzione [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) . Questa funzione compila una struttura di [**\_ informazioni sui simboli**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) . Poiché il nome è di lunghezza variabile, è necessario specificare un buffer sufficientemente grande da mantenere il nome archiviato alla fine della struttura delle informazioni sui **simboli \_** . Inoltre, il membro **MaxNameLen** deve essere impostato sul numero di byte riservati per il nome. In questo esempio, *dwAddress* è l'indirizzo di cui eseguire il mapping a un simbolo. La funzione **SymFromAddr** archivia un offset all'inizio del simbolo nell'indirizzo in *dwDisplacement*. Nell'esempio si presuppone che sia stato inizializzato il gestore di simboli utilizzando il codice nell' [inizializzazione del gestore di simboli](initializing-the-symbol-handler.md).


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



Per recuperare il numero di riga del codice sorgente per un indirizzo specificato, un'applicazione può usare [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr). Questa funzione richiede un puntatore a una struttura [**Imagehlp \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) per ricevere il nome del file di origine e il numero di riga corrispondente a un indirizzo di codice specificato. Si noti che il gestore di simboli può recuperare le informazioni sul numero di riga solo quando le **\_ \_ linee di caricamento SYMOPT** vengono impostate tramite la funzione [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) . È necessario impostare questa opzione prima di caricare il modulo. Il parametro dwAddress contiene l'indirizzo del codice per il quale verrà individuato il nome del file di origine e il numero di riga.


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



 

 



