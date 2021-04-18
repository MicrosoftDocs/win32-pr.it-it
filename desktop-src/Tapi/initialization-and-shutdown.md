---
description: Per fare in modo che un'applicazione possa usare una qualsiasi delle funzioni telefoniche aggiuntive, è necessaria una connessione a TAPI, tramite la quale può ricevere messaggi.
ms.assetid: c0211f64-4f73-4348-ae49-9a898d3aa093
title: Inizializzazione e arresto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6831b8cfda84ac564450caec554191198fd4c21f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308602"
---
# <a name="initialization-and-shutdown"></a>Inizializzazione e arresto

Per fare in modo che un'applicazione usi qualsiasi funzione telefono supplementare di TAPI, è necessaria una connessione a TAPI, tramite la quale può ricevere messaggi. L'applicazione stabilisce la connessione tramite la funzione [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) . In questa funzione, l'applicazione specifica il meccanismo di notifica mediante il quale TAPI informa l'applicazione delle modifiche nello stato del telefono e il completamento asincrono delle funzioni telefoniche.

La funzione [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) restituisce due informazioni all'applicazione: un *handle dell'applicazione* e il numero di dispositivi telefonici. L'handle dell'applicazione rappresenta l'utilizzo dell'applicazione di TAPI. Le funzioni TAPI che usano handle di telefono non richiedono l'handle dell'applicazione, perché questo handle viene derivato dall'handle telefonico specificato.

Il secondo elemento di informazioni restituito da [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) è il numero di dispositivi telefonici disponibili per TAPI. I dispositivi telefonici sono identificati dall'identificatore del dispositivo (*ID dispositivo*). Gli identificatori di dispositivo validi sono compresi tra zero e il numero di dispositivi telefonici meno uno. Se, ad esempio, **phoneInitializeEx** segnala che in un sistema sono presenti due dispositivi telefonici, gli identificatori validi per i dispositivi telefonici sono 0 e 1. Al termine dell'applicazione usando le funzioni telefoniche di TAPI, viene richiamato [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown), passando il relativo handle dell'applicazione per arrestare l'utilizzo di TAPI. Questo consente a TAPI di liberare tutte le risorse assegnate all'applicazione.

Le applicazioni non devono richiamare [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) senza aprire successivamente un telefono (almeno per il monitoraggio). Se l'applicazione non monitora e non usa dispositivi, deve chiamare [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown) in modo che le risorse di memoria allocate dalla libreria a collegamento dinamico TAPI possano essere rilasciate se non necessario e la libreria stessa può essere scaricata dalla memoria, ma non necessaria.

Sia [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) che [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown) funzionano in modo sincrono. Ovvero, queste funzioni restituiscono un'indicazione di esito positivo o negativo e non restituiscono mai un identificatore di richiesta asincrono.

 

 



