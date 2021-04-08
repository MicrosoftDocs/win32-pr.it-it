---
title: Blocco evento
description: Blocco evento
ms.assetid: 1e537503-f7e7-42f4-aa3c-3c71715b84fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e403448d53949c263b8e146961690de1200436c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856045"
---
# <a name="event-freezing"></a>Blocco evento

Un contenitore può notificare a un controllo che non è pronto a rispondere agli eventi chiamando [**IOleControl:: FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) con **true**. Può sbloccare gli eventi chiamando **FreezeEvents** con **false**. Quando un contenitore blocca gli eventi, è in corso il blocco dell'elaborazione degli eventi, non la ricezione di eventi; ovvero, un contenitore può comunque ricevere eventi mentre gli eventi vengono bloccati. Se un contenitore riceve una notifica degli eventi mentre i relativi eventi sono bloccati, il contenitore deve ignorare l'evento. Non sono necessarie altre azioni.

Un controllo deve prendere nota della chiamata di un contenitore a [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) con **true** se è importante per il controllo che un evento non viene perso. Mentre l'elaborazione degli eventi di un contenitore è bloccata, un controllo deve implementare una delle tecniche seguenti:

-   Attivare gli eventi con la massima consapevolezza che il contenitore non eseguirà alcuna azione.
-   Rimuovere tutti gli eventi che il controllo avrebbe generato.
-   Accodare tutti gli eventi in sospeso e attivarli dopo che il contenitore ha chiamato [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) con **false**.
-   Accodare solo gli eventi rilevanti o importanti e attivarli dopo che il contenitore ha chiamato [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) con **false**.

Ogni tecnica è accettabile e appropriata in circostanze diverse. Lo sviluppatore del controllo è responsabile della determinazione e dell'implementazione della tecnica appropriata per la funzionalità del controllo.

 

 




