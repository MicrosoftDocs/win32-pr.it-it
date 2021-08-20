---
description: È possibile usare il messaggio WM \_ PAINT per eseguire il disegno necessario per visualizzare le informazioni.
ms.assetid: cc56745f-95d0-4607-a206-1e7ed7109bf0
title: Utilizzo del WM_PAINT messaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1969d5aae7e64ad74d8070c7515daa6e9e782135ce0af54b49c7faab07f5d34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037449"
---
# <a name="using-the-wm_paint-message"></a>Uso del messaggio WM \_ PAINT

È possibile usare il [**messaggio WM \_ PAINT**](wm-paint.md) per eseguire il disegno necessario per visualizzare le informazioni. Poiché il sistema invia messaggi WM PAINT all'applicazione quando la finestra deve essere aggiornata o quando si richiede in modo esplicito un aggiornamento, è possibile consolidare il codice per il disegno nella routine della finestra \_ dell'applicazione. È quindi possibile usare questo codice ogni volta che l'applicazione deve disegnare informazioni nuove o esistenti.

Le sezioni seguenti illustrano diversi modi per usare il messaggio WM \_ PAINT per disegnare in una finestra:

-   [Disegno nell'area client](drawing-in-the-client-area.md)
-   [Ridisegno dell'intera area client](redrawing-the-entire-client-area.md)
-   [Ridisegno nell'area di aggiornamento](redrawing-in-the-update-region.md)
-   [Invalidazione dell'area client](invalidating-the-client-area.md)
-   [Disegno di una finestra ridotta a icona](drawing-a-minimized-window.md)
-   [Disegno di uno sfondo di finestra personalizzato](drawing-a-custom-window-background.md)

 

 



