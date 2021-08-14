---
title: Comportamento del pool di sistema
description: Discussione sulle azioni eseguite dal pool di sistema quando vengono inviate notifiche di eventi e quando non sono in sospeso operazioni biometriche.
ms.assetid: cc1f8ffa-ce69-48ff-8509-81d85807d12a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923cfff4b36bd14d100ce1f73db455be5261d75dc2c5be1eddc8f9d6af87fce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911594"
---
# <a name="system-pool-behavior"></a>Comportamento del pool di sistema

La discussione seguente evidenzia le azioni eseguite dal pool di sistema quando vengono inviate notifiche di eventi e quando non sono in sospeso operazioni biometriche.

## <a name="event-dispatching"></a>Invio di eventi

Quando un'unità biometrica genera un avviso di evento, il pool di sistema usa un filtro a catena per inviare l'avviso e assegnarle uno dei livelli di priorità seguenti:

-   La priorità alta viene assegnata alle richieste di corrispondenza e registrazione esplicite generate dai client.
-   La priorità media viene assegnata a eventi di corrispondenza o registrazione imprevisti o non reclamati.
-   La priorità bassa viene assegnata agli eventi di navigazione.

Gli eventi di acquisizione vengono recapitati nella sequenza seguente:

-   Se la finestra di stato attivo corrente è in attesa di un'operazione di corrispondenza o di registrazione, l'esempio viene elaborato e inviato al client proprietario della finestra attiva corrente.
-   Se l'evento di acquisizione non viene reclamato dalla finestra di stato attivo corrente ed è stato registrato un gestore eventi non reclamato con il servizio biometrico Windows, l'evento di acquisizione viene inviato a questo gestore.
-   Se l'evento rimane non reclamato, viene eliminato.

Se l'evento è un evento di navigazione ed è stato registrato un gestore eventi di navigazione con il servizio biometrico Windows, l'evento di acquisizione viene inviato a questo gestore. Se non è presente alcun gestore eventi, l'evento viene eliminato.

## <a name="idle-mode"></a>Modalità inattiva

Quando non sono presenti client in attesa del completamento di richieste di corrispondenza o registrazione esplicite, il pool di sistema determina se generare automaticamente richieste di acquisizione ripetute e inviare la notifica dell'evento risultante al gestore eventi non reclamato o attendere gli eventi di navigazione e inviarli al gestore eventi di navigazione.

Se un gestore eventi non reclamato è stato registrato con il servizio biometrico Windows, il pool di sistema esegue le azioni seguenti:

-   La modalità di navigazione per il sensore è disabilitata.
-   Le operazioni non reclamate vengono inviate al gestore eventi indipendentemente dall'attivazione della finestra.
-   Se non sono presenti richieste in sospeso per un'operazione biometrica, viene eseguita un'acquisizione automatica.

Se un gestore di navigazione è stato registrato con il Windows biometrico, il pool di sistema esegue le operazioni seguenti:

-   Le unità biometriche nel pool di sistema vengono inserite in uno stato di navigazione se non sono in sospeso operazioni biometriche.
-   Gli eventi di navigazione sono disabilitati se un avviso di evento di corrispondenza o di registrazione viene inviato da un client.
-   Se è stato registrato un gestore eventi non reclamato, gli eventi di navigazione vengono disabilitati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pool di sensori privati](private-sensor-pool.md)
</dt> <dt>

[Pool di sensori](sensor-pools.md)
</dt> <dt>

[Pool di sensori di sistema](system-sensor-pool.md)
</dt> </dl>

 

 




