---
description: Una finestra figlio è una finestra con lo stile \_ WS CHILD o WS \_ CHILDWINDOW.
ms.assetid: d8110492-c1b9-4b49-9b34-587adb7c65c9
title: Area di aggiornamento della finestra figlio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf702855e506424a08e5be6c6b0cfe514035f1c54348306475140fb7fc440a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105896"
---
# <a name="child-window-update-region"></a>Area di aggiornamento della finestra figlio

Una finestra figlio è una finestra con lo stile \_ WS CHILD o WS \_ CHILDWINDOW. Analogamente ad altri stili di finestra, le finestre figlio ricevono [**messaggi WM \_ PAINT**](wm-paint.md) per richiedere l'aggiornamento. Ogni finestra figlio ha un'area di aggiornamento, che il sistema o l'applicazione può impostare per generare eventuali **messaggi WM \_ PAINT.**

Le aree visibili e di aggiornamento di una finestra figlio sono interessate dalla finestra padre dell'elemento figlio. Questo non vale per le finestre di altri stili. Il sistema imposta spesso l'area di aggiornamento della finestra figlio quando imposta l'area di aggiornamento della finestra padre, facendo in modo che la finestra figlio riceva messaggi [**WM \_ PAINT**](wm-paint.md) quando la finestra padre li riceve. Il sistema limita la posizione dell'area visibile della finestra figlio all'interno dell'area client della finestra padre e ritaglia qualsiasi parte della finestra figlio spostata all'esterno della finestra padre.

Il sistema imposta l'area di aggiornamento per una finestra figlio ogni volta che una parte dell'area di aggiornamento della finestra padre include una parte della finestra figlio. In questi casi, il sistema invia innanzitutto un messaggio [**WM \_ PAINT**](wm-paint.md) alla finestra padre e quindi invia un messaggio alla finestra figlio, consentendo all'elemento figlio di ripristinare tutte le parti della finestra che l'elemento padre potrebbe avere disegnato.

Il sistema non imposta l'area di aggiornamento dell'elemento padre quando è impostata la proprietà dell'elemento figlio. Un'applicazione non può generare [**\_ un messaggio WM PAINT**](wm-paint.md) per la finestra padre invalidando la finestra figlio. Analogamente, un'applicazione non può generare un messaggio **WM \_ PAINT** per l'elemento figlio invalidando una parte dell'area client dell'elemento padre che si trova interamente sotto la finestra figlio. In questi casi, nessuna delle due finestre riceve un **messaggio WM \_ PAINT.**

Un'applicazione può impedire l'impostazione dell'area di aggiornamento di una finestra figlio quando la proprietà della finestra padre è impostata specificando lo stile WS CLIPCHILDREN durante la creazione della \_ finestra padre. Quando questo stile è impostato, il sistema esclude le finestre figlio dall'area visibile dell'elemento padre e pertanto ignora qualsiasi parte dell'area di aggiornamento che può contenere le finestre figlio. Quando l'applicazione disegna nella finestra padre, qualsiasi disegno che copre la finestra figlio viene ritagliato, rendendo non necessario un messaggio [**WM \_ PAINT**](wm-paint.md) successivo alla finestra figlio.

Anche le aree di aggiornamento e visibili di una finestra figlio sono interessate dagli elementi di pari livello della finestra figlio. Le finestre di pari livello sono tutte le finestre con una finestra padre comune. Se le finestre di pari livello si sovrappongono, l'impostazione dell'area di aggiornamento per una influisce sull'area di aggiornamento di un'altra, causando l'invio di messaggi [**WM \_ PAINT**](wm-paint.md) a entrambe le finestre. Se viene composita una finestra nella catena padre (una finestra con WX EX COMPOSITED), le finestre di pari livello ricevono messaggi WM PAINT in ordine inverso della relativa posizione \_ \_ nell'ordine **\_** Z. In questo caso, la finestra più in alto nell'ordine Z (in alto) riceve il messaggio **WM \_ PAINT** per ultimo e viceversa. Se una finestra nella catena padre non è composta, le finestre di pari livello ricevono messaggi **WM \_ PAINT** in ordine Z.

Le finestre di pari livello non vengono ritagliate automaticamente. Un elemento di pari livello può disegnare su un altro elemento di pari livello sovrapposto anche se la finestra che sta disegnando ha una posizione inferiore nell'ordine Z. Un'applicazione può evitare questo problema specificando lo stile WS \_ CLIPSIBLINGS durante la creazione delle finestre. Quando questo stile è impostato, il sistema esclude tutte le parti di una finestra di pari livello sovrapposta dall'area visibile di una finestra se la finestra di pari livello sovrapposta ha una posizione superiore nell'ordine Z.

> [!Note]  
> Le aree di aggiornamento e visibili per le finestre con lo stile WS POPUP o \_ WS POPUPWINDOW non sono interessate dalle finestre \_ padre.

 

 

 



