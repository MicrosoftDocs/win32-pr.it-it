---
description: Viene descritto come rilevare se un set di API specifico è disponibile nel dispositivo corrente.
title: Rilevare la disponibilità di un set di API
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 7117ae82f142315a3e5f28065583381ef6af67f3
ms.sourcegitcommit: 0c786b1682063d0cae0fc43180945183fa2c7981
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/24/2020
ms.locfileid: "104118654"
---
# <a name="detect-api-set-availability"></a>Rilevare la disponibilità di un set di API

In alcuni casi, è possibile eseguire intenzionalmente il mapping di un nome di contratto del set di API specificato a un nome di modulo vuoto in alcuni dispositivi Windows 10. I motivi di questo problema variano, ma un esempio comune è che una funzionalità costosa in termini di risorse di sistema può essere rimossa dal sistema operativo Windows se configurata per un dispositivo con vincoli di risorse. Ciò costituisce un problema per le applicazioni che gestiscono normalmente le funzionalità facoltative a livello di API.

L'approccio tradizionale per verificare se un'API Win32 è disponibile consiste nell'usare [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress). Tuttavia, non si tratta di un metodo affidabile per il test dei set di API a causa del supporto per l' [invio inverso](api-set-loader-operation.md#reverse-forwarding) di Windows 10. Quando l'avanzamento inverso viene applicato a una determinata API, **LoadLibrary** o **GetProcAddress** può risolversi in un puntatore a funzione valido anche nei casi in cui l'implementazione interna è stata rimossa. In questo caso, il puntatore a funzione punterà a una funzione stub che restituisce semplicemente un errore.

Per rilevare questo caso, è possibile usare la funzione [IsApiSetImplemented](/windows/win32/api/apiquery2/nf-apiquery2-isapisetimplemented) per eseguire una query sulla disponibilità sottostante di un'implementazione API specificata. Questo test verifica che la chiamata a questa funzione provochi l'esecuzione di un'implementazione funzionale dell'API.

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