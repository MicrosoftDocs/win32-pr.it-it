---
title: Informazioni sulle funzioni e le intestazioni delle informazioni di MprInfo
description: Le funzioni seguenti richiedono che il chiamante passi una struttura o un'intestazione di informazioni come uno dei parametri.
ms.assetid: 389002c9-2d24-4b35-ab5b-801fe2091db9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 001c39bf28500d7261b3eb99abf0266470daf3d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955533"
---
# <a name="understanding-mprinfo-functions-and-information-headers"></a>Informazioni sulle funzioni e le intestazioni delle informazioni di MprInfo

Le funzioni seguenti richiedono che il chiamante passi una struttura o un' *intestazione* di informazioni come uno dei parametri.



| Funzione di amministrazione                                                        | Funzione di configurazione                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| Nessuna funzione di amministrazione                                                     | [**MprConfigTransportCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportcreate)                     |
| [**MprAdminTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportsetinfo)                   | [**MprConfigTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportsetinfo)                   |
| [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) | [**MprConfigInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) |
| [**MprAdminInterfaceTransportAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportadd)         | [**MprConfigInterfaceTransportAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportadd)         |



 

Analogamente, le funzioni seguenti restituiscono le intestazioni delle informazioni.



| Funzione di amministrazione                                                        | Funzione di configurazione                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**MprAdminTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportgetinfo)                   | [**MprConfigTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportgetinfo)                   |
| [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) | [**MprConfigInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) |



 

Per le funzioni di trasporto, l'intestazione Information contiene informazioni globali per il trasporto. Per le funzioni client (InterfaceTransport), l'intestazione contiene informazioni specifiche del client, ad esempio OSPF, da amministrare.

Le intestazioni delle informazioni e il relativo contenuto devono essere modificati solo usando le funzioni [MprInfo](router-information-functions.md) . Gli sviluppatori non devono tentare di modificare direttamente il contenuto delle intestazioni delle informazioni.

Le funzioni di solo interfaccia, ad esempio [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) , non richiedono l'uso di funzioni MprInfo. Le informazioni passate e restituite con queste funzioni hanno sempre il formato di una struttura di [**\_ interfaccia MPR**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) .

 

 




