---
description: Nell'esempio seguente viene chiamata la funzione PdhEnumObjectItems per enumerare le istanze e i contatori degli oggetti processo nel computer locale.
ms.assetid: d7518ba6-a0f1-4985-aa2c-1ca15a0ceb02
title: Enumerazione di oggetti processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 072510f27ba91a3cad3b76cd2f0c1c04e8c9dd10dd0304f8665d12d16283fda4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061189"
---
# <a name="enumerating-process-objects"></a>Enumerazione di oggetti processo

Nell'esempio seguente viene chiamata la funzione [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa) per enumerare le istanze e i contatori degli oggetti processo nel computer locale.


```C++
// This program needs only the essential Windows header files.
#define WIN32_LEAN_AND_MEAN 1

#include <windows.h>
#include <malloc.h>
#include <stdio.h>
#include <pdh.h>
#include <pdhmsg.h>

#pragma comment(lib, "pdh.lib")

CONST PWSTR COUNTER_OBJECT = L"Process";

void main(void)
{
    PDH_STATUS status = ERROR_SUCCESS;
    LPWSTR pwsCounterListBuffer = NULL;
    DWORD dwCounterListSize = 0;
    LPWSTR pwsInstanceListBuffer = NULL;
    DWORD dwInstanceListSize = 0;
    LPWSTR pTemp = NULL;

    // Determine the required buffer size for the data. 
    status = PdhEnumObjectItems(
        NULL,                   // real-time source
        NULL,                   // local machine
        COUNTER_OBJECT,         // object to enumerate
        pwsCounterListBuffer,   // pass NULL and 0
        &dwCounterListSize,     // to get required buffer size
        pwsInstanceListBuffer, 
        &dwInstanceListSize, 
        PERF_DETAIL_WIZARD,     // counter detail level
        0); 

    if (status == PDH_MORE_DATA) 
    {
        // Allocate the buffers and try the call again.
        pwsCounterListBuffer = (LPWSTR)malloc(dwCounterListSize * sizeof(WCHAR));
        pwsInstanceListBuffer = (LPWSTR)malloc(dwInstanceListSize * sizeof(WCHAR));

        if (NULL != pwsCounterListBuffer && NULL != pwsInstanceListBuffer) 
        {
            status = PdhEnumObjectItems(
                NULL,                   // real-time source
                NULL,                   // local machine
                COUNTER_OBJECT,         // object to enumerate
                pwsCounterListBuffer, 
                &dwCounterListSize,
                pwsInstanceListBuffer, 
                &dwInstanceListSize, 
                PERF_DETAIL_WIZARD,     // counter detail level
                0); 
     
            if (status == ERROR_SUCCESS) 
            {
                wprintf(L"Counters that the Process objects defines:\n\n");

                // Walk the counters list. The list can contain one
                // or more null-terminated strings. The list is terminated
                // using two null-terminator characters.
                for (pTemp = pwsCounterListBuffer; *pTemp != 0; pTemp += wcslen(pTemp) + 1) 
                {
                     wprintf(L"%s\n", pTemp);
                }

                wprintf(L"\nInstances of the Process object:\n\n");

                // Walk the instance list. The list can contain one
                // or more null-terminated strings. The list is terminated
                // using two null-terminator characters.
                for (pTemp = pwsInstanceListBuffer; *pTemp != 0; pTemp += wcslen(pTemp) + 1) 
                {
                     wprintf(L"%s\n", pTemp);
                }
            }
            else 
            {
                wprintf(L"Second PdhEnumObjectItems failed with %0x%x.\n", status);
            }
        } 
        else 
        {
            wprintf(L"Unable to allocate buffers.\n");
            status = ERROR_OUTOFMEMORY;
        }
    } 
    else 
    {
        wprintf(L"\nPdhEnumObjectItems failed with 0x%x.\n", status);
    }

    if (pwsCounterListBuffer != NULL) 
        free (pwsCounterListBuffer);

    if (pwsInstanceListBuffer != NULL) 
        free (pwsInstanceListBuffer);
}
```



 

 



