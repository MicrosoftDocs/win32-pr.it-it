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
# <a name="detecting-the-remote-desktop-services-environment"></a><span data-ttu-id="aab71-103">Rilevamento dell'ambiente Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="aab71-103">Detecting the Remote Desktop Services environment</span></span>

<span data-ttu-id="aab71-104">Per ottimizzare le prestazioni, è consigliabile che le applicazioni rilevino se sono in esecuzione in una sessione client Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="aab71-104">To optimize performance, it is good practice for applications to detect whether they are running in a Remote Desktop Services client session.</span></span> <span data-ttu-id="aab71-105">Ad esempio, quando un'applicazione è in esecuzione in una sessione remota, deve eliminare gli effetti grafici non necessari, come descritto in [effetti grafici](graphic-effects.md).</span><span class="sxs-lookup"><span data-stu-id="aab71-105">For example, when an application is running on a remote session, it should eliminate unnecessary graphic effects, as described in [Graphic Effects](graphic-effects.md).</span></span> <span data-ttu-id="aab71-106">Se l'utente esegue l'applicazione in un ambiente locale, non è cruciale per l'applicazione ottimizzare il comportamento.</span><span class="sxs-lookup"><span data-stu-id="aab71-106">If the user is running the application in a local environment, it is not as critical for the application to optimize its behavior.</span></span>

<span data-ttu-id="aab71-107">Nell'esempio seguente viene illustrata una funzione che restituisce **true** se l'applicazione è in esecuzione in una sessione remota e **false** se l'applicazione è in esecuzione nella console di.</span><span class="sxs-lookup"><span data-stu-id="aab71-107">The following example shows a function that returns **TRUE** if the application is running in a remote session and **FALSE** if the application is running on the console.</span></span>


```C++
#include <windows.h>
#pragma comment(lib, "user32.lib")

BOOL IsRemoteSession(void)
{
   return GetSystemMetrics( SM_REMOTESESSION );
}
```



<span data-ttu-id="aab71-108">Per ulteriori informazioni, vedere il [collegamento di run-time a Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).</span><span class="sxs-lookup"><span data-stu-id="aab71-108">For more information, see [Run-time Linking to Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).</span></span>

<span data-ttu-id="aab71-109">Non usare **GetSystemMetrics (SM \_ REMOTESESSION)** per determinare se l'applicazione è in esecuzione in una sessione remota in Windows 8 e versioni successive o Windows Server 2012 e versioni successive se la sessione remota può anche usare i miglioramenti RemoteFX VGPU per il protocollo RDP (Remote Display Protocol) di Microsoft.</span><span class="sxs-lookup"><span data-stu-id="aab71-109">You should not use **GetSystemMetrics(SM\_REMOTESESSION)** to determine if your application is running in a remote session in Windows 8 and later or Windows Server 2012 and later if the remote session may also be using the RemoteFX vGPU improvements to the Microsoft Remote Display Protocol (RDP).</span></span> <span data-ttu-id="aab71-110">In questo caso, **GetSystemMetrics (SM \_ REMOTESESSION)** identificherà la sessione remota come una sessione locale.</span><span class="sxs-lookup"><span data-stu-id="aab71-110">In this case, **GetSystemMetrics(SM\_REMOTESESSION)** will identify the remote session as a local session.</span></span>

<span data-ttu-id="aab71-111">L'applicazione può controllare la seguente chiave del registro di sistema per determinare se la sessione è una sessione remota che usa RemoteFX vGPU.</span><span class="sxs-lookup"><span data-stu-id="aab71-111">Your application can check the following registry key to determine whether the session is a remote session that uses RemoteFX vGPU.</span></span> <span data-ttu-id="aab71-112">Se è presente una sessione locale, questa chiave del registro di sistema fornisce l'ID della sessione locale.</span><span class="sxs-lookup"><span data-stu-id="aab71-112">If a local session exists, this registry key provides the ID of the local session.</span></span>

<span data-ttu-id="aab71-113">**HKEY \_ Local \_ computer \\ System \\ CurrentControlSet \\ Control \\ Terminal Server \\ GlassSessionId**</span><span class="sxs-lookup"><span data-stu-id="aab71-113">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Terminal Server\\GlassSessionId**</span></span>

<span data-ttu-id="aab71-114">Se l'ID della sessione corrente in cui è in esecuzione l'applicazione è identico a quello della chiave del registro di sistema, l'applicazione è in esecuzione in una sessione locale.</span><span class="sxs-lookup"><span data-stu-id="aab71-114">If the ID of the current session in which the application is running is the same as in the registry key, the application is running in a local session.</span></span> <span data-ttu-id="aab71-115">Le sessioni identificate come sessione remota in questo modo includono sessioni remote che usano RemoteFX vGPU.</span><span class="sxs-lookup"><span data-stu-id="aab71-115">Sessions identified as remote session in this way include remote sessions that use RemoteFX vGPU.</span></span> <span data-ttu-id="aab71-116">Nel codice di esempio seguente viene illustrata questa operazione.</span><span class="sxs-lookup"><span data-stu-id="aab71-116">The following sample code demonstrates this.</span></span>


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



 

 




