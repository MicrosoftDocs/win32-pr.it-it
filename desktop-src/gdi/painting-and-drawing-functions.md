---
description: Le funzioni seguenti vengono usate con il disegno e il disegno.
ms.assetid: ec18323e-c13b-4328-83bf-9e4ed4a712b8
title: Funzioni di disegno e disegno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 162ce40c88766a81320f72ea7c2e4a84dd92c478
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978482"
---
# <a name="painting-and-drawing-functions"></a>Funzioni di disegno e disegno

Le funzioni seguenti vengono usate con il disegno e il disegno.



| Funzione                                       | Descrizione                                                                                                 |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)               | Prepara una finestra per il disegno.                                                                             |
| [**DrawAnimatedRects**](/windows/desktop/api/Winuser/nf-winuser-drawanimatedrects) | Disegna un rettangolo e lo aggiunge un'animazione per indicare un'icona o un'attività della finestra.                                      |
| [**DrawCaption**](/windows/desktop/api/Winuser/nf-winuser-drawcaption)             | Disegna una didascalia della finestra.                                                                                     |
| [**DrawEdge**](/windows/desktop/api/Winuser/nf-winuser-drawedge)                   | Disegna uno o più bordi del rettangolo.                                                                       |
| [**DrawFocusRect**](/windows/desktop/api/Winuser/nf-winuser-drawfocusrect)         | Disegna un rettangolo nello stile che indica che il rettangolo ha lo stato attivo.                                  |
| [**DrawFrameControl**](/windows/desktop/api/Winuser/nf-winuser-drawframecontrol)   | Disegna un controllo frame.                                                                                      |
| [**DrawState**](/windows/desktop/api/Winuser/nf-winuser-drawstatea)                 | Visualizza un'immagine e applica un effetto visivo per indicare uno stato.                                          |
| [**DrawStateProc**](/windows/desktop/api/Winuser/nc-winuser-drawstateproc)         | Funzione di callback che esegue il rendering di un'immagine complessa per [**DrawState**](/windows/desktop/api/Winuser/nf-winuser-drawstatea).                        |
| [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint)                   | Contrassegna la fine del disegno in una finestra.                                                                      |
| [**ExcludeUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn)   | Impedisce il disegno all'interno di aree non valide di una finestra.                                                          |
| [**GdiFlush**](/windows/desktop/api/Wingdi/nf-wingdi-gdiflush)                   | Scarica il batch corrente del thread chiamante.                                                                 |
| [**GdiGetBatchLimit**](/windows/desktop/api/Wingdi/nf-wingdi-gdigetbatchlimit)   | Restituisce il numero massimo di chiamate di funzione che è possibile accumulare nel batch corrente del thread chiamante. |
| [**GdiSetBatchLimit**](/windows/desktop/api/Wingdi/nf-wingdi-gdisetbatchlimit)   | Imposta il numero massimo di chiamate di funzione che è possibile accumulare nel batch corrente del thread chiamante.    |
| [**GetBkColor**](/windows/desktop/api/Wingdi/nf-wingdi-getbkcolor)               | Restituisce il colore di sfondo per un contesto di dispositivo.                                                          |
| [**GetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode)                 | Restituisce la modalità di combinazione dello sfondo per un contesto di dispositivo.                                                       |
| [**GetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect)         | Ottiene il rettangolo di delimitazione accumulato per un contesto di dispositivo.                                               |
| [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2)                     | Ottiene la modalità di combinazione in primo piano di un contesto di dispositivo.                                                           |
| [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect)         | Ottiene le coordinate del rettangolo più piccolo che racchiude l'area di aggiornamento di una finestra.                 |
| [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn)           | Ottiene l'area di aggiornamento di una finestra.                                                                         |
| [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)             | Ottiene il contesto di dispositivo per una finestra, tra cui la barra del titolo, i menu e le barre di scorrimento.                          |
| [**GetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-getwindowrgn)           | Ottiene una copia dell'area della finestra di una finestra.                                                               |
| [**GetWindowRgnBox**](/windows/desktop/api/Winuser/nf-winuser-getwindowrgnbox)     | Ottiene le dimensioni del rettangolo di delimitazione più stretto per l'area della finestra di una finestra.                   |
| [**GrayString**](/windows/desktop/api/Winuser/nf-winuser-graystringa)               | Disegna il testo grigio in una posizione.                                                                              |
| [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect)       | Aggiunge un rettangolo all'area di aggiornamento di una finestra.                                                               |
| [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn)         | Invalida l'area client all'interno di un'area.                                                                |
| [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate)   | Disabilita o Abilita il disegno in una finestra.                                                                    |
| [**OutputProc**](/windows/desktop/api/Winuser/nc-winuser-graystringproc)               | Funzione di callback utilizzata con la funzione [**GrayString**](/windows/desktop/api/Winuser/nf-winuser-graystringa) . Viene usato per creare una stringa.   |
| [**PaintDesktop**](/windows/desktop/api/Winuser/nf-winuser-paintdesktop)           | Riempie l'area di visualizzazione in un contesto di dispositivo con un modello.                                               |
| [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)           | Aggiorna un'area nell'area client di una finestra.                                                                 |
| [**SetBkColor**](/windows/desktop/api/Wingdi/nf-wingdi-setbkcolor)               | Imposta lo sfondo su un valore di colore.                                                                       |
| [**SetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode)                 | Imposta la modalità di combinazione dello sfondo di un contesto di dispositivo.                                                           |
| [**SetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect)         | Controlla l'accumulo delle informazioni sul rettangolo di delimitazione per un contesto di dispositivo.                           |
| [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2)                     | Imposta la modalità di combinazione in primo piano.                                                                               |
| [**SetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn)           | Imposta l'area della finestra di una finestra.                                                                         |
| [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow)           | Aggiorna l'area client di una finestra.                                                                        |
| [**ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect)           | Convalida l'area client all'interno di un rettangolo.                                                               |
| [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn)             | Convalida l'area client all'interno di un'area.                                                                  |
| [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc)           | Restituisce un handle per la finestra associata a un contesto di dispositivo.                                            |



 

 

 



