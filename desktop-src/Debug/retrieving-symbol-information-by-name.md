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
# <a name="retrieving-symbol-information-by-name"></a>Recupero delle informazioni sui simboli per nome

Nel codice seguente viene illustrato come chiamare la funzione [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) . Questa funzione compila una struttura di [**\_ informazioni sui simboli**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) . Poiché il nome è di lunghezza variabile, è necessario specificare un buffer sufficientemente grande da mantenere il nome archiviato alla fine della struttura delle informazioni sui **simboli \_** . Inoltre, il membro **MaxNameLen** deve essere impostato sul numero di byte riservati per il nome. In questo esempio, szSymbolName è un buffer che archivia il nome del simbolo richiesto. Nell'esempio si presuppone che sia stato inizializzato il gestore di simboli utilizzando il codice nell' [inizializzazione del gestore di simboli](initializing-the-symbol-handler.md).


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



Se un'applicazione dispone di un modulo o di un nome di file di origine e di informazioni sul numero di riga, può utilizzare [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) per recuperare un indirizzo di codice virtuale. Questa funzione richiede un puntatore a una struttura [**Imagehlp \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) per ricevere l'indirizzo del codice virtuale. Si noti che il gestore di simboli può recuperare informazioni sul numero di riga solo quando \_ \_ l'opzione SYMOPT Load Lines viene impostata tramite la funzione [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) . È necessario impostare questa opzione prima di caricare il modulo. Il parametro szModuleName contiene il nome del modulo di origine; è facoltativo e può essere **null**. Il parametro szFileName deve contenere il nome del file di origine e il parametro dwLineNumber deve contenere il numero di riga per il quale verrà recuperato l'indirizzo virtuale.


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



 

 



