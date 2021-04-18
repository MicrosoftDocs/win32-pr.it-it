---
description: .
ms.assetid: a6ea76e6-9721-453a-a657-96f53660e09d
title: API Sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c4d6fd7805607afa80fcee27568004906a0a8e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306364"
---
# <a name="sensor-api"></a>API Sensor

## <a name="purpose"></a>Scopo

Windows 7 include il supporto nativo per i sensori, ovvero dispositivi che possono misurare fenomeni fisici come temperatura o località. Questa documentazione descrive l'API del sensore, che consente alle applicazioni di ottenere e usare i dati dei sensori in modo standardizzato.

Per quanto riguarda gli utenti, ci affidiamo a tutti i nostri sensi per fornire informazioni sul mondo. Quando creiamo dei computer da intraprendere per alcune attività, aggiungiamo i meccanismi dei sensori in modo che i computer possano rispondere in modo appropriato alle condizioni mutevoli.

Ad esempio, i motori delle automobili usano in genere un'ampia gamma di sensori. Questi sensori vengono monitorati da un computer onboarding che regola continuamente le impostazioni, ad esempio la tempistica del motore, per massimizzare la potenza e l'efficienza. Un televisore può utilizzare un sensore di luce ambiente per regolare la luminosità dell'immagine in modo che corrisponda alle mutevoli condizioni della stanza. Anche qualcosa di semplice come un pulsante del campanello funge da sensore rudimentale per rilevare una presenza umana sullo sportello.

Mentre il campanello puramente meccanico soddisfa lo scopo, le informazioni fornite dai sensori complessi diventano molto più potenti quando vengono combinate con il software. I sensori moderni possono fornire una grande quantità di dati molto rapidamente e in un'ampia gamma di formati, quindi il software fornisce un meccanismo naturale per il rilevamento dei dati del sensore.

Attualmente, gli sviluppatori di software possono scrivere programmi che usano i sensori, ma la mancanza di standardizzazione rende la programmazione per i sensori un'attività ardua. Al termine di un programma basato su sensori, in genere è sempre dipendente da un particolare tipo di hardware. L'uso di una o più soluzioni verticali per consentire la distribuzione di un sistema basato su software ha limitato l'integrazione dei sensori con l'hardware del computer e, fino a questo momento, i computer basati su Windows non hanno avuto alcuna eccezione.

Windows 7 include il supporto nativo per i sensori, espanso da una nuova piattaforma di sviluppo per l'uso dei sensori, inclusi i sensori di posizione, ad esempio i dispositivi GPS. La piattaforma sensore e posizione di Windows offre ai produttori di dispositivi un modo standard per esporre i dispositivi sensori agli sviluppatori e ai consumer di software, fornendo allo stesso tempo agli sviluppatori un Application Programming Interface standardizzato (API) per l'uso di sensori e dati di sensori.

I sensori sono dispositivi o meccanismi che consentono di misurare i fenomeni fisici, fornire dati descrittivi o fornire informazioni sullo stato di un oggetto fisico o di un ambiente. I computer possono usare i sensori incorporati, i sensori connessi tramite connessioni cablate o wireless o i sensori che forniscono dati attraverso una rete o Internet.

L'API Sensor fornisce un modo standard per accedere a livello di codice ai dati forniti dai sensori. L'API del sensore standardizza:

-   Categorie, tipi e proprietà del sensore.
-   Formati di dati per i tipi di sensore standard.
-   Interfacce COM per l'utilizzo di sensori e raccolte di sensori.
-   Meccanismi di evento per la ricezione asincrona di dati del sensore.

L'API del sensore consente inoltre di definire categorie, tipi, proprietà, formati di dati ed eventi personalizzati del sensore.

## <a name="developer-audience"></a>Sviluppatori

L'API del sensore fornisce le funzionalità tramite un set di interfacce COM. In questa documentazione si presuppone che l'utente abbia familiarità con la programmazione mediante il linguaggio di programmazione C++ e che si disponga di una conoscenza di base di come utilizzare le interfacce e gli oggetti COM. Per motivi di brevità, molti esempi di codice in questa documentazione (oltre agli esempi di codice) utilizzano oggetti Active Template Library (ATL) per implementare la funzionalità COM.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Per iniziare](getting-started.md)
-   [Informazioni sull'API del sensore](about-the-sensor-api.md)
-   [Guida alla programmazione dell'API del sensore](sensor-api-programming-guide.md)
-   [Informazioni di riferimento sulla programmazione dell'API del sensore](sensor-api-programming-reference.md)

 

 



