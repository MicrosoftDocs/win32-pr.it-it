---
description: L'esempio di codice assembly x86 seguente ottiene l'ID sessione di Servizi terminal associato al processo corrente.
ms.assetid: 9fcb35cb-6813-46a5-aa38-e102f1b6b7dc
title: Recupero dell'ID sessione del processo corrente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4326020f145c98544132703611fbd783edac9ae9eb89a5c69f44b67dc997ca30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955980"
---
# <a name="getting-the-session-id-of-the-current-process"></a>Recupero dell'ID sessione del processo corrente

\[Gli indirizzi di memoria specificati da questo codice di esempio possono cambiare nelle versioni future Windows. Per garantire che l'applicazione continui a essere eseguita correttamente in futuro, l'applicazione deve chiamare [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) e [**quindi ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) anziché il codice di esempio seguente.\]

L'esempio di codice assembly x86 seguente ottiene l'ID sessione di Servizi terminal associato al processo corrente.

``` syntax
mov     eax,fs:[00000018]
mov     eax,[eax+0x30]
mov     eax,[eax+0x1d4]
```

 

 
