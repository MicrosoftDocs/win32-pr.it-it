---
description: Il codice seguente illustra come chiamare la funzione SymFromAddr.
ms.assetid: 63dfadea-b0c4-4050-add8-d1f3aef7a495
title: Recupero di informazioni sui simboli in base all'indirizzo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6484327117e66826402dc97abb09f58813e528599c69bd97054528f5cfe89aba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076385"
---
# <a name="retrieving-symbol-information-by-address"></a>Recupero di informazioni sui simboli in base all'indirizzo

Il codice seguente illustra come chiamare la [**funzione SymFromAddr.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) Questa funzione inserisce una struttura [**SYMBOL \_ INFO.**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) Poiché la lunghezza del nome è variabile, è necessario specificare un buffer sufficientemente grande da contenere il nome archiviato alla fine della **struttura SYMBOL \_ INFO.** Inoltre, il **membro MaxNameLen** deve essere impostato sul numero di byte riservati per il nome. In questo esempio *dwAddress è* l'indirizzo di cui eseguire il mapping a un simbolo. La **funzione SymFromAddr** archivierà un offset all'inizio del simbolo per l'indirizzo in *dwDisplacement*. Nell'esempio si presuppone che sia stato inizializzato il gestore dei simboli usando il codice in [Inizializzazione del gestore dei simboli](initializing-the-symbol-handler.md).


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



Per recuperare il numero di riga del codice sorgente per un indirizzo specificato, un'applicazione può [**usare SymGetLineFromAddr64.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) Questa funzione richiede un puntatore a una struttura [**IMAGEHLP \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) per ricevere il nome del file di origine e il numero di riga corrispondenti a un indirizzo di codice specificato. Si noti che il gestore dei simboli può recuperare le informazioni sul numero di riga solo quando **SYMOPT \_ LOAD \_ LINES** è impostato usando la [**funzione SymSetOptions.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) Questa opzione deve essere impostata prima di caricare il modulo. Il parametro dwAddress contiene l'indirizzo di codice per il quale verranno individuati il nome del file di origine e il numero di riga.


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



 

 



