---
title: Informazioni di riferimento per l'interfaccia del protocollo di routing
description: Questa documentazione descrive le funzioni e le strutture usate per implementare un protocollo di routing come DLL in modalità utente.
ms.assetid: 0429f5ca-6574-48f5-85ab-70b4677ca539
keywords:
- Routing e Servizio di accesso remoto RRAS, interfaccia del protocollo di routing, informazioni di riferimento
- Routing Protocol Interface RRAS , informazioni di riferimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0196a5cbad8919a07a6e9a19ee5f7848eb6378ad2c56f7f0977125e5e79133a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027351"
---
# <a name="routing-protocol-interface-reference"></a>Informazioni di riferimento per l'interfaccia del protocollo di routing

Questa documentazione descrive le funzioni e le strutture usate per implementare un protocollo di routing come DLL in modalità utente.

MPR50 deve essere definito nel file make per il protocollo di routing.

La macro **SIZEOF \_ IP \_ BINDING(x)** calcola le dimensioni, in byte, di una struttura [**IP ADAPTER BINDING \_ \_ \_ INFO**](/windows/desktop/api/Routprot/ns-routprot-ip_adapter_binding_info) che contiene il numero di indirizzi IP.

Questi elementi di riferimento sono descritti negli argomenti seguenti:

-   [Funzioni dell'interfaccia del protocollo di routing](routing-protocol-interface-functions.md)
-   [Strutture dell'interfaccia del protocollo di routing](routing-protocol-interface-structures.md)
-   [Gestione tabelle del servizio IPX](ipx-service-table-management.md)

 

 




