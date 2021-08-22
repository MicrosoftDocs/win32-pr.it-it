---
description: Il modello di programmazione Di telefonia Microsoft astrae il controllo delle comunicazioni dal controllo dei dispositivi, liberando le applicazioni degli utenti finali e i produttori di dispositivi dalla necessità di marzo in blocco.
ms.assetid: 07dd8447-08dc-4ae3-9a22-70e914c392db
title: Modello di programmazione di telefonia Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33407069c8ff489006c3cb85e03b676126eca1abedf484d9d1bb5b1305677a15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518646"
---
# <a name="microsoft-telephony-programming-model"></a>Modello di programmazione di telefonia Microsoft

Il modello di programmazione Di telefonia Microsoft astrae il controllo delle comunicazioni dal controllo dei dispositivi, liberando le applicazioni degli utenti finali e i produttori di dispositivi dalla necessità di marzo in blocco. Usando questo modello, un'applicazione server o dell'utente finale non richiede informazioni dettagliate sul controllo del dispositivo e non è necessario adattare il dispositivo all'applicazione. Le applicazioni e i dispositivi possono essere sottoposti a innovazione e modifiche senza rendersi inutili per i clienti.

Il diagramma seguente illustra come viene eseguita questa astrazione.

![come Tapi astrae il controllo delle comunicazioni dal controllo del dispositivo](images/tapicomp.png)

Questi componenti possono essere visualizzati come repository di conoscenze specializzate. L'applicazione TAPI (Telefonia Application Programming Interface) riconosce le esigenze dell'utente, la DLL TAPI e TAPISRV comprendono la telefonia generale e i provider di servizi (TSP e MSP) conoscono il controllo dettagliato dei dispositivi. Gli autori di applicazioni e i produttori di dispositivi richiedono solo una conoscenza generale dei requisiti reciproci.

-   Un'applicazione carica la DLL TAPI nello spazio di elaborazione e usa TAPI per comunicare le esigenze.
-   TAPI stabilisce una comunicazione di collegamento RPC con il server TAPI.
-   TAPI 3.x crea inoltre un oggetto MSP e comunica con esso usando un set definito di comandi, l'interfaccia MSPI (Media Service Provider Interface).
-   Quando un'applicazione chiama un'operazione TAPI, la libreria a collegamento dinamico TAPI convalida ed effettua il marshalling dei parametri, quindi inoltra le informazioni a TAPISRV.
-   TAPISRV tiene traccia delle risorse di comunicazione disponibili per il computer locale e delle interfacce con i provider di servizi di telefonia (TSP) tramite TSPI (Telefonia Service Provider Interface).
-   Le comunicazioni tra un provider di servizi di configurazione e un provider di servizi di configurazione si verificano usando una connessione virtuale che passa attraverso la DLL TAPI e TAPISRV.
-   La coppia TSP/MSP fornisce informazioni sullo stato e sulle funzionalità del dispositivo e implementa i comandi specifici necessari per una risposta desiderata.

Il risultato dell'uso di questo modello di programmazione è che le applicazioni possono ignorare o adattarsi alle modifiche del dispositivo e i nuovi dispositivi possono essere immediatamente utili invece di attendere le modifiche alla codebase. La quota di mercato potenziale viene espansa sia per gli autori di applicazioni che per i produttori di dispositivi.

Gli argomenti seguenti descrivono i componenti di Telefonia Microsoft in modo più dettagliato:

-   [Applicazioni TAPI](tapi-applications.md)
-   [TAPI DLL](tapi-dll.md)
-   [TAPI Server](tapi-server.md)
-   [Fornitori](service-providers.md)
-   [Modello sincrono/asincrono](synchronous-asynchronous-model.md)
-   [Strutture dei dati TAPI](tapi-data-structures.md)
-   [Livelli di servizio TAPI](tapi-levels-of-service.md)

 

 



