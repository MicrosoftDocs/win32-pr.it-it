---
title: Rilevamento dell'Servizi Desktop remoto virtuale
description: Per ottimizzare le prestazioni, è consigliabile che le applicazioni rilevino se sono in esecuzione in una Servizi Desktop remoto client.
ms.assetid: 9ba03801-8471-43a9-8e24-114a082d5776
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f54634112b4a6ac3cc1e981421e4a3e33af5e32bae8ab63ec8690f2df12c7a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657991"
---
# <a name="detecting-the-remote-desktop-services-environment"></a>Rilevamento dell'Servizi Desktop remoto virtuale

Per ottimizzare le prestazioni, è consigliabile che le applicazioni rilevino se sono in esecuzione in una Servizi Desktop remoto client. Ad esempio, quando un'applicazione è in esecuzione in una sessione remota, deve eliminare gli effetti grafici non necessari, come descritto in [Effetti grafici.](graphic-effects.md) Se l'utente esegue l'applicazione in un ambiente locale, non è essenziale per l'applicazione ottimizzarne il comportamento.

Nell'esempio seguente viene illustrata una funzione che restituisce **TRUE** se l'applicazione è in esecuzione in una sessione remota e **FALSE se** l'applicazione è in esecuzione nella console.


```C++
#include <windows.h>
#pragma comment(lib, "user32.lib")

BOOL IsRemoteSession(void)
{
   return GetSystemMetrics( SM_REMOTESESSION );
}
```



Per altre informazioni, vedere [Collegamento in fase di esecuzione Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).

Non usare **GetSystemMetrics(SM \_ REMOTESESSION)** per determinare se l'applicazione è in esecuzione in una sessione remota in Windows 8 e versioni successive o Windows Server 2012 e versioni successive se la sessione remota potrebbe anche usare i miglioramenti della vGPU di RemoteFX per Microsoft Remote Display Protocol (RDP). In questo caso, **GetSystemMetrics(SM \_ REMOTESESSION)** identificherà la sessione remota come sessione locale.

L'applicazione può controllare la chiave del Registro di sistema seguente per determinare se la sessione è una sessione remota che usa RemoteFX vGPU. Se esiste una sessione locale, questa chiave del Registro di sistema fornisce l'ID della sessione locale.

**HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ Terminal Server \\ GlassSessionId**

Se l'ID della sessione corrente in cui è in esecuzione l'applicazione è lo stesso della chiave del Registro di sistema, l'applicazione viene eseguita in una sessione locale. Le sessioni identificate come sessione remota in questo modo includono sessioni remote che usano RemoteFX vGPU. Nel codice di esempio seguente viene illustrata questa operazione.


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



 

 




