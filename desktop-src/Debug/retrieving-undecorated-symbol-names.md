---
description: Il codice seguente illustra come recuperare un nome di simbolo non decorato da un nome di simbolo usando UnDecorateSymbolName.
ms.assetid: fcb0591a-dac3-45eb-b4c0-4a35c42450e5
title: Recupero dei nomi di simboli non decorati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b0f21c884a0a58f0546ef275f2f3096abe2c50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305238"
---
# <a name="retrieving-undecorated-symbol-names"></a>Recupero dei nomi di simboli non decorati

Il codice seguente illustra come recuperare un nome di simbolo non decorato da un nome di simbolo usando [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname). Il nome decorato viene archiviato in `szName` . Nell'esempio si presuppone che sia stato inizializzato il gestore di simboli utilizzando il codice nell' [inizializzazione del gestore di simboli](initializing-the-symbol-handler.md).


```C++
if (UnDecorateSymbolName(szName, szUndName, sizeof(szUndName), UNDNAME_COMPLETE))
{
    // UnDecorateSymbolName returned success
    printf ("Symbol : %s\n", szUndName);
}
else
{
    // UnDecorateSymbolName failed
    DWORD error = GetLastError();
    printf("UnDecorateSymbolName returned error %d\n", error);
}
```



 

 



