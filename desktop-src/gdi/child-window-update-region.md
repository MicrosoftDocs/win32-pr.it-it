---
description: Una finestra figlio è una finestra con lo \_ stile WS Child o WS \_ elemento ChildWindow.
ms.assetid: d8110492-c1b9-4b49-9b34-587adb7c65c9
title: Area di aggiornamento della finestra figlio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b92e6cba93c3be253b8ed8616bdcf9301e92494
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967069"
---
# <a name="child-window-update-region"></a>Area di aggiornamento della finestra figlio

Una finestra figlio è una finestra con lo \_ stile WS Child o WS \_ elemento ChildWindow. Analogamente ad altri stili della finestra, le finestre figlio ricevono i messaggi di [**\_ disegno WM**](wm-paint.md) per richiedere l'aggiornamento. Ogni finestra figlio dispone di un'area di aggiornamento, che può essere impostata dal sistema o dall'applicazione per generare messaggi di **\_ disegno WM** finali.

L'aggiornamento e le aree visibili di una finestra figlio sono interessati dalla finestra padre del figlio; Questa operazione non è valida per le finestre di altri stili. Il sistema imposta spesso l'area di aggiornamento della finestra figlio quando imposta l'area di aggiornamento della finestra padre, facendo sì che la finestra figlio riceva i messaggi di [**\_ disegno WM**](wm-paint.md) quando la finestra padre li riceve. Il sistema limita la posizione dell'area visibile della finestra figlio all'interno dell'area client della finestra padre e ritaglia qualsiasi parte della finestra figlio spostata all'esterno della finestra padre.

Il sistema imposta l'area di aggiornamento per una finestra figlio ogni volta che una parte dell'area di aggiornamento della finestra padre include una parte della finestra figlio. In questi casi, il sistema invia prima di tutto un messaggio di [**\_ disegno WM**](wm-paint.md) alla finestra padre e quindi Invia un messaggio alla finestra figlio, consentendo al figlio di ripristinare tutte le parti della finestra che l'elemento padre potrebbe avere disegnato.

Il sistema non imposta l'area di aggiornamento del padre quando viene impostata l'elemento figlio. Un'applicazione non è in grado di generare un messaggio di [**\_ disegno WM**](wm-paint.md) per la finestra padre invalidando la finestra figlio. Analogamente, un'applicazione non è in grado di generare un messaggio di **\_ disegno WM** per l'elemento figlio invalidando una parte dell'area client del padre che si trova interamente sotto la finestra figlio. In questi casi, nessuna finestra riceve un messaggio di **\_ disegno WM** .

Un'applicazione può impedire l'impostazione dell'area di aggiornamento di una finestra figlio quando viene impostata la finestra padre specificando lo \_ stile WS CLIPCHILDREN durante la creazione della finestra padre. Quando questo stile è impostato, il sistema esclude le finestre figlio dall'area visibile del padre e pertanto ignora qualsiasi parte dell'area di aggiornamento che può contenere le finestre figlio. Quando l'applicazione viene disegnata nella finestra padre, qualsiasi disegno che coprirebbe la finestra figlio viene troncato, rendendo superfluo il successivo messaggio di disegno [**WM \_**](wm-paint.md) alla finestra figlio.

Anche l'aggiornamento e le aree visibili di una finestra figlio sono interessati dagli elementi di pari livello della finestra figlio. Le finestre di pari livello sono tutte finestre con una finestra padre comune. Se le finestre di pari livello si sovrappongono, l'impostazione dell'area di aggiornamento per una ha effetto sull'area di aggiornamento di un'altra, causando l'invio di messaggi di [**\_ disegno WM**](wm-paint.md) a entrambe le finestre. Se una finestra nella catena padre è composta (una finestra con WX \_ ex \_ composita), le finestre di pari livello ricevono i messaggi di **\_ disegno WM** nell'ordine inverso rispetto alla posizione nella z order. Dato questo, la finestra più alta nella z order (nella parte superiore) riceve il messaggio di **\_ disegno WM** per ultimo e viceversa. Se una finestra della catena padre non è composta, Windows di pari livello riceve i messaggi di **\_ disegno WM** in z order.

Le finestre di pari livello non vengono ritagliate automaticamente. Un elemento di pari livello può disegnare su un altro elemento di pari livello sovrapposto anche se la finestra disegnata presenta una posizione più bassa nella z order. Un'applicazione può impedire questo problema specificando lo \_ stile WS CLIPSIBLINGS durante la creazione delle finestre. Quando questo stile è impostato, il sistema esclude tutte le parti di una finestra di pari livello sovrapposte dall'area visibile di una finestra se la finestra di pari livello sovrapposta ha una posizione più alta nella z order.

> [!Note]  
> L'aggiornamento e le aree visibili per le finestre con lo \_ stile WS popup o WS \_ POPUPWINDOW non sono interessate dalle finestre padre.

 

 

 



