---
title: Uso dei moduli di gestione dei colori (CMM)
description: I moduli di gestione dei colori sono moduli di codice WCS che usano le informazioni nei profili di dispositivo per eseguire la conversione dei colori e il mapping dei colori.
ms.assetid: df119e1a-b6f5-40a3-8852-8a57b21483d0
keywords:
- Windows Color System (WCS),Color Management Module (CMM)
- WCS (Windows Color System),Color Management Module (CMM)
- gestione del colore delle immagini, modulo di gestione dei colori (CMM)
- gestione dei colori, modulo di gestione dei colori (CMM)
- colors,Color Management Module (CMM)
- Modulo di gestione dei colori (CMM)
- CMM (modulo gestione colori)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b12a087bfc972ffcbd7f9fb083a9d73d669f134
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386900"
---
# <a name="using-color-management-modules-cmm"></a>Uso dei moduli di gestione dei colori (CMM)

I moduli di gestione dei colori sono moduli di codice WCS che usano le informazioni nei profili di dispositivo per eseguire la conversione dei colori e il mapping dei colori. Gli sviluppatori di applicazioni non devono implementare ICM. Microsoft fornisce il CMM predefinito. Tuttavia, se si scrive un software che richiede l'uso di algoritmi specializzati di conversione dei colori e mapping dei colori, è possibile crearne uno.

> [!Note]  
> I punti di ingresso CMM *non sono* funzioni API e non devono essere chiamati dalle applicazioni.

 

Quando vengono installate le macchine virtuali di gestione dei dispositivi, il programma di installazione le registra nel Registro di sistema di Windows. Le applicazioni possono enumerare i CMM registrati e selezionarne uno usando la [**funzione SelectCMM.**](/windows/win32/api/icm/nf-icm-selectcmm) L'applicazione di esempio seguente illustra come enumerare tutte le macchine virtuali di gestione delle applicazioni registrate.


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
                 gszICMatcher, &hkCMM);
    DWORD dwMaxName, dwMaxValue;
    DWORD dwInfoErr = RegQueryInfoKey(&hkCMM, NULL, NULL,
                                NULL, NULL, NULL, NULL, NULL,
                                &dwMaxName, &dwMaxValue,
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
                   &cjCMM,NULL,&dwType,
                   chCMMFile,&cjCMMFile) == ERROR_SUCCESS)
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



 

 




