---
description: Descrive come rilevare se un set di API specifico è disponibile nel dispositivo corrente.
title: Rilevare la disponibilità di un set di API
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: cc4e26c6e59cfa0af095b297efb72a52d0be30a89a23d42d169e3bf45e72fd13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896531"
---
# <a name="detect-api-set-availability"></a>Rilevare la disponibilità di un set di API

In alcuni casi, un nome di contratto del set di API specificato può essere intenzionalmente mappato a un nome di modulo vuoto in alcuni Windows 10 dispositivi. I motivi possono variare, ma un esempio comune è che una funzionalità costosa in termini di risorse di sistema può essere rimossa dal sistema operativo Windows se configurata per un dispositivo con risorse limitate. In questo modo le applicazioni possono gestire correttamente le funzionalità facoltative a livello di API.

L'approccio tradizionale per verificare se un'API Win32 è disponibile consiste nell'usare [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress). Tuttavia, questi non sono un mezzo affidabile [](api-set-loader-operation.md#reverse-forwarding) per testare i set di API a causa del supporto dell'inoltro inverso in Windows 10. Quando l'inoltro inverso viene applicato a una determinata API, **LoadLibrary** o **GetProcAddress** può risolversi in un puntatore a funzione valido anche nei casi in cui l'implementazione interna è stata rimossa. In questo caso, il puntatore a funzione punta a una funzione stub che restituisce semplicemente un errore.

Per rilevare questo caso, è possibile usare la [funzione IsApiSetImplemented](/windows/win32/api/apiquery2/nf-apiquery2-isapisetimplemented) per eseguire query sulla disponibilità sottostante di una determinata implementazione dell'API. Questo test convalida che la chiamata a questa funzione comporta l'esecuzione di un'implementazione funzionale dell'API.

L'esempio di codice seguente illustra come usare **IsApiSetImplemented** per determinare se la funzione [WTSEnumerateSessions](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa) è disponibile nel dispositivo corrente prima di chiamarla. 

```c++
#include <windows.h>
#include <stdio.h>
#include <Wtsapi32.h>

int __cdecl wmain(int /* argc */, PCWSTR /* argv */ [])
{
    PWTS_SESSION_INFO pInfo = {};
    DWORD count = 0;

    if (!IsApiSetImplemented("ext-ms-win-session-wtsapi32-l1-1-0"))
    {
        wprintf(L"IsApiSetImplemented on ext-ms-win-session-wtsapi32-l1-1-0 returns FALSE\n");
    }
    else
    {
        if (WTSEnumerateSessionsW(WTS_CURRENT_SERVER_HANDLE, 0, 1, &pInfo, &count))
        {
            wprintf(L"SessionCount = %d\n", count);

            for (ULONG i = 0; i < count; i++)
            {
                PWTS_SESSION_INFO pCurInfo = &pInfo[i];
                wprintf(L"    %s: ID = %d, state = %d\n", pCurInfo->pWinStationName, 
                    pCurInfo->SessionId, pCurInfo->State);
            }

            WTSFreeMemory(pInfo);
        }
        else
        {
            wprintf(L"WTSEnumerateSessions failure : %x\n", GetLastError());
        }
    }

    return 0;
}
```