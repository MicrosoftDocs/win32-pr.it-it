---
title: Gestione finestre desktop
description: La funzionalità di composizione desktop, introdotta in Windows Vista, ha cambiato fondamentalmente il modo in cui le applicazioni visualizzano i pixel sullo schermo.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_overview.htm
keywords:
- Gestione finestre desktop (DWM),about
- DWM (Gestione finestre desktop),about
- Gestione finestre desktop (DWM), composizione
- DWM (Gestione finestre desktop),composizione
- composizione desktop
- Composizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8259be171f225cc955546314febdff5395a47318499b830ee855bc8b985b025
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456041"
---
# <a name="desktop-window-manager"></a>Gestione finestre desktop

La funzionalità di composizione desktop, introdotta in Windows Vista, ha cambiato fondamentalmente il modo in cui le applicazioni visualizzano i pixel sullo schermo. Quando la composizione desktop è abilitata, le singole finestre non vengono più disegnate direttamente sullo schermo o sul dispositivo di visualizzazione principale come nelle versioni precedenti di Windows. Al contrario, il loro disegno viene reindirizzato alle superfici fuori schermo nella memoria video, di cui viene eseguito il rendering in un'immagine desktop e presentate sullo schermo.

La composizione desktop viene eseguita dal Gestione finestre desktop (DWM). Tramite la composizione desktop, DWM consente effetti visivi sul desktop, nonché varie funzionalità, ad esempio fotogrammi finestra effetto cristallo, animazioni di transizione di finestra 3D, Windows capovolgimento e capovolgimento Windows Flip3D e supporto ad alta risoluzione.

Il Gestione finestre desktop viene eseguito come Windows servizio. Può essere abilitato e disabilitato tramite l'elemento Strumenti Pannello di controllo, in Servizi, come Gestione finestre desktop Sessione.

Molte delle funzionalità DWM possono essere controllate o accessibili da un'applicazione tramite le API DWM. La documentazione seguente descrive le funzionalità e i requisiti delle API DWM.

-   [Panoramiche di DWM](desktop-window-manager-overviews.md)
-   [Codice di esempio DWM](dwm-samples.md)
-   [Informazioni di riferimento su DWM](reference.md)

 

 




