---
description: Nell'esempio di codice assembly x86 seguente viene ottenuto l'ID di sessione di Servizi terminal associato al processo corrente.
ms.assetid: 9fcb35cb-6813-46a5-aa38-e102f1b6b7dc
title: Recupero dell'ID di sessione del processo corrente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac76865bcfe9144e8b95d4642385804aaf1af8fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126618"
---
# <a name="getting-the-session-id-of-the-current-process"></a>Recupero dell'ID di sessione del processo corrente

\[Gli indirizzi di memoria specificati da questo codice di esempio possono cambiare nelle versioni future di Windows. Per assicurarsi che l'applicazione continuerà a funzionare correttamente in futuro, l'applicazione deve chiamare [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) e quindi [**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) anziché il codice di esempio seguente.\]

Nell'esempio di codice assembly x86 seguente viene ottenuto l'ID di sessione di Servizi terminal associato al processo corrente.

``` syntax
mov     eax,fs:[00000018]
mov     eax,[eax+0x30]
mov     eax,[eax+0x1d4]
```

 

 
