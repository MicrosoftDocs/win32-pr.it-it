---
title: L'interfaccia utente di Edge viene eliminata negli scenari "in-out-in" e "inerzia"
description: L'interfaccia utente di Edge viene eliminata negli scenari "in-out-in" e "inerzia"
ms.assetid: 005B6D03-52A6-4780-8D3E-4A5CDA5EED8C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec032fa97f54fc1b1325055c9b02bdebe9e817b0f85971c2e2a7062e93c284c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593961"
---
# <a name="edge-ui-is-suppressed-in-in-out-in-and-inertia-scenarios"></a>L'interfaccia utente di Edge viene eliminata negli scenari "in-out-in" e "inerzia"

## <a name="platform"></a>Piattaforma

<dl> Client - Windows 8.1  
</dl>

## <a name="description"></a>Descrizione

In alcuni casi gli utenti possono richiamare involontariamente l'interfaccia utente di Edge (accessi, barra dell'app, cambio di app). È stata introdotta una funzionalità che consente agli sviluppatori di progettare la propria interfaccia utente per l'intero schermo senza fare gli affordance (ad esempio, i bordi) per impedire all'utente di raggiungere accidentalmente i bordi.

Esistono due casi che potrebbero portare più spesso a scorrimenti rapidi perimetrali accidentali:

-   Durante la panoramica veloce, la velocità e l'imprecisione dell'interazione possono occasionalmente causare l'accesso dal bordo dello schermo
-   Se gli utenti lasciano rapidamente e entrano di nuovo nell'area dello schermo mentre entrano nell'input penna con il dito, ad esempio in un'app di disegno, questo comportamento in uscita può attivare erroneamente l'interfaccia utente di Edge e interrompere l'esperienza utente

Per migliorare l'esperienza utente e sviluppatore, l'interfaccia utente di Edge verrà ora eliminata in due istanze specifiche:

-   Quando un utente esegue la panoramica in un'applicazione che supporta l'inerzia DManip e scorre all'esterno dello schermo durante l'inerzia, l'interfaccia utente di Edge non verrà richiamata all'interno di una finestra di timeout
-   Nei dispositivi certificati, quando un utente scorre rapidamente dall'interno dello schermo all'esterno dello schermo e all'interno (in uscita) all'interno di determinati parametri, l'interfaccia utente di Edge non verrà richiamata

## <a name="manifestations"></a>Manifestazioni

Gli utenti scorreranno rapidamente verso il bordo durante l'uso di un'app per vedere una diminuzione della chiamata al bordo non intenzionale.

## <a name="solution"></a>Soluzione

Gli sviluppatori devono tenere presenti queste mitigazioni e devono essere in grado di usare lo schermo intero senza temere che gli utenti attivino accidentalmente l'interfaccia utente di Edge durante l'interazione con l'applicazione lungo il perimetro.

 

 




