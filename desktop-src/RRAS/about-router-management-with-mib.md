---
title: Informazioni sulla gestione dei router con MIB
description: Le API MIB (Management Information Base) per la gestione dei router rendono possibile eseguire query e impostare i valori delle variabili MIB esportate da uno dei gestori di router o da uno dei protocolli di routing utilizzati dal gestore router.
ms.assetid: d0fafd82-e7cb-4524-a499-d14830f02b21
keywords:
- Routing, Management Information Base
- Routing, Management Information Base, descritto
- Management Information Base RRAS
- MIB
- MIB, vedere Management Information Base
- Management Information Base RRAS
- Management Information Base RRAS , descritto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a867d903e0fb79f9360dc5f1cb485040ed4489b328365bc2daa063a35fbe27d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792196"
---
# <a name="about-router-management-with-mib"></a>Informazioni sulla gestione dei router con MIB

Le API MIB (Management Information Base) per la gestione dei router rendono possibile eseguire query e impostare i valori delle variabili MIB esportate da uno dei gestori di router o da uno dei protocolli di routing utilizzati dal gestore router. Usando questa API, il router supporta il Simple Network Management Protocol (SNMP).

Nel framework SNMP ogni oggetto gestibile nel router è rappresentato da una variabile con un identificatore di oggetto (OID) univoco. Corrispondente a ogni OID è un valore che rappresenta lo stato corrente dell'oggetto. La raccolta di OID e valori è detta MIB (Management Information Base). Le chiamate MprAdminMib consentono a uno sviluppatore di specificare un oggetto in base al relativo OID e di eseguire query o scrivere ("Set") il valore dell'oggetto.

Per eseguire query e impostare variabili MIB, il modulo che esegue le chiamate deve definire un set di strutture di dati. Queste strutture di dati includono strutture da usare come identificatori di oggetto e strutture che contengono i valori delle variabili MIB a cui si accede. Queste strutture di dati sono opache per tutti gli elementi, ad esempio il chiamante della funzione MIB e il modulo che ha gestito la chiamata.

Il modulo che si sta servindo della chiamata MIB è un gestore di router o uno dei protocolli di routing. Il chiamante deve specificare un gestore router anche se la chiamata viene gestita da uno dei protocolli di routing. In tal caso, il chiamante deve specificare il gestore router corrispondente alla famiglia di protocolli per tale protocollo di routing. Ad esempio, se il protocollo di routing OSPF (Open Shortest Path First) gestisce la chiamata MIB, il chiamante dovrà specificare Gestione router IP, poiché OSPF appartiene alla famiglia di protocolli IP. In ognuna delle funzioni MIB il *parametro dwTransportId* specifica un gestore router e il *parametro RoutingPid* specifica il protocollo di routing. Il gestore router ha anche un *RoutingPid* univoco, poiché alcune delle variabili MIB possono essere gestite dal gestore router stesso.

Le funzioni MprAdminMib possono essere chiamate in un computer diverso da quello amministrato. Le funzioni MprAdminMIB che estraeno o scrivono valori accettano come parametro un handle per il computer da amministrare. Usare la [**funzione MprAdminMIBServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibserverconnect) per stabilire la connessione al computer remoto e ottenere questo handle. Dopo aver chiamato le funzioni MprAdminMIB necessarie per eseguire una particolare attività amministrativa, chiamare la [**funzione MprAdminMIBServerDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibserverdisconnect) per terminare la connessione al computer remoto.

Le [**funzioni MprAdminMIBEntryCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrycreate) e [**MprAdminMIBEntrySet**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentryset) accettano come parametri un OID e un buffer che contiene il nuovo valore per l'oggetto.

Le [**funzioni MprAdminMIBEntryGet**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentryget), [**MprAdminMIBEntryGetFirst**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetfirst) e [**MprAdminMIBEntryGetNext**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetnext) accettano come parametri un OID e l'indirizzo di una variabile puntatore. In caso di esito positivo, la variabile puntatore punta a un buffer che contiene il valore per l'oggetto. Il chiamante deve liberare la memoria per questo buffer chiamando la [**funzione MprAdminMIBBufferFree.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibbufferfree)

Le [**funzioni MprAdminMIBEntryGetFirst**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetfirst) e [**MprAdminMIBEntryGetNext**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetnext) consentono a uno sviluppatore di eseguire una *procedura SNMP.* Poiché gli OID sono ordinati, ogni OID e pertanto ogni oggetto gestibile ha *un* OID successivo. Una procedura SNMP si riferisce all'attraversamento di una parte dell'MIB leggendo o scrivendo una sequenza di OID.

Tutte le chiamate MprAdminMib passano attraverso Dynamic Interface Manager (DIM). A seconda dell'OID, DIM passa la chiamata a uno dei gestori di router. SIA IP che IPX supportano SNMP. Anche in questo caso, a seconda dell'OID, il gestore del router può gestire la chiamata stessa o passare la chiamata a uno dei client. Tutti i client router devono implementare ed esportare le funzioni seguenti che corrispondono alle funzioni MprAdminMIB denominate in modo analogo:

-   [**MibCreate**](/windows/desktop/api/Routprot/nc-routprot-pmib_create)
-   [**MibDelete**](/windows/desktop/api/Routprot/nc-routprot-pmib_delete)
-   [**MibSet**](/windows/desktop/api/Routprot/nc-routprot-pmib_set)
-   [**MibGet**](/windows/desktop/api/Routprot/nc-routprot-pmib_get)
-   [**MibGetFirst**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_first)
-   [**MibGetNext**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_next)
-   [**MibGetTrapInfo**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_trap_info)
-   [**MibSetTrapInfo**](/windows/desktop/api/Routprot/nc-routprot-pmib_set_trap_info)

 

 




