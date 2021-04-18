---
description: Il modello di programmazione della telefonia Microsoft astrae il controllo delle comunicazioni dal controllo dei dispositivi, liberando le applicazioni degli utenti finali e i produttori di dispositivi dalla necessità di procedere in contemporanea.
ms.assetid: 07dd8447-08dc-4ae3-9a22-70e914c392db
title: Modello di programmazione di telefonia Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efb8947f3b428ab4a252301e3fdd5f94e29f6ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305586"
---
# <a name="microsoft-telephony-programming-model"></a>Modello di programmazione di telefonia Microsoft

Il modello di programmazione della telefonia Microsoft astrae il controllo delle comunicazioni dal controllo dei dispositivi, liberando le applicazioni degli utenti finali e i produttori di dispositivi dalla necessità di procedere in contemporanea. Utilizzando questo modello, un'applicazione server o un utente finale non richiede informazioni dettagliate sul controllo del dispositivo e non è necessario che il dispositivo sia personalizzato per l'applicazione. Le applicazioni e i dispositivi possono essere sottoposti a Innovation and Change senza renderli inutili ai clienti.

Il diagramma seguente illustra il modo in cui questa astrazione viene eseguita.

![come TAPI astrae il controllo delle comunicazioni dal controllo del dispositivo](images/tapicomp.png)

Questi componenti possono essere visualizzati come repository di conoscenze specializzate. L'applicazione TAPI (Telephony Application Programming Interface) è in grado di riconoscere le esigenze degli utenti, la DLL TAPI e TAPISRV comprendere la telefonia generale e i provider di servizi (TSP e MSP) conoscono il controllo dei dispositivi dettagliato. Gli sviluppatori di applicazioni e i produttori di dispositivi richiedono solo una conoscenza generale degli altri requisiti.

-   Un'applicazione carica la DLL TAPI nello spazio di elaborazione e USA TAPI per comunicare le esigenze.
-   TAPI stabilisce le comunicazioni di collegamento RPC con il server TAPI.
-   Inoltre, TAPI 3. x crea un oggetto MSP e comunica con esso utilizzando un set di comandi definito, Media Service Provider Interface (MSPI).
-   Quando un'applicazione chiama un'operazione TAPI, la libreria a collegamento dinamico TAPI convalida ed effettua il marshalling dei parametri, quindi le invia a TAPISRV.
-   TAPISRV tiene traccia delle risorse di comunicazione disponibili per il computer locale e le interfacce con i provider di servizi di telefonia (TSPs) tramite l'interfaccia di telefonia del provider di servizi (TSPI).
-   Le comunicazioni tra un TSP e un MSP avvengono utilizzando una connessione virtuale che passa attraverso la DLL TAPI e TAPISRV.
-   La coppia TSP/MSP fornisce informazioni sullo stato e sulle funzionalità del dispositivo e implementa i comandi specifici richiesti per una risposta desiderata.

Il risultato dell'uso di questo modello di programmazione è che le applicazioni possono ignorare o modificare le modifiche apportate ai dispositivi e i nuovi dispositivi possono essere immediatamente utili anziché attendere le modifiche di base del codice. La potenziale quota di mercato viene espansa sia per writer di applicazioni che per produttori di dispositivi.

Gli argomenti seguenti descrivono i componenti di telefonia Microsoft in modo più dettagliato:

-   [Applicazioni TAPI](tapi-applications.md)
-   [DLL TAPI](tapi-dll.md)
-   [Server TAPI](tapi-server.md)
-   [Provider di servizi](service-providers.md)
-   [Modello sincrono/asincrono](synchronous-asynchronous-model.md)
-   [Strutture di dati TAPI](tapi-data-structures.md)
-   [Livelli di servizio TAPI](tapi-levels-of-service.md)

 

 



