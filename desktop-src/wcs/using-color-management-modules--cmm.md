---
title: Uso di moduli di gestione colori (CMM)
description: I moduli di gestione colori (CMM) sono moduli di codice WCS che usano le informazioni nei profili di dispositivo per eseguire la conversione dei colori e il mapping dei colori.
ms.assetid: df119e1a-b6f5-40a3-8852-8a57b21483d0
keywords:
- Windows Color System (WCS), modulo di gestione colori (CMM)
- WCS (sistema di colori Windows), modulo Gestione colori (CMM)
- Gestione colori immagine, modulo di gestione colori (CMM)
- gestione dei colori, modulo di gestione colori (CMM)
- colori, modulo di gestione colori (CMM)
- Modulo di gestione colori (CMM)
- CMM (modulo di gestione colori)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518558305639f0699358f22fb3544698741cfedf
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/02/2021
ms.locfileid: "106320177"
---
# <a name="using-color-management-modules-cmm"></a>Uso di moduli di gestione colori (CMM)

I moduli di gestione colori (CMM) sono moduli di codice WCS che usano le informazioni nei profili di dispositivo per eseguire la conversione dei colori e il mapping dei colori. Gli sviluppatori di applicazioni non devono implementare CMM. Microsoft fornisce il CMM predefinito. Tuttavia, se si scrive software che richiede l'uso di algoritmi di conversione colori e di mapping dei colori specializzati, è possibile crearne uno.

> [!Note]  
> I punti di ingresso CMM *non* sono funzioni API e non devono essere chiamati dalle applicazioni.

 

Quando CMM sono installati, il programma di installazione li registra nel registro di sistema di Windows. Le applicazioni possono enumerare il CMM registrato e selezionarne uno usando la funzione [**SelectCMM**](/windows/win32/api/icm/nf-icm-selectcmm) . Nell'applicazione di esempio seguente viene illustrato come enumerare tutti i CMM registrati.


```C++
#include <stdio.h>
#include <stdlib.h>
#include <stddef.h>
#include <string.h>
#include <mbstring.h>
#include <windows.h>
#include <icm.h>

#ifdef WINDOWS_98
TCHAR  gszICMatcher[] = __TEXT(
  "SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\ICM\\ICMatchers");
#else
TCHAR  gszICMatcher[] = __TEXT(
  "SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\ICM\\ICMatchers");
#endif

_CRTAPI1 main (int argc, char *argv[])
{
    DWORD dwNumCMM = 0;

    HANDLE hkCMM;
    DWORD dwErr = RegCreateKey(HKEY_LOCAL_MACHINE,
                 gszICMatcher, &amp;hkCMM);
    DWORD dwMaxName, dwMaxValue;
    DWORD dwInfoErr = RegQueryInfoKey(&amp;hkCMM, NULL, NULL,
                                NULL, NULL, NULL, NULL, NULL,
                                &amp;dwMaxName, &amp;dwMaxValue,
                                NULL, NULL);
    TCHAR chCMM[dwMaxName];
    ULONG cjCMM = sizeof(chCMM)/sizeof(chCMM[0]);
    DWORD dwType;
    TCHAR chCMMFile[dwMaxValue];
    ULONG cjCMMFile = sizeof(chCMMFile)/sizeof(chCMMFile[0]);

    if (dwErr != ERROR_SUCCESS)
    {
        printf("Could not open ICMatcher registry key: %d\n", dwErr);
    }

    if (dwErr == ERROR_SUCCESS)
    {
        while (RegEnumValue(
                   hkCMM,dwNumCMM,chCMM,
                   &amp;cjCMM,NULL,&amp;dwType,
                   chCMMFile,&amp;cjCMMFile) == ERROR_SUCCESS)
        {
            if (dwType == REG_SZ)
            {
                printf("%d: %-80s - %-80s\n",dwNumCMM,chCMM,chCMMFile);
            }
            else
            {
                printf("%d: error\n");
            }

            dwNumCMM++;
            cjCMM = sizeof(chCMM);
            cjCMMFile = sizeof(chCMMFile);
        }
    }

    RegCloseKey(hkCMM);
}
```



 

 




