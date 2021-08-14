---
title: Eseguire la registrazione con Gestione tabelle di routing
description: Il codice di esempio seguente illustra come registrare una nuova entità con il gestore tabelle di routing.
ms.assetid: 320cc97f-2875-4d26-b2f4-5611a43d5839
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ccb3aaae18d9e327bffb94019b1b69c4fc2b62bc36a7cb4ae31225f9a8a827d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788610"
---
# <a name="register-with-the-routing-table-manager"></a>Eseguire la registrazione con Gestione tabelle di routing

Il codice di esempio seguente illustra come registrare una nuova entità con il gestore tabelle di routing.


```C++
#include <windows.h>
#include <stdio.h>
#include "Rtmv2.h"
#include "nldef.h"

// The following #defines are from routprot.h in the Platform Software Develoment Kit (SDK)
#define PROTO_TYPE_UCAST     0
#define PROTOCOL_ID(Type, VendorId, ProtocolId) (((Type & 0x03)<<30)|((VendorId & 0x3FFF)<<16)|(ProtocolId & 0xFFFF))
#define PROTO_VENDOR_ID      0xFFFF

int __cdecl main(){
 
    RTM_ENTITY_HANDLE RtmRegHandle;
    RTM_ENTITY_INFO EntityInfo;
    RTM_REGN_PROFILE RegnProfile;
    DWORD dwRet = ERROR_SUCCESS;

    EntityInfo.RtmInstanceId = 0;
    EntityInfo.AddressFamily = AF_INET;
    EntityInfo.EntityId.EntityProtocolId = PROTO_IP_RIP;
    EntityInfo.EntityId.EntityInstanceId = PROTOCOL_ID(PROTO_TYPE_UCAST, PROTO_VENDOR_ID, PROTO_IP_RIP);

    // Register the new entity
    dwRet = RtmRegisterEntity(&EntityInfo, NULL, NULL, FALSE, &RegnProfile, &RtmRegHandle);
    if (dwRet != ERROR_SUCCESS){
        // Registration failed - Log an Error and Quit
    }

    // Clean-up: Deregister the new entity
    dwRet = RtmDeregisterEntity(RtmRegHandle);
    if (dwRet != ERROR_SUCCESS){
        // Registration failed - Log an Error and Quit
    }

    return 0;
}
```



 

 




