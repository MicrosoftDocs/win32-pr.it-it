---
title: Oggetto Gestione finestre desktop
description: La Gestione finestre desktop
ms.assetid: 79250d49-dad5-46c6-892d-b92dac14b417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fca8550134ba0c1cdafe0bd5c349061ef900a9e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103899"
---
# <a name="the-desktop-window-manager"></a>La Gestione finestre desktop

Prima di Windows Vista, un programma Windows disegnava direttamente sullo schermo. In altre parole, il programma scriverà direttamente nel buffer di memoria mostrato dalla scheda video. Questo approccio può causare artefatti visivi se una finestra non si ridisegna correttamente. Ad esempio, se l'utente trascina una finestra su un'altra finestra e la finestra sottostante non si ridisegna abbastanza rapidamente, la finestra in alto può lasciare una traccia:

![screenshot che mostra gli artefatti ridisegnati.](images/graphics04.png)

La traccia è causata dal fatto che entrambe le finestre disegnano nella stessa area di memoria. Mentre la finestra in alto viene trascinata, la finestra sottostante deve essere ridisegnata. Se il ridisegno è troppo lento, causa gli artefatti visualizzati nell'immagine precedente.

Windows Vista ha cambiato fondamentalmente il modo in cui vengono disegnate le finestre, introducendo il Gestione finestre desktop (DWM). Quando DWM è abilitato, una finestra non viene più disegnata direttamente nel buffer di visualizzazione. Al contrario, ogni finestra viene disegnata in un buffer di memoria offscreen, detto anche *superficie offscreen.* DWM quindi composite queste superfici sullo schermo.

![diagramma che mostra come il dwm composita il desktop.](images/graphics05.png)

DWM offre diversi vantaggi rispetto all'architettura grafica precedente.

-   Meno messaggi ridisegnati. Quando una finestra è ostruito da un'altra finestra, non è necessario ridisegnarsi.
-   Artefatti ridotti. In precedenza, il trascinamento di una finestra poteva creare elementi visivi, come descritto.
-   Effetti visivi. Poiché il DWM è responsabile della composizione dello schermo, può eseguire il rendering di aree traslucidi e sfocate della finestra.
-   Ridimensionamento automatico per valori DPI elevati. Anche se il ridimensionamento non è il modo ideale per gestire valori DPI elevati, si tratta di un fallback praticabile per le applicazioni meno recenti che non sono state progettate per le impostazioni DPI elevate. Questo argomento verrà illustrato più avanti, nella sezione [DPI e Device-Independent Pixel.](dpi-and-device-independent-pixels.md)
-   Visualizzazioni alternative. Il DWM può usare le superfici offscreen in vari modi interessanti. Ad esempio, DWM è la tecnologia alla base di Scorrimento finestre 3D, anteprime e transizioni animate.

Si noti, tuttavia, che il DWM non è garantito per essere abilitato. La scheda grafica potrebbe non supportare i requisiti di sistema DWM e gli utenti possono disabilitare DWM tramite il pannello **di controllo Proprietà** del sistema. Ciò significa che il programma non deve basarsi sul comportamento di ridisegno del DWM. Testare il programma con DWM disabilitato per assicurarsi che venga ridisegnato correttamente.

## <a name="next"></a>Prossima

[Modalità mantenuta e modalità immediata](retained-mode-versus-immediate-mode.md)

 

 




