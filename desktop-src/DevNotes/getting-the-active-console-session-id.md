---
description: La definizione di Winternl. h seguente è l'indirizzo di memoria statica dell'ID di sessione della console Servizi terminal attiva. Questo ID di sessione della console attiva non è definito nelle versioni del sistema operativo Microsoft Windows precedenti a Windows XP.
ms.assetid: f3022ab8-60ea-490b-a87d-cc1afc99d26f
title: Recupero dell'ID di sessione della console attiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936db3f8038348864fc90fc55eeb4287a67c45d6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877641"
---
# <a name="getting-the-active-console-session-id"></a>Recupero dell'ID di sessione della console attiva

La definizione di Winternl. h seguente è l'indirizzo di memoria statica dell'ID di sessione della console Servizi terminal attiva. Questo ID di sessione della console attiva non è definito nelle versioni del sistema operativo Microsoft Windows precedenti a Windows XP.

> [!Note]  
> Questa definizione può cambiare nelle versioni future di Windows. Per assicurarsi che l'applicazione continuerà a funzionare correttamente in futuro, l'applicazione deve chiamare [**WTSGetActiveConsoleSessionId**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid).

 

``` syntax
#define INTERNAL_TS_ACTIVE_CONSOLE_ID    
        (*((volatile ULONG*)(0x7ffe02d8)))
```

 

 
