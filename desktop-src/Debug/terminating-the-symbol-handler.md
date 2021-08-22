---
description: Il codice seguente pulisce tutta la memoria associata alla gestione dei simboli per il processo specificato, usando SymCleanup.
ms.assetid: 270a1984-9e66-4dd2-accb-d715287f1ec0
title: Terminazione del gestore dei simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af49c26ffe1a80fad3bf7b03fc18699c07e9b025e8b07b5f6bb6c377cde743b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956940"
---
# <a name="terminating-the-symbol-handler"></a>Terminazione del gestore dei simboli

Il codice seguente pulisce tutta la memoria associata alla gestione dei simboli per il processo specificato, [**usando SymCleanup.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup)


```C++
if (SymCleanup(hProcess))
{
    // SymCleanup returned success
}
else
{
    // SymCleanup failed
    DWORD error = GetLastError();
    printf("SymCleanup returned error : %d\n", error);
}
```



 

 



