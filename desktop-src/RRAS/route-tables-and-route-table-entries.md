---
title: Tabelle di route e voci della tabella di route
description: Gestione tabelle di routing mantiene tabelle di route distinte per ogni famiglia di protocolli.
ms.assetid: 3848d93d-cc54-4a08-bd36-a9700cde6ce0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f118ec1d0a6f8fe4ef301654e139f217257c3a0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297609"
---
# <a name="route-tables-and-route-table-entries"></a>Tabelle di route e voci della tabella di route

**Windows Server 2003:** Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le nuove applicazioni devono usare l'API di Routing Table Manager versione 2.

Gestione tabelle di routing mantiene tabelle di route distinte per ogni famiglia di protocolli. Attualmente, è disponibile il supporto esplicito per le famiglie di protocolli di routing Internet Protocol (IP) e Internet Packet Exchange (IPX). Indipendentemente dalla famiglia di protocolli, ogni voce di route contiene le informazioni seguenti:

-   Rete di destinazione.
-   Identificatore del protocollo che ha aggiunto la route.
-   Indice dell'interfaccia tramite cui è stata ottenuta la route. Questo valore di indice è il valore numerico assegnato a un'interfaccia di rete (basata su hardware o virtuale) che trasmette i dati nella rete. (Ad esempio, una scheda di interfaccia di rete Ethernet o una scheda wireless 802.1 b).
-   Indirizzo del router hop successivo. RRAS utilizza questo router per inoltrare i pacchetti alla rete di destinazione se la rete non è direttamente connessa.
-   Data e ora di creazione o dell'ultimo aggiornamento della route.
-   Quantità di tempo in cui la route viene mantenuta nella tabella di routing. Se questa quantità di tempo scade e la route non è stata aggiornata, il servizio di gestione delle tabelle di routing rimuove la route dalla tabella. In questo caso, si dice che la route è *obsoleta*.
-   Dati specifici della famiglia di protocolli. Questi dati sono trasparenti per RTMv1. Tuttavia, se questi dati cambiano per una route designata come "route migliore", il gestore delle tabelle di routing invia una notifica di modifica della route.
-   Dati specifici del protocollo di routing. Questi dati sono completamente trasparenti per Gestione tabelle di routing, in quanto le modifiche apportate a questi dati non provocano la notifica delle modifiche della route.

I valori seguenti riuniti identificano in modo univoco una route nella tabella di routing:

-   Rete di destinazione
-   Identificatore di protocollo
-   Indice dell'interfaccia
-   Indirizzo del router hop successivo

In generale, gestione tabelle di routing crea voci separate per le route che differiscono da uno di questi valori di parametro. Viene tuttavia creata un'eccezione per i protocolli di routing che non mantengono più di una voce per ogni rete di destinazione. Per questi protocolli, gestione tabelle di routing ignora le differenze tra l'indice dell'interfaccia o l'indirizzo hop successivo. Un esempio di protocollo di questo tipo è l'implementazione RRAS del primo percorso (OSPF) più breve aperto.

 

 




