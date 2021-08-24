---
description: "Un'applicazione disegna in una finestra in diversi momenti: quando si crea una finestra per la prima volta, quando si modificano le dimensioni della finestra, quando si sposta la finestra da dietro un'altra finestra, quando si riduce al minimo o si massimizza la finestra, quando si visualizzano i dati da un file aperto e quando si scorre, si modifica o si seleziona una parte dei dati visualizzati."
ms.assetid: 4b5d6842-5707-4884-a55a-e09e342cea46
title: Quando disegnare in una finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 832f219ad15fa919715b0f6892b73686237e1c3681e298106db3cefc4a8c3ec0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468091"
---
# <a name="when-to-draw-in-a-window"></a>Quando disegnare in una finestra

Un'applicazione disegna in una finestra in diversi momenti: quando si crea una finestra per la prima volta, quando si modificano le dimensioni della finestra, quando si sposta la finestra da dietro un'altra finestra, quando si riduce al minimo o si massimizza la finestra, quando si visualizzano i dati da un file aperto e quando si scorre, si modifica o si seleziona una parte dei dati visualizzati.

Il sistema gestisce azioni come lo spostamento e il ridimensionamento di una finestra. Se un'azione influisce sul contenuto della finestra, il sistema contrassegna la parte interessata come pronta per l'aggiornamento e, all'opportunità successiva, invia un messaggio [**WM \_ PAINT**](wm-paint.md) alla routine della finestra della finestra. Il messaggio è un segnale per l'applicazione per determinare cosa deve essere aggiornato e per eseguire il disegno necessario.

Alcune azioni vengono gestite dall'applicazione, ad esempio la visualizzazione di file aperti e la selezione dei dati visualizzati. Per queste azioni, un'applicazione può contrassegnare per l'aggiornamento della parte della finestra interessata dall'azione, causando l'invio di un messaggio [**WM \_ PAINT**](wm-paint.md) all'opportunità successiva. Se un'azione richiede feedback immediato, l'applicazione può disegnare mentre l'azione viene eseguita, senza attendere **WM \_ PAINT**. Ad esempio, un'applicazione tipica evidenzia l'area selezionata dall'utente anziché attendere il successivo messaggio **WM \_ PAINT** per aggiornare l'area.

In tutti i casi, un'applicazione può disegnare in una finestra non appena viene creata. Per disegnare nella finestra, l'applicazione deve prima recuperare un handle per un contesto di dispositivo di visualizzazione per la finestra. Idealmente, un'applicazione esegue la maggior parte delle operazioni di disegno durante l'elaborazione dei [**messaggi WM \_ PAINT.**](wm-paint.md) In questo caso, l'applicazione recupera un contesto di dispositivo di visualizzazione chiamando la [**funzione BeginPaint.**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) Se un'applicazione disegna in qualsiasi altro momento, ad esempio all'interno di [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) o durante l'elaborazione di messaggi della tastiera o del mouse, chiama la funzione [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) per recuperare il controller di dominio di visualizzazione.

 

 
