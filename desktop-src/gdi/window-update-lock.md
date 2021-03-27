---
description: Un blocco di aggiornamento della finestra è una sospensione temporanea del disegno in una finestra.
ms.assetid: 92b1ba04-ff79-4a37-9633-99412cdafe95
title: Blocco aggiornamento finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4897915020134387947c7a77009c4bdbd63cfdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227137"
---
# <a name="window-update-lock"></a>Blocco aggiornamento finestra

Un *blocco di aggiornamento della finestra* è una sospensione temporanea del disegno in una finestra. Il sistema utilizza il blocco per impedire ad altre finestre di disegnare sul rettangolo di rilevamento ogni volta che l'utente sposta o ridimensiona una finestra. Le applicazioni possono utilizzare il blocco per impedire il disegno se eseguono operazioni di ridimensionamento o di modifica simili con le proprie finestre.

Un'applicazione usa la funzione [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) per impostare o cancellare un blocco di aggiornamento della finestra, specificando la finestra da bloccare. Il blocco si applica alla finestra specificata e a tutte le relative finestre figlio. Quando il blocco viene impostato, le funzioni [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) e [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) restituiscono un contesto di dispositivo di visualizzazione con un'area visibile vuota. Dato questo, l'applicazione può continuare a creare nella finestra, ma tutto l'output viene troncato. Il blocco viene mantenuto finché l'applicazione non la cancella chiamando **LockWindowUpdate**, specificando **null** per la finestra. Sebbene **LockWindowUpdate** forza l'area visibile di una finestra come vuota, la funzione non rende invisibile la finestra specificata e non cancella il \_ bit di stile visibile WS.

Dopo l'impostazione del blocco, l'applicazione può usare la funzione [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) con il valore DCX \_ LOCKWINDOWUPDATE per recuperare un contesto di periferica di visualizzazione da estrarre sulla finestra bloccata. Ciò consente all'applicazione di creare un rettangolo di rilevamento durante l'elaborazione dei messaggi della tastiera o del mouse. Il sistema utilizza questo metodo quando l'utente sposta e ridimensiona le finestre. **GetDCEx** Recupera il contesto del dispositivo di visualizzazione dalla cache del contesto del dispositivo di visualizzazione, in modo che l'applicazione debba rilasciare il contesto di dispositivo appena possibile dopo il disegno.

Quando viene impostato un blocco di aggiornamento della finestra, il sistema crea un rettangolo di delimitazione accumulato per ogni finestra bloccata. Quando il blocco viene cancellato, il sistema utilizza questo rettangolo di delimitazione per impostare l'area di aggiornamento per la finestra e le relative finestre figlio, forzando un messaggio di [**\_ disegno WM**](wm-paint.md) finale. Se il rettangolo di delimitazione accumulato è vuoto, ovvero se non si è verificato alcun disegno durante l'impostazione del blocco, l'area di aggiornamento non viene impostata.

 

 



