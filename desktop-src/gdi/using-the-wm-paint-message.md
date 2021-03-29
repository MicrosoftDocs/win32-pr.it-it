---
description: È possibile utilizzare il \_ messaggio di disegno WM per eseguire il disegno necessario per la visualizzazione delle informazioni.
ms.assetid: cc56745f-95d0-4607-a206-1e7ed7109bf0
title: Uso del messaggio WM_PAINT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba77246e04effc74de8158aef9bfc4aaf27471c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227140"
---
# <a name="using-the-wm_paint-message"></a>Uso del \_ messaggio di disegno WM

È possibile utilizzare il [**messaggio \_ di disegno WM**](wm-paint.md) per eseguire il disegno necessario per la visualizzazione delle informazioni. Poiché il sistema invia \_ messaggi di disegno WM all'applicazione quando è necessario aggiornare la finestra o quando si richiede in modo esplicito un aggiornamento, è possibile consolidare il codice per il disegno nella routine della finestra dell'applicazione. È quindi possibile usare questo codice ogni volta che l'applicazione deve creare informazioni nuove o esistenti.

Le sezioni seguenti illustrano diversi modi per usare il \_ messaggio di disegno WM per disegnare in una finestra:

-   [Disegno nell'area client](drawing-in-the-client-area.md)
-   [Ridisegno dell'intera area client](redrawing-the-entire-client-area.md)
-   [Ridisegno nell'area di aggiornamento](redrawing-in-the-update-region.md)
-   [Invalidare l'area client](invalidating-the-client-area.md)
-   [Disegno di una finestra ridotta a icona](drawing-a-minimized-window.md)
-   [Disegno di uno sfondo personalizzato della finestra](drawing-a-custom-window-background.md)

 

 



