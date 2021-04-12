---
title: Gestione finestre desktop
description: .
ms.assetid: 79250d49-dad5-46c6-892d-b92dac14b417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73167b762a9952eb508f09e70f3d4183b3b7a018
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329791"
---
# <a name="the-desktop-window-manager"></a>Gestione finestre desktop

Prima di Windows Vista, un programma di Windows veniva disegnato direttamente sullo schermo. In altre parole, il programma scrive direttamente nel buffer di memoria visualizzato dalla scheda video. Questo approccio può provocare artefatti visivi se una finestra non viene ridisegnata correttamente. Se, ad esempio, l'utente trascina una finestra su un'altra finestra e la finestra sottostante non viene ridisegnata abbastanza rapidamente, la finestra in primo piano può uscire da una traccia:

![screenshot che Mostra gli artefatti di ridisegno.](images/graphics04.png)

Il percorso è dovuto al fatto che entrambe le finestre disegnano nella stessa area di memoria. Quando la finestra in primo piano viene trascinata, la finestra sottostante deve essere ridisegnata. Se il ridisegno è troppo lento, causa gli artefatti mostrati nell'immagine precedente.

Windows Vista ha modificato in modo sostanziale il modo in cui vengono disegnate le finestre, introducendo il Gestione finestre desktop (DWM). Quando DWM è abilitato, una finestra non viene più disegnata direttamente nel buffer di visualizzazione. Ogni finestra viene invece disegnata in un buffer di memoria Offscreen, detto anche *superficie Offscreen*. DWM quindi compone queste superfici sullo schermo.

![diagramma che illustra il modo in cui DWM compone il desktop.](images/graphics05.png)

DWM offre diversi vantaggi rispetto all'architettura grafica precedente.

-   Meno messaggi di ridisegno. Quando una finestra è ostruita da un'altra finestra, non è necessario che la finestra ostruita venga ridisegnata.
-   Elementi ridotti. In precedenza, il trascinamento di una finestra poteva creare artefatti visivi, come descritto.
-   Effetti visivi. Poiché DWM è responsabile della composizione dello schermo, può eseguire il rendering delle aree trasparenti e sfocate della finestra.
-   Ridimensionamento automatico per valori DPI alti. Sebbene il ridimensionamento non sia il modo ideale per gestire valori DPI elevati, è un fallback valido per le applicazioni meno recenti che non sono state progettate per impostazioni DPI elevate. Si tornerà a questo argomento in un secondo momento, nella sezione [dpi e Device-Independent pixel](dpi-and-device-independent-pixels.md).
-   Visualizzazioni alternative. DWM può utilizzare le superfici Offscreen in diversi modi interessanti. Ad esempio, DWM è la tecnologia alla base di Windows Flip 3D, anteprime e transizioni animate.

Si noti, tuttavia, che non è garantita l'abilitazione di DWM. La scheda grafica potrebbe non supportare i requisiti di sistema DWM e gli utenti possono disabilitare DWM tramite il pannello di controllo **Proprietà sistema** . Ciò significa che il programma non deve basarsi sul comportamento di ridisegno di DWM. Testare il programma con DWM disabilitato per assicurarsi che venga ridisegnato correttamente.

## <a name="next"></a>Prossima

[Modalità mantenuta rispetto alla modalità immediata](retained-mode-versus-immediate-mode.md)

 

 




