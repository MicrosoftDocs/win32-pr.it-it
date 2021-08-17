---
description: Le funzioni di tempo incluse nel run-time C usano il tipo time t per rappresentare il numero di secondi trascorsi dalla mezzanotte \_ del 1° gennaio 1970. L'esempio seguente converte un valore \_ time t in un'ora del file usando la funzione Int32x32To64.
ms.assetid: f626c0b2-a5a1-475d-9a24-64e7b0407278
title: Conversione di un time_t in un'ora del file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30fc7161e55bb235690f5c7d5fe0f4cd575bd7c902d5357606290def0509f6b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764512"
---
# <a name="converting-a-time_t-value-to-a-file-time"></a>Conversione di un valore \_ time t in un'ora del file

Le funzioni di tempo incluse nel run-time C usano il tipo time t per rappresentare il numero di secondi trascorsi dalla mezzanotte \_ del 1° gennaio 1970. L'esempio seguente converte un valore \_ time t in un'ora del file usando la [**funzione Int32x32To64.**](/windows/desktop/api/winnt/nf-winnt-int32x32to64)


```C++
#include <windows.h>
#include <time.h>

void TimetToFileTime( time_t t, LPFILETIME pft )
{
    LONGLONG ll = Int32x32To64(t, 10000000) + 116444736000000000;
    pft->dwLowDateTime = (DWORD) ll;
    pft->dwHighDateTime = ll >>32;
}
```



Dopo aver ottenuto un'ora del file, è possibile convertire questo valore in ora di sistema usando la [**funzione FileTimeToSystemTime.**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime)

 

 
