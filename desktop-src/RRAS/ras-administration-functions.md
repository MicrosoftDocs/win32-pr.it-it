---
title: Funzioni di amministrazione RAS
description: In questa documentazione vengono descritte le funzioni RRAS utilizzate per sviluppare software per amministrare le connessioni remote RAS.
ms.assetid: 27cf63e2-9dd3-4bc1-98af-e93055d89492
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec0a18f6c49964d89c308b065289dd4de9fc22c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332044"
---
# <a name="ras-administration-functions"></a>Funzioni di amministrazione RAS

In questa documentazione vengono descritte le funzioni RRAS utilizzate per sviluppare software per amministrare le connessioni remote RAS. Queste funzioni includono:

-   [**MprAdminConnectionClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionclearstats)
-   [**MprAdminConnectionEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum)
-   [**MprAdminConnectionEnumEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenumex)
-   [**MprAdminConnectionGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfo)
-   [**MprAdminConnectionGetInfoEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfoex)
-   [**MprAdminConnectionRemoveQuarantine**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionremovequarantine)
-   [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)
-   [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)
-   [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)
-   [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)
-   [**MprAdminPortReset**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportreset)

Funzioni aggiuntive vengono usate per l'amministrazione RAS e il router. Le funzioni seguenti sono documentate nelle informazioni di riferimento sulle [funzioni di amministrazione del router](router-administration-functions.md) :

-   [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)
-   [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)
-   [**MprAdminIsServiceRunning**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning)
-   [**MprAdminServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect)
-   [**MprAdminServerDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverdisconnect)

Per implementare una DLL di amministrazione RAS, utilizzare le funzioni descritte nell'argomento seguente:

-   [Funzioni DLL amministratore RAS](ras-admin-dll-functions.md)

Per gestire gli utenti di un server RAS, utilizzare le funzioni descritte nell'argomento seguente:

-   [Funzioni di amministrazione utenti RAS](ras-user-administration-functions.md)

 

 




