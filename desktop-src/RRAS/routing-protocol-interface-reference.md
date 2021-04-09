---
title: Guida di riferimento all'interfaccia del protocollo di routing
description: In questa documentazione vengono descritte le funzioni e le strutture utilizzate per implementare un protocollo di routing come DLL in modalità utente.
ms.assetid: 0429f5ca-6574-48f5-85ab-70b4677ca539
keywords:
- Servizio Routing e accesso remoto RRAS, interfaccia protocollo di routing, riferimento
- Interfaccia del protocollo di routing RRAS, riferimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9341dd8dbd304da84fd675aee92e378a44271056
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856097"
---
# <a name="routing-protocol-interface-reference"></a>Guida di riferimento all'interfaccia del protocollo di routing

In questa documentazione vengono descritte le funzioni e le strutture utilizzate per implementare un protocollo di routing come DLL in modalità utente.

MPR50 deve essere definito nel file make per il protocollo di routing.

La macro di **\_ binding IP sizeof \_ (x)** calcola la dimensione, in byte, di una struttura di [**\_ informazioni di \_ binding \_ della scheda IP**](/windows/desktop/api/Routprot/ns-routprot-ip_adapter_binding_info) che contiene il numero di indirizzi IP.

Questi elementi di riferimento sono descritti negli argomenti seguenti:

-   [Funzioni di interfaccia del protocollo di routing](routing-protocol-interface-functions.md)
-   [Strutture di interfaccia del protocollo di routing](routing-protocol-interface-structures.md)
-   [Gestione tabella dei servizi IPX](ipx-service-table-management.md)

 

 




