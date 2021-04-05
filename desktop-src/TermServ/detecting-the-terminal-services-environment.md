---
title: Rilevamento dell'ambiente Servizi Desktop remoto
description: Per ottimizzare le prestazioni, è consigliabile che le applicazioni rilevino se sono in esecuzione in una sessione client Servizi Desktop remoto.
ms.assetid: 9ba03801-8471-43a9-8e24-114a082d5776
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fde3263925a3b8bf4921dd0dfc95842a5dc5b4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515769"
---
# <a name="detecting-the-remote-desktop-services-environment"></a>Rilevamento dell'ambiente Servizi Desktop remoto

Per ottimizzare le prestazioni, è consigliabile che le applicazioni rilevino se sono in esecuzione in una sessione client Servizi Desktop remoto. Ad esempio, quando un'applicazione è in esecuzione in una sessione remota, deve eliminare gli effetti grafici non necessari, come descritto in [effetti grafici](graphic-effects.md). Se l'utente esegue l'applicazione in un ambiente locale, non è cruciale per l'applicazione ottimizzare il comportamento.

Nell'esempio seguente viene illustrata una funzione che restituisce **true** se l'applicazione è in esecuzione in una sessione remota e **false** se l'applicazione è in esecuzione nella console di.


```C++
#include <windows.h>
#pragma comment(lib, "user32.lib")

BOOL IsRemoteSession(void)
{
   return GetSystemMetrics( SM_REMOTESESSION );
}
```



Per ulteriori informazioni, vedere il [collegamento di run-time a Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).

Non usare **GetSystemMetrics (SM \_ REMOTESESSION)** per determinare se l'applicazione è in esecuzione in una sessione remota in Windows 8 e versioni successive o Windows Server 2012 e versioni successive se la sessione remota può anche usare i miglioramenti RemoteFX VGPU per il protocollo RDP (Remote Display Protocol) di Microsoft. In questo caso, **GetSystemMetrics (SM \_ REMOTESESSION)** identificherà la sessione remota come una sessione locale.

L'applicazione può controllare la seguente chiave del registro di sistema per determinare se la sessione è una sessione remota che usa RemoteFX vGPU. Se è presente una sessione locale, questa chiave del registro di sistema fornisce l'ID della sessione locale.

**HKEY \_ Local \_ computer \\ System \\ CurrentControlSet \\ Control \\ Terminal Server \\ GlassSessionId**

Se l'ID della sessione corrente in cui è in esecuzione l'applicazione è identico a quello della chiave del registro di sistema, l'applicazione è in esecuzione in una sessione locale. Le sessioni identificate come sessione remota in questo modo includono sessioni remote che usano RemoteFX vGPU. Nel codice di esempio seguente viene illustrata questa operazione.


```C++
#define TERMINAL_SERVER_KEY _T("SYSTEM\\CurrentControlSet\\Control\\Terminal Server\\")
#define GLASS_SESSION_ID    _T("GlassSessionId")

BOOL
IsCurrentSessionRemoteable()
{
    BOOL fIsRemoteable = FALSE;
                                       
    if (GetSystemMetrics(SM_REMOTESESSION)) 
    {
        fIsRemoteable = TRUE;
    }
    else
    {
        HKEY hRegKey = NULL;
        LONG lResult;

        lResult = RegOpenKeyEx(
            HKEY_LOCAL_MACHINE,
            TERMINAL_SERVER_KEY,
            0, // ulOptions
            KEY_READ,
            &hRegKey
            );

        if (lResult == ERROR_SUCCESS)
        {
            DWORD dwGlassSessionId;
            DWORD cbGlassSessionId = sizeof(dwGlassSessionId);
            DWORD dwType;

            lResult = RegQueryValueEx(
                hRegKey,
                GLASS_SESSION_ID,
                NULL, // lpReserved
                &dwType,
                (BYTE*) &dwGlassSessionId,
                &cbGlassSessionId
                );

            if (lResult == ERROR_SUCCESS)
            {
                DWORD dwCurrentSessionId;

                if (ProcessIdToSessionId(GetCurrentProcessId(), &dwCurrentSessionId))
                {
                    fIsRemoteable = (dwCurrentSessionId != dwGlassSessionId);
                }
            }
        }

        if (hRegKey)
        {
            RegCloseKey(hRegKey);
        }
    }

    return fIsRemoteable;
}
```



 

 




