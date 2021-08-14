---
title: Tabelle di route e voci di tabella di route
description: Il gestore tabelle di routing gestisce tabelle di route distinte per ogni famiglia di protocolli.
ms.assetid: 3848d93d-cc54-4a08-bd36-a9700cde6ce0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31fea4ac965fe397d5bb7eba2b65479358a1e192f1583b1e7e73c2532dbd3a50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788056"
---
# <a name="route-tables-and-route-table-entries"></a>Tabelle di route e voci di tabella di route

**Windows Server 2003:** Questa API è stata sostituita dall'API Gestione tabelle di [routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le nuove applicazioni devono usare l'API Gestione tabelle di routing versione 2.

Il gestore tabelle di routing gestisce tabelle di route distinte per ogni famiglia di protocolli. Attualmente, viene fornito il supporto esplicito per le famiglie di protocolli di routing IP (Internet Protocol) e IPX (Internet Packet Exchange). Indipendentemente dalla famiglia di protocolli, ogni voce di route contiene le informazioni seguenti:

-   Rete di destinazione.
-   Identificatore del protocollo che ha aggiunto la route.
-   Indice dell'interfaccia tramite cui è stata ottenuta la route. Questo valore di indice è il valore numerico assegnato a un'interfaccia di rete (basata su hardware o virtuale) che trasmette i dati in rete. Ad esempio, una scheda di interfaccia di rete Ethernet o una scheda wireless 802.1b.
-   Indirizzo del router hop successivo. RRAS usa questo router per inoltrare i pacchetti alla rete di destinazione se la rete non è direttamente connessa.
-   Ora dell'ultimo aggiornamento o creazione della route.
-   Periodo di tempo per cui questa route viene mantenuta nella tabella di routing. Se questa quantità di tempo è scaduta e la route non è stata aggiornata, il gestore tabelle di routing rimuove la route dalla tabella. In questo caso, si dice che la route sia *obsoleta.*
-   Dati specifici della famiglia di protocolli. Questi dati sono trasparenti per RTMv1. Tuttavia, se questi dati cambiano per una route designata come "route migliore", il gestore tabelle di routing invia una notifica di modifica della route.
-   Dati specifici del protocollo di routing. Questi dati sono completamente trasparenti per il gestore tabelle di routing, in questo modo le modifiche a questi dati non causano la notifica delle modifiche di route.

I valori seguenti, insieme, identificano in modo univoco una route nella tabella di routing:

-   Rete di destinazione
-   Identificatore di protocollo
-   Indice dell'interfaccia
-   Indirizzo del router dell'hop successivo

In generale, il gestore tabelle di routing crea voci separate per le route che differiscono in uno qualsiasi di questi valori di parametro. Tuttavia, viene generata un'eccezione per i protocolli di routing che non mantengono più di una voce per ogni rete di destinazione. Per questi protocolli, gestione tabelle di routing ignora le differenze nell'indice dell'interfaccia o nell'indirizzo dell'hop successivo. Un esempio di questo protocollo è l'implementazione RRAS di Open Shortest Path First (OSPF).

 

 




