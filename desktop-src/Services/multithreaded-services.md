---
description: Gestione controllo servizi (SCM) controlla un servizio inviando eventi di controllo del servizio alla routine del gestore di controllo dei servizi.
ms.assetid: 86e04b43-5f6f-409e-ac18-d7efada4d3d3
title: Servizi multithreading
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5795a170f912050d115537407fcb491305a35ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316615"
---
# <a name="multithreaded-services"></a>Servizi multithreading

Gestione controllo servizi (SCM) controlla un servizio inviando eventi di controllo del servizio alla routine del gestore di controllo del servizio. Il servizio deve rispondere per controllare gli eventi in modo tempestivo, in modo che SCM possa tenere traccia dello stato del servizio. Inoltre, lo stato del servizio deve corrispondere alla descrizione dello stato ricevuto dall'SCM.

A causa di questo meccanismo di comunicazione tra un servizio e il controllo SCM, è necessario prestare attenzione quando si usano più thread in un servizio. Quando a un servizio viene richiesto di arrestare il servizio SCM, è necessario attendere la chiusura di tutti i thread prima di segnalare al gestore SCM che il servizio è stato arrestato. In caso contrario, il controllo SCM può diventare confuso sullo stato del servizio e potrebbe non riuscire a arrestarsi correttamente.

Il servizio SCM deve ricevere una notifica che indica che il servizio sta rispondendo all'evento di arresto del controllo e che lo stato di avanzamento viene eseguito durante l'arresto del servizio. Il servizio SCM presuppone che il servizio sia in corso se il servizio risponde (tramite [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)) entro l'intervallo di tempo (hint di attesa) specificato nella precedente chiamata a **SetServiceStatus** e il punto di controllo viene aggiornato in modo che sia maggiore del checkpoint specificato nella precedente chiamata a **SetServiceStatus**.

Se il servizio segnala al gestore SCM che il servizio è stato arrestato prima della chiusura di tutti i thread, è possibile che SCM interpreti questa operazione come una contraddizione. Questo potrebbe causare uno stato in cui il servizio non può essere arrestato o riavviato.

 

 



