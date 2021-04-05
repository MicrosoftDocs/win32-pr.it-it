---
title: Gestione finestre desktop
description: La funzionalità di composizione desktop, introdotta in Windows Vista, ha cambiato radicalmente il modo in cui le applicazioni visualizzano i pixel sullo schermo.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_overview.htm
keywords:
- Gestione finestre desktop (DWM), informazioni
- DWM (Gestione finestre desktop), informazioni
- Gestione finestre desktop (DWM), composizione
- DWM (Gestione finestre desktop), composizione
- composizione del desktop
- Composizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8578001aebf1c73e6d400ffae383674a8432c399
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711191"
---
# <a name="desktop-window-manager"></a>Gestione finestre desktop

La funzionalità di composizione desktop, introdotta in Windows Vista, ha cambiato radicalmente il modo in cui le applicazioni visualizzano i pixel sullo schermo. Quando è abilitata la composizione del desktop, le singole finestre non vengono più riportate direttamente sullo schermo o sul dispositivo di visualizzazione principale come nelle versioni precedenti di Windows. Il disegno viene invece reindirizzato alle superfici fuori schermo nella memoria video, che vengono quindi sottoposte a rendering in un'immagine desktop e visualizzate sullo schermo.

La composizione del desktop viene eseguita dal Gestione finestre desktop (DWM). Grazie alla composizione del desktop, DWM consente effetti visivi sul desktop, nonché diverse funzionalità, ad esempio la cornice della finestra, le animazioni di transizione delle finestre 3D, Windows Flip e Windows Flip3D e un supporto ad alta risoluzione.

Il Gestione finestre desktop viene eseguito come servizio Windows. Può essere abilitata e disabilitata tramite l'elemento del pannello di controllo strumenti di amministrazione, in servizi, come Gestione finestre desktop gestione sessioni.

Molte delle funzionalità di DWM possono essere controllate o accessibili da un'applicazione tramite le API di DWM. Nella documentazione seguente vengono descritte le caratteristiche e i requisiti delle API DWM.

-   [Panoramica di DWM](desktop-window-manager-overviews.md)
-   [Esempio di codice DWM](dwm-samples.md)
-   [Riferimento per DWM](reference.md)

 

 




