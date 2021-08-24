---
description: Il codice seguente illustra come chiamare la funzione SymFromName.
ms.assetid: d3a9d73e-fb77-4be3-a881-c258bcc587fe
title: Recupero di informazioni sui simboli in base al nome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ec0a04ef2cac9dcd8256f8d00ff59b00bec449cdb4b5661566e7087e782cdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076365"
---
# <a name="retrieving-symbol-information-by-name"></a>Recupero di informazioni sui simboli in base al nome

Il codice seguente illustra come chiamare la [**funzione SymFromName.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) Questa funzione inserisce una struttura [**SYMBOL \_ INFO.**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) Poiché la lunghezza del nome è variabile, è necessario specificare un buffer sufficientemente grande da contenere il nome archiviato alla fine della **struttura SYMBOL \_ INFO.** Inoltre, il **membro MaxNameLen** deve essere impostato sul numero di byte riservati per il nome. In questo esempio szSymbolName è un buffer che archivia il nome del simbolo richiesto. Nell'esempio si presuppone che sia stato inizializzato il gestore dei simboli usando il codice in [Inizializzazione del gestore dei simboli](initializing-the-symbol-handler.md).


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



Se un'applicazione ha un nome di modulo o di file di origine e informazioni sul numero di riga, può usare [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) per recuperare un indirizzo di codice virtuale. Questa funzione richiede un puntatore a una [**struttura IMAGEHLP \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) per ricevere l'indirizzo del codice virtuale. Si noti che il gestore dei simboli può recuperare le informazioni sul numero di riga solo quando l'opzione SYMOPT LOAD LINES è impostata usando \_ \_ la funzione [**SymSetOptions.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) Questa opzione deve essere impostata prima di caricare il modulo. Il parametro szModuleName contiene il nome del modulo di origine. è facoltativo e può essere **NULL.** Il parametro szFileName deve contenere il nome del file di origine e il parametro dwLineNumber deve contenere il numero di riga per cui verrà recuperato l'indirizzo virtuale.


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



 

 



