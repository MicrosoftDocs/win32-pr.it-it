---
description: La definizione Dinl.h seguente è l'indirizzo di memoria statica dell'ID sessione della console di Servizi terminal attivo. Questo ID sessione della console attiva non è definito nelle versioni del sistema operativo Microsoft Windows precedenti a Windows XP.
ms.assetid: f3022ab8-60ea-490b-a87d-cc1afc99d26f
title: Recupero dell'ID sessione della console attiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f7b23669240f0cd109a48f454ee6f6329f6839221a1677e81b75712430cb42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002301"
---
# <a name="getting-the-active-console-session-id"></a>Recupero dell'ID sessione della console attiva

La definizione Dinl.h seguente è l'indirizzo di memoria statica dell'ID sessione della console di Servizi terminal attivo. Questo ID sessione della console attiva non è definito nelle versioni del sistema operativo Microsoft Windows precedenti a Windows XP.

> [!Note]  
> Questa definizione può cambiare nelle versioni future di Windows. Per garantire che l'applicazione continui a essere eseguita correttamente in futuro, l'applicazione deve [**chiamare WTSGetActiveConsoleSessionId**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid).

 

``` syntax
#define INTERNAL_TS_ACTIVE_CONSOLE_ID    
        (*((volatile ULONG*)(0x7ffe02d8)))
```

 

 
