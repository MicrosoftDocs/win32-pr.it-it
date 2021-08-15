---
description: API Sensor
ms.assetid: a6ea76e6-9721-453a-a657-96f53660e09d
title: API Sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc5c3fd3cbdbf2aac9a161a6cb8bc150d2828c2d48a346b94843878cda49a6a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889672"
---
# <a name="sensor-api"></a>API Sensor

## <a name="purpose"></a>Scopo

Windows 7 include il supporto nativo per i sensori, ovvero dispositivi in grado di misurare i fenomenali fisici, ad esempio la temperatura o la posizione. Questa documentazione descrive l'API Sensor, che consente alle applicazioni di ottenere e usare i dati dai sensori in modo standardizzato.

Come esseri umani, ci affidiamo ai nostri sensi per fornire informazioni sul mondo che ci circonda. Quando si creano computer per assumere parte del lavoro, si aggiungono meccanismi di sensori in modo che i computer possano rispondere in modo appropriato alle condizioni mutevoli.

Ad esempio, i motori di automobili usano in genere un'ampia gamma di sensori. Questi sensori vengono monitorati da un computer di bordo che regola continuamente le impostazioni, ad esempio la temporizzazione del motore, per ottimizzare la potenza e l'efficienza. Un tv può usare un sensore di luce ambientale per regolare la luminosità dell'immagine in base alle condizioni del locale. Anche qualcosa di semplice come un pulsante del campanello funge da sensore rudimentale per rilevare una presenza umana alla porta.

Mentre il campanello puramente meccanico soddisfa lo scopo, le informazioni fornite da sensori complessi diventano molto più potenti quando vengono combinate con il software. I sensori moderni possono fornire molti dati molto rapidamente e in diversi formati, quindi il software offre un meccanismo naturale per dare un senso ai dati dei sensori.

Attualmente, gli sviluppatori di software possono scrivere programmi che usano sensori, ma la mancanza di standardizzazione rende la programmazione per i sensori un'attività difficile. Dopo il completamento, un programma basato su sensori dipende in genere da un particolare tipo di hardware. L'uso di una o più soluzioni verticali per abilitare la distribuzione di un sistema basato su software ha limitato l'integrazione dei sensori con l'hardware del computer e finora i computer basati Windows non hanno fatto eccezione.

Windows 7 include il supporto nativo per i sensori, ampliato da una nuova piattaforma di sviluppo per l'uso dei sensori, inclusi i sensori di posizione, ad esempio i dispositivi GPS. La piattaforma Windows Sensor and Location offre ai produttori di dispositivi un modo standard per esporre i dispositivi dei sensori agli sviluppatori di software e ai consumer, fornendo allo stesso tempo agli sviluppatori un'API (Application Programming Interface) standardizzata per l'uso di sensori e dati dei sensori.

I sensori sono dispositivi o meccanismi che possono misurare i fenomenali fisici, fornire dati descrittivi o fornire informazioni sullo stato di un oggetto fisico o di un ambiente. I computer possono usare sensori predefiniti, sensori connessi tramite connessioni cablate o wireless o sensori che forniscono dati tramite una rete o Internet.

L'API Sensor offre un modo standard per accedere a livello di codice ai dati forniti dai sensori. L'API Sensor standardizza:

-   Categorie, tipi e proprietà dei sensori.
-   Formati di dati per i tipi di sensori standard.
-   Interfacce COM per l'uso di sensori e raccolte di sensori.
-   Meccanismi di evento per la ricezione asincrona dei dati del sensore.

L'API Sensor consente anche di definire categorie, tipi, proprietà, formati di dati ed eventi dei sensori personalizzati.

## <a name="developer-audience"></a>Sviluppatori

L'API Sensor fornisce le funzionalità tramite un set di interfacce COM. Questa documentazione presuppone che si abbia una conoscenza funzionante della programmazione con il linguaggio di programmazione C++ e si abbia una conoscenza di base di come usare oggetti e interfacce COM. Per motivi di brevità, molti esempi di codice in questa documentazione (nonché negli esempi di codice) usano oggetti Active Template Library (ATL) per implementare la funzionalità COM.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Per iniziare](getting-started.md)
-   [Informazioni sull'API Sensor](about-the-sensor-api.md)
-   [Guida alla programmazione delle API dei sensori](sensor-api-programming-guide.md)
-   [Informazioni di riferimento sulla programmazione delle API dei sensori](sensor-api-programming-reference.md)

 

 



