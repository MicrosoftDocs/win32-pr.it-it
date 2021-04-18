---
title: Versioni del sistema operativo
description: Questo tipo di dati DWORD deve avere il tipo di sistema operativo nella parola più ordinata e il numero di versione del sistema operativo nella parola di basso livello. Nella tabella seguente sono elencati i valori possibili per il sistema operativo.
ms.assetid: 318e277b-a797-45a5-87c5-25b91fdf278d
keywords:
- Archiviazione strutturata versioni del sistema operativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd5de916d354a721834b9a10651c36d3bf389e28
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299986"
---
# <a name="operating-system-versions"></a>Versioni del sistema operativo

Questo tipo di dati **DWORD** deve avere il tipo di sistema operativo nella parola più ordinata e il numero di versione del sistema operativo nella parola di basso livello. Nella tabella seguente sono elencati i valori possibili per il sistema operativo.



| Sistema operativo       | Valore  |
|------------------------|--------|
| Windows a 32 bit (Win32) | 0x0002 |
| Macintosh              | 0x0001 |
| Windows a 16 bit (Win16) | 0x0000 |



 

Per i sistemi operativi Microsoft Windows, la versione del sistema operativo è la parola di ordine inferiore restituita dalla funzione [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion) . Per Microsoft Windows, il codice di esempio seguente imposta correttamente la versione del sistema operativo di origine.

``` syntax
#ifdef WIN32 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 2 ) ; 
#else 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 0 ) ; 
#endif
```

 

 