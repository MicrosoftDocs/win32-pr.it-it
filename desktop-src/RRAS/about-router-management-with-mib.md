---
title: Informazioni sulla gestione dei router con MIB
description: Le API MIB (Management Information Base) per la gestione dei router consentono di eseguire query e impostare i valori delle variabili MIB esportate da uno dei gestori router o da uno dei protocolli di routing del servizio.
ms.assetid: d0fafd82-e7cb-4524-a499-d14830f02b21
keywords:
- Routing, informazioni di gestione-base
- Routing, informazioni di gestione-base, descrizione
- Informazioni di gestione RRAS
- MIB
- MIB, vedere base Information Management
- Informazioni di gestione RRAS
- Informazioni di gestione RRAS, descrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e015dacc0b36a00ab62d42c710551aa368aa59e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711206"
---
# <a name="about-router-management-with-mib"></a>Informazioni sulla gestione dei router con MIB

Le API MIB (Management Information Base) per la gestione dei router consentono di eseguire query e impostare i valori delle variabili MIB esportate da uno dei gestori router o da uno dei protocolli di routing del servizio. Utilizzando questa API, il router supporta il Simple Network Management Protocol (SNMP).

Nel Framework SNMP ogni oggetto gestibile nel router è rappresentato da una variabile con un identificatore di oggetto univoco (OID). Corrispondente a ogni OID è un valore che rappresenta lo stato corrente dell'oggetto. La raccolta di OID e Values viene definita MIB (Management Information Base). Le chiamate MprAdminMib consentono a uno sviluppatore di specificare un oggetto in base al relativo OID e di eseguire una query o scrivere ("impostare") il valore dell'oggetto.

Per eseguire una query e impostare le variabili MIB, il modulo che servizi le chiamate deve definire un set di strutture di dati. Queste strutture di dati includono strutture da usare come identificatori di oggetto e strutture che contengono i valori delle variabili MIB a cui si accede. Queste strutture di dati sono opache per tutti tranne il chiamante della funzione MIB e del modulo che gestisce la chiamata.

Il modulo che gestisce la chiamata MIB è un gestore router o uno dei protocolli di routing. Il chiamante deve specificare una gestione router anche se la chiamata viene gestita da uno dei protocolli di routing. In tal caso, il chiamante deve specificare il gestore router che corrisponde alla famiglia di protocolli per quel protocollo di routing. Se, ad esempio, il protocollo di routing OSPF (Open shorter Path First) stava gestendo la chiamata MIB, il chiamante avrebbe dovuto specificare la gestione router IP, dal momento che OSPF appartiene alla famiglia di protocolli IP. In ognuna delle funzioni MIB, il parametro *dwTransportId* specifica un gestore router e il parametro *RoutingPid* specifica il protocollo di routing. Gestione router dispone inoltre di un *RoutingPid* univoco, dal momento che alcune variabili MIB possono essere gestite dallo stesso gestore di router.

Le funzioni MprAdminMib possono essere chiamate su un computer diverso da quello amministrato. Le funzioni MprAdminMIB che eseguono query o scrivono valori, accettano come parametro un handle per il computer da amministrare. Utilizzare la funzione [**MprAdminMIBServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibserverconnect) per stabilire la connessione al computer remoto e ottenere questo handle. Dopo aver chiamato le funzioni MprAdminMIB necessarie per eseguire una determinata attività amministrativa, chiamare la funzione [**MprAdminMIBServerDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibserverdisconnect) per terminare la connessione al computer remoto.

Le funzioni [**MprAdminMIBEntryCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrycreate) e [**MprAdminMIBEntrySet**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentryset) accettano come parametri un OID e un buffer che contiene il nuovo valore per l'oggetto.

Le funzioni [**MprAdminMIBEntryGet**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentryget), [**MprAdminMIBEntryGetFirst**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetfirst) e [**MPRADMINMIBENTRYGETNEXT**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetnext) accettano come parametri un OID e l'indirizzo di una variabile puntatore. In esito positivo, la variabile puntatore punta a un buffer che contiene il valore per l'oggetto. Il chiamante deve liberare la memoria per questo buffer chiamando la funzione [**MprAdminMIBBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibbufferfree) .

Le funzioni [**MprAdminMIBEntryGetFirst**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetfirst) e [**MprAdminMIBEntryGetNext**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetnext) consentono a uno sviluppatore di eseguire un *percorso SNMP*. Poiché OID sono ordinati, ogni OID e pertanto ogni oggetto gestibile ha un OID *successivo* . Un percorso SNMP si riferisce all'attraversamento di una parte del MIB leggendo o scrivendo una sequenza di OID.

Tutte le chiamate MprAdminMib passano attraverso Dynamic Interface Manager (DIM). A seconda dell'OID, DIM passa la chiamata a uno dei gestori di router. (Sia IP che IPX supportano SNMP). Anche in questo caso, a seconda dell'OID, gestione router può gestire la chiamata stessa oppure passare la chiamata a uno dei client. Tutti i client router sono necessari per implementare ed esportare le funzioni seguenti che corrispondono alle funzioni MprAdminMIB denominate in modo analogo:

-   [**MibCreate**](/windows/desktop/api/Routprot/nc-routprot-pmib_create)
-   [**MibDelete**](/windows/desktop/api/Routprot/nc-routprot-pmib_delete)
-   [**MibSet**](/windows/desktop/api/Routprot/nc-routprot-pmib_set)
-   [**MibGet**](/windows/desktop/api/Routprot/nc-routprot-pmib_get)
-   [**MibGetFirst**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_first)
-   [**MibGetNext**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_next)
-   [**MibGetTrapInfo**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_trap_info)
-   [**MibSetTrapInfo**](/windows/desktop/api/Routprot/nc-routprot-pmib_set_trap_info)

 

 




