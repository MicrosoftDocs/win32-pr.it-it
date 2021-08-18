---
description: Gestione controllo servizi controlla un servizio inviando eventi di controllo del servizio alla routine del gestore del controllo dei servizi.
ms.assetid: 86e04b43-5f6f-409e-ac18-d7efada4d3d3
title: Servizi multithreading
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32b4b51f740e0a3773115b9048ec34619910936f1531fba1260740df28873b67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003729"
---
# <a name="multithreaded-services"></a>Servizi multithreading

Gestione controllo servizi controlla un servizio inviando eventi di controllo del servizio alla routine del gestore del controllo del servizio. Il servizio deve rispondere agli eventi di controllo in modo che SCM possa tenere traccia dello stato del servizio. Inoltre, lo stato del servizio deve corrispondere alla descrizione del relativo stato ricevuto da Gestione controllo servizi.

A causa di questo meccanismo di comunicazione tra un servizio e Gestione controllo servizi, è necessario prestare attenzione quando si utilizzano più thread in un servizio. Quando a un servizio viene richiesto di arrestarsi da Gestione controllo servizi, è necessario attendere la chiusura di tutti i thread prima di segnalare a Gestione controllo servizi che il servizio è stato arrestato. In caso contrario, gestione controllo servizi può confondersi sullo stato del servizio e potrebbe non riuscire ad arrestarsi correttamente.

Gestione controllo servizi deve ricevere una notifica che il servizio risponde all'evento di arresto del controllo e che è in corso l'arresto del servizio. Gestione configurazione server presupporrà che il servizio sia in corso se il servizio risponde (tramite [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)) entro il tempo (hint di attesa) specificato nella chiamata precedente a **SetServiceStatus** e il punto di controllo viene aggiornato in modo da essere maggiore del checkpoint specificato nella chiamata precedente a **SetServiceStatus.**

Se il servizio segnala a Gestione controllo servizi che il servizio è stato arrestato prima dell'uscita di tutti i thread, è possibile che gestione controllo servizi interpreti questa operazione come un'operazione di questo tipo. Ciò potrebbe comportare uno stato in cui il servizio non può essere arrestato o riavviato.

 

 



