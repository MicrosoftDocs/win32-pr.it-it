---
title: Comportamento del pool di sistema
description: Discussione sulle azioni eseguite dal pool di sistema quando si inviano notifiche degli eventi e quando non sono in sospeso operazioni biometriche.
ms.assetid: cc1f8ffa-ce69-48ff-8509-81d85807d12a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a82d957b2b1b4968835eec1482662e30765e4a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396098"
---
# <a name="system-pool-behavior"></a>Comportamento del pool di sistema

Nella discussione seguente vengono evidenziate le azioni eseguite dal pool di sistema quando si inviano notifiche sugli eventi e quando non sono in sospeso operazioni biometriche.

## <a name="event-dispatching"></a>Invio di eventi

Quando un'unità biometrica genera una notifica di evento, il pool di sistema utilizza un filtro a catena per inviare l'avviso e assegnargli uno dei seguenti livelli di priorità:

-   La priorità alta viene assegnata alle richieste esplicite di corrispondenza e registrazione generate dai client.
-   La priorità media viene assegnata a eventi di registrazione o di corrispondenza imprevisti o non recuperati.
-   Per gli eventi di navigazione viene assegnata una priorità bassa.

Gli eventi di acquisizione vengono recapitati nella sequenza seguente:

-   Se la finestra di stato attivo corrente è in attesa di un'operazione di corrispondenza o di registrazione, l'esempio viene elaborato e inviato al client proprietario della finestra attiva corrente.
-   Se l'evento Capture non è stato recuperato dalla finestra di stato attivo corrente e un gestore eventi non attestato è stato registrato con il servizio biometrico di Windows, l'evento Capture viene inviato a questo gestore.
-   Se l'evento rimane non recuperato, viene ignorato.

Se l'evento è un evento di navigazione e un gestore eventi di navigazione è stato registrato con il servizio biometrico di Windows, l'evento Capture viene inviato a questo gestore. Se non è presente alcun gestore eventi, l'evento viene ignorato.

## <a name="idle-mode"></a>Modalità di inattività

Quando non sono presenti client in attesa del completamento delle richieste di registrazione o di corrispondenza esplicita, il pool di sistema determina se generare automaticamente richieste di acquisizione ripetute e inviare l'avviso di evento risultante al gestore eventi non reclamato oppure attendere gli eventi di navigazione e inviarli al gestore eventi di navigazione.

Se un gestore eventi non attestato è stato registrato con il servizio biometrico di Windows, il pool di sistema esegue le azioni seguenti:

-   La modalità di navigazione per il sensore è disabilitata.
-   Le operazioni non richieste vengono inviate al gestore eventi indipendentemente dallo stato attivo della finestra.
-   Se non sono presenti richieste in attesa di un'operazione biometrica, viene eseguita un'acquisizione automatica.

Se un gestore di spostamento è stato registrato con il servizio biometrico di Windows, il pool di sistema esegue le operazioni seguenti:

-   Le unità biometriche nel pool di sistema vengono posizionate in uno stato di navigazione se non sono presenti operazioni biometriche in sospeso.
-   Gli eventi di navigazione sono disabilitati se un client invia una corrispondenza o un evento di registrazione.
-   Se è stato registrato un gestore eventi non attestati, gli eventi di navigazione sono disabilitati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pool di sensori privati](private-sensor-pool.md)
</dt> <dt>

[Pool di sensori](sensor-pools.md)
</dt> <dt>

[Pool di sensori di sistema](system-sensor-pool.md)
</dt> </dl>

 

 




