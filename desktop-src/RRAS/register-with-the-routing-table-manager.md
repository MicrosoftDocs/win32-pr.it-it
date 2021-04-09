---
title: Eseguire la registrazione con gestione tabelle di routing
description: Nell'esempio di codice seguente viene illustrato come registrare una nuova entità con gestione tabelle di routing.
ms.assetid: 320cc97f-2875-4d26-b2f4-5611a43d5839
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3b5e2f3ba3df414f383305d09c129b52bcb32cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044512"
---
# <a name="register-with-the-routing-table-manager"></a>Eseguire la registrazione con gestione tabelle di routing

Nell'esempio di codice seguente viene illustrato come registrare una nuova entità con gestione tabelle di routing.


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



 

 




