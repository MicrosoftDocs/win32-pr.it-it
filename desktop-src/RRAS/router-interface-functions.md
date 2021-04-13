---
title: Funzioni di interfaccia del router
description: Usare le funzioni seguenti per amministrare le interfacce sul router.
ms.assetid: e988753e-908a-4c42-aad3-dd9f641c90a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a5318eedfbc3a04c13549012fda3bd4d93b4d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328231"
---
# <a name="router-interface-functions"></a>Funzioni di interfaccia del router

Usare le funzioni seguenti per amministrare le interfacce sul router.



| Funzione di amministrazione                                          | Funzione di configurazione                                             |
|------------------------------------------------------------------|--------------------------------------------------------------------|
| [**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate)       | [**MprConfigInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacecreate)       |
| [**MprAdminInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete)       | [**MprConfigInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacedelete)       |
| [**MprAdminInterfaceEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfaceenum)           | [**MprConfigInterfaceEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfaceenum)           |
| [**MprAdminInterfaceGetHandle**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegethandle) | [**MprConfigInterfaceGetHandle**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegethandle) |
| [**MprAdminInterfaceGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegetinfo)     | [**MprConfigInterfaceGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegetinfo)     |
| [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo)     | [**MprConfigInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo)     |



 

Queste funzioni influiscono sulle interfacce stesse, non sui client in esecuzione sulle interfacce. Per questo motivo, nessuna delle funzioni richiede che il chiamante specifichi un trasporto specifico (IP o IPX); Sebbene i client, ad esempio i protocolli di routing, siano associati a trasporti particolari, le interfacce non lo sono.

Queste funzioni vengono gestite direttamente da DIM. Non utilizzano i gestori dei router.

Le funzioni [**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) e [**MprAdminInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete) non possono creare o eliminare interfacce LAN. Possono solo creare o eliminare le interfacce di connessione a richiesta. Vedere [**\_ \_ tipo di interfaccia del router**](/windows/desktop/api/Mprapi/ne-mprapi-router_interface_type) per un elenco di tipi di interfaccia.

 

 




