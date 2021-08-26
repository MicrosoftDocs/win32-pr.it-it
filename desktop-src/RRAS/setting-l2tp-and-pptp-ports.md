---
title: Impostazione delle porte L2TP e PPTP del servizio RRAS locale
description: Questo esempio ottiene e imposta la configurazione delle porte L2TP e PPTP del servizio RRAS locale. Presuppone che il processo chiamante disponga di privilegi sufficienti per accedere al servizio RRAS locale.
ms.assetid: 9e4aa8d4-e09e-4c84-acf0-c505a58841a4
keywords:
- Impostazione delle porte del servizio RRAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ae05fabd171bba59286b3a68120895132b303af9c5e81e7c6a36410e98195be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073771"
---
# <a name="setting-l2tp-and-pptp-ports-of-local-rras-service"></a>Impostazione delle porte L2TP e PPTP del servizio RRAS locale

Questo esempio ottiene e imposta la configurazione delle porte L2TP e PPTP del servizio RRAS locale. Presuppone che il processo chiamante disponga di privilegi sufficienti per accedere al servizio RRAS locale.


```C++
#include <windows.h>
#include <stdio.h>
#include "mprapi.h"
#include <tchar.h>
#pragma comment(lib, "mprapi.lib")

int __cdecl main(){

    DWORD dwRes = ERROR_SUCCESS;
    PMPR_SERVER_1 pMprServer = NULL;
    MPR_SERVER_1 MprServer;
    MPR_SERVER_HANDLE hMprServer = NULL;

    // Connect to the local RRAS server
    dwRes = MprAdminServerConnect(NULL, &hMprServer);
    if(dwRes != ERROR_SUCCESS){
        //
        //Handle errors here
        //
        return dwRes;
    }

    // Collect L2TP and PPTP port information from local RRAS server
    dwRes = MprAdminServerGetInfo(hMprServer, 1, (LPBYTE*)&pMprServer);
    if(dwRes != ERROR_SUCCESS){
        //
        //Handle errors here
        //
        MprAdminServerDisconnect(hMprServer);
        return dwRes;
    }

    if(!pMprServer->dwL2tpPortFlags)
        wprintf(L"The local machine contains %d L2TP port(s) that is(are) not configured for RRAS.\n", pMprServer->dwNumL2tpPorts);
    else
        wprintf(L"The local machine contains %d L2TP port(s) that is(are) configured for RRAS.\n", pMprServer->dwNumL2tpPorts);

    if(!pMprServer->dwPptpPortFlags)
        wprintf(L"The local machine contains %d PPTP port(s) that is(are) not configured for RRAS.\n", pMprServer->dwNumPptpPorts);
    else
        wprintf(L"The local machine contains %d PPTP port(s) that is(are) configured for RRAS.\n\n", pMprServer->dwNumPptpPorts);

    // Save original L2TP and PPTP configuration info
    MprServer.dwL2tpPortFlags = pMprServer->dwL2tpPortFlags;
    MprServer.dwPptpPortFlags = pMprServer->dwPptpPortFlags;
    MprServer.dwNumL2tpPorts = pMprServer->dwNumL2tpPorts;
    MprServer.dwNumPptpPorts = pMprServer->dwNumPptpPorts;

    // Modify L2TP and PPTP port information on the local RRAS server
    wprintf(L"Disabling RRAS enabled L2TP and PPTP ports on the local system.");
    pMprServer->dwL2tpPortFlags = FALSE;
    pMprServer->dwPptpPortFlags = FALSE;
    dwRes = MprAdminServerSetInfo(hMprServer, 1, (LPBYTE)pMprServer);
    if(dwRes != ERROR_SUCCESS_REBOOT_REQUIRED && dwRes != ERROR_SUCCESS){
        //
        // Handle errors here
        //
        wprintf(L".....ERROR\n");
        MprAdminBufferFree(pMprServer);
        MprAdminServerDisconnect(hMprServer);
        return dwRes;
    }
    wprintf(L".....OK\n");
    
    //Cleanup
    pMprServer->dwL2tpPortFlags = MprServer.dwL2tpPortFlags;
    pMprServer->dwPptpPortFlags = MprServer.dwPptpPortFlags;
    pMprServer->dwNumL2tpPorts = MprServer.dwNumL2tpPorts;
    pMprServer->dwNumPptpPorts = MprServer.dwNumPptpPorts;
    dwRes = MprAdminServerSetInfo(hMprServer, 1, (LPBYTE)pMprServer);
    
    MprAdminBufferFree(pMprServer);
    MprAdminServerDisconnect(hMprServer);
    return dwRes;
}
```



 

 




