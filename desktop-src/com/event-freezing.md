---
title: Blocco degli eventi
description: Blocco degli eventi
ms.assetid: 1e537503-f7e7-42f4-aa3c-3c71715b84fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba439ebce12a48d78e1eb1d2daa31990c02f4a42082d3425e9b6ef2f842b3ba1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736801"
---
# <a name="event-freezing"></a>Blocco degli eventi

Un contenitore può notificare a un controllo che non è pronto a rispondere agli eventi chiamando [**IOleControl::FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) con **TRUE.** Può sbloccare gli eventi chiamando **FreezeEvents** con **FALSE.** Quando un contenitore blocca gli eventi, blocca l'elaborazione degli eventi, non la ricezione di eventi. ciò significa che un contenitore può comunque ricevere eventi mentre gli eventi sono bloccati. Se un contenitore riceve una notifica degli eventi mentre i relativi eventi sono bloccati, il contenitore deve ignorare l'evento. Non sono appropriate altre azioni.

Un controllo deve prendere nota della chiamata di un contenitore a [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) con **TRUE** se è importante per il controllo che un evento non viene perso. Mentre l'elaborazione degli eventi di un contenitore è bloccata, un controllo deve implementare una delle tecniche seguenti:

-   Genera gli eventi con la piena consapevolezza che il contenitore non esempierà alcuna azione.
-   Elimina tutti gli eventi generati dal controllo.
-   Accodare tutti gli eventi in sospeso e generarli dopo che il contenitore ha chiamato [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) con **FALSE.**
-   Accodare solo gli eventi rilevanti o importanti e generarli dopo che il contenitore ha chiamato [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) con **FALSE.**

Ogni tecnica è accettabile e appropriata in circostanze diverse. Lo sviluppatore del controllo è responsabile della determinazione e dell'implementazione della tecnica appropriata per la funzionalità del controllo.

 

 




