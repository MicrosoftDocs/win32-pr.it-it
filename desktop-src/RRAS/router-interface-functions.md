---
title: Funzioni dell'interfaccia router
description: Usare le funzioni seguenti per amministrare le interfacce nel router.
ms.assetid: e988753e-908a-4c42-aad3-dd9f641c90a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bcaaf257e31623036a075c21da66d4665b3afe7e821f8f246f6a225e02b8272
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117787837"
---
# <a name="router-interface-functions"></a>Funzioni dell'interfaccia router

Usare le funzioni seguenti per amministrare le interfacce nel router.



| Funzione di amministrazione                                          | Funzione di configurazione                                             |
|------------------------------------------------------------------|--------------------------------------------------------------------|
| [**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate)       | [**MprConfigInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacecreate)       |
| [**MprAdminInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete)       | [**MprConfigInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacedelete)       |
| [**MprAdminInterfaceEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfaceenum)           | [**MprConfigInterfaceEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfaceenum)           |
| [**MprAdminInterfaceGetHandle**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegethandle) | [**MprConfigInterfaceGetHandle**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegethandle) |
| [**MprAdminInterfaceGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegetinfo)     | [**MprConfigInterfaceGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegetinfo)     |
| [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo)     | [**MprConfigInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo)     |



 

Queste funzioni influiscono sulle interfacce stesse, non sui client in esecuzione sulle interfacce. Per questo motivo, nessuna delle funzioni richiede al chiamante di specificare un trasporto specifico (IP o IPX). anche se i client ( ad esempio i protocolli di routing) sono associati a trasporti specifici, le interfacce stesse non lo sono.

Queste funzioni vengono gestite direttamente da DIM. Non utilizzano i gestori router.

Le [**funzioni MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) e [**MprAdminInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete) non possono creare o eliminare interfacce LAN. Possono solo creare o eliminare interfacce di connessione a richiesta. Per [**un elenco dei tipi di \_ \_ interfaccia,**](/windows/desktop/api/Mprapi/ne-mprapi-router_interface_type) vedere TIPO DI INTERFACCIA ROUTER.

 

 




