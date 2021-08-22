---
description: Il codice seguente illustra come recuperare un nome di simbolo non dichiarato da un nome di simbolo usando UnDecorateSymbolName.
ms.assetid: fcb0591a-dac3-45eb-b4c0-4a35c42450e5
title: Recupero di nomi di simboli nondecorati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f18a1cbdf51c64134489850343b466e49d9867fab483699a719997c3be9b5798
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076345"
---
# <a name="retrieving-undecorated-symbol-names"></a>Recupero di nomi di simboli nondecorati

Il codice seguente illustra come recuperare un nome di simbolo non dichiarato da un nome di simbolo usando [**UnDecorateSymbolName.**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) Il nome decorato viene archiviato in `szName` . Nell'esempio si presuppone che sia stato inizializzato il gestore dei simboli usando il codice in [Inizializzazione del gestore dei simboli](initializing-the-symbol-handler.md).


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



 

 



