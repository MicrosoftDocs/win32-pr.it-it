---
description: Le funzioni temporali incluse nel runtime del linguaggio C usano il \_ tipo Time t per rappresentare il numero di secondi trascorsi dalla mezzanotte del 1 gennaio 1970. Nell'esempio seguente viene convertito un \_ valore Time t in un file time utilizzando la funzione Int32x32To64.
ms.assetid: f626c0b2-a5a1-475d-9a24-64e7b0407278
title: Conversione di un valore time_t in un file Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee866efaed716fb12d2501337236afdb7cf641b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319901"
---
# <a name="converting-a-time_t-value-to-a-file-time"></a><span data-ttu-id="a2390-104">Conversione di un \_ valore Time t in un file Time</span><span class="sxs-lookup"><span data-stu-id="a2390-104">Converting a time\_t Value to a File Time</span></span>

<span data-ttu-id="a2390-105">Le funzioni temporali incluse nel runtime del linguaggio C usano il \_ tipo Time t per rappresentare il numero di secondi trascorsi dalla mezzanotte del 1 gennaio 1970.</span><span class="sxs-lookup"><span data-stu-id="a2390-105">The time functions included in the C run-time use the time\_t type to represent the number of seconds elapsed since midnight, January 1, 1970.</span></span> <span data-ttu-id="a2390-106">Nell'esempio seguente viene convertito un \_ valore Time t in un file time utilizzando la funzione [**Int32x32To64**](/windows/desktop/api/winnt/nf-winnt-int32x32to64) .</span><span class="sxs-lookup"><span data-stu-id="a2390-106">The following example converts a time\_t value to a file time, using the [**Int32x32To64**](/windows/desktop/api/winnt/nf-winnt-int32x32to64) function.</span></span>


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



<span data-ttu-id="a2390-107">Una volta ottenuto un file, è possibile convertire questo valore in ora di sistema utilizzando la funzione [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime) .</span><span class="sxs-lookup"><span data-stu-id="a2390-107">After you have obtained a file time, you can convert this value to system time using the [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime) function.</span></span>

 

 
