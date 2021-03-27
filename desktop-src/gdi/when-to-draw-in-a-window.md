---
description: "Un'applicazione viene disegnata in una finestra a diverse volte: quando si crea una finestra per la prima volta, quando si modificano le dimensioni della finestra, quando si sposta la finestra da un'altra finestra, quando si riducono o si ottimizza la finestra, quando si visualizzano i dati da un file aperto e quando si scorre, si modifica o si seleziona una parte dei dati visualizzati."
ms.assetid: 4b5d6842-5707-4884-a55a-e09e342cea46
title: Quando creare un oggetto in una finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42c8c157de5a591be5ad1a6ad3e319cf83220e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345136"
---
# <a name="when-to-draw-in-a-window"></a>Quando creare un oggetto in una finestra

Un'applicazione viene disegnata in una finestra a diverse volte: quando si crea una finestra per la prima volta, quando si modificano le dimensioni della finestra, quando si sposta la finestra da un'altra finestra, quando si riducono o si ottimizza la finestra, quando si visualizzano i dati da un file aperto e quando si scorre, si modifica o si seleziona una parte dei dati visualizzati.

Il sistema gestisce le azioni, ad esempio lo stato di trasferimento e il ridimensionamento di una finestra Se un'azione influisce sul contenuto della finestra, il sistema contrassegna la parte interessata della finestra come pronta per l'aggiornamento e, alla successiva opportunità, invia un messaggio [**di \_ disegno WM**](wm-paint.md) alla routine della finestra. Il messaggio è un segnale all'applicazione per determinare quali elementi devono essere aggiornati e per eseguire il disegno necessario.

Alcune azioni sono gestite dall'applicazione, ad esempio la visualizzazione di file aperti e la selezione dei dati visualizzati. Per queste azioni, un'applicazione può contrassegnare l'aggiornamento della parte della finestra interessata dall'azione, causando l'invio di un messaggio di [**\_ disegno WM**](wm-paint.md) alla successiva opportunità. Se un'azione richiede un feedback immediato, l'applicazione può disegnare mentre viene eseguita l'azione, senza attendere **il \_ disegno WM**. Ad esempio, in un'applicazione tipica viene evidenziata l'area selezionata dall'utente anziché attendere il successivo messaggio di **\_ disegno WM** per aggiornare l'area.

In tutti i casi, un'applicazione può creare in una finestra non appena viene creata. Per creare la finestra, l'applicazione deve prima recuperare un handle per un contesto di dispositivo di visualizzazione per la finestra. Idealmente, un'applicazione esegue la maggior parte delle operazioni di disegno durante l'elaborazione dei messaggi di disegno [**WM \_**](wm-paint.md) . In questo caso, l'applicazione recupera un contesto di dispositivo di visualizzazione chiamando la funzione [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) . Se un'applicazione viene disegnata in qualsiasi altro momento, ad esempio all'interno di [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) o durante l'elaborazione dei messaggi della tastiera o del mouse, viene chiamata la funzione [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) per recuperare il controller di dominio di visualizzazione.

 

 
