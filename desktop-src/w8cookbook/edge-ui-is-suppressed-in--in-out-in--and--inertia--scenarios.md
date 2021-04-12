---
title: L'interfaccia utente di Edge viene eliminato negli scenari "in-out-in" e "inerzia"
description: L'interfaccia utente di Edge viene eliminato negli scenari "in-out-in" e "inerzia"
ms.assetid: 005B6D03-52A6-4780-8D3E-4A5CDA5EED8C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef08eab653349beab0710d59d45bedc2874ced44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221986"
---
# <a name="edge-ui-is-suppressed-in-in-out-in-and-inertia-scenarios"></a>L'interfaccia utente di Edge viene eliminato negli scenari "in-out-in" e "inerzia"

## <a name="platform"></a>Piattaforma

<dl> Client-Windows 8.1  
</dl>

## <a name="description"></a>Descrizione

Ci sono casi in cui gli utenti possono richiamare inavvertitamente l'interfaccia utente Edge (Charm, barra dell'app, cambio di app). È stata introdotta una funzionalità che consente agli sviluppatori di progettare l'interfaccia utente per l'intero schermo senza apportare affordances (ad esempio, bordi) per impedire all'utente di raggiungere accidentalmente i bordi.

Esistono due casi che potrebbero condurre più spesso a inavvertitamente i bordi del bordo:

-   In una rapida panoramica, la velocità e l'imprecisione dell'interazione possono occasionalmente comportarne il ritorno dal bordo dello schermo
-   Se gli utenti lasciano e rientrano rapidamente nell'area dello schermo mentre Inking con il dito, ad esempio, in un'app per la creazione di un disegno, questo comportamento in uscita può attivare erroneamente l'interfaccia utente di Edge e interrompere l'esperienza utente

Per migliorare l'esperienza degli utenti e degli sviluppatori, l'interfaccia utente di Edge verrà ora rilevata in due istanze specifiche:

-   Quando un utente esegue la panoramica in un'applicazione che supporta l'inerzia DManip e scorre all'esterno dello schermo mentre è in corso l'inerzia, l'interfaccia utente perimetrale non verrà richiamata entro una finestra di timeout
-   Nei dispositivi certificati, quando un utente scorre rapidamente dall'interno dello schermo all'esterno dello schermo e torna all'interno (movimento in uscita) all'interno di determinati parametri, l'interfaccia utente di Edge non verrà richiamata

## <a name="manifestations"></a>Manifestazioni

Quando si usa un'app, gli utenti possono scorrere rapidamente i dispositivi con una riduzione della chiamata al bordo involontario.

## <a name="solution"></a>Soluzione

Gli sviluppatori devono tenere presenti queste mitigazioni e dovrebbero essere in grado di usare l'intero schermo senza temere che gli utenti inneschino accidentalmente l'interfaccia utente di Edge mentre interagiscono con l'applicazione lungo il perimetro.

 

 




