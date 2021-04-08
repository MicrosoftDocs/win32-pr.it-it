---
title: Come limitare lo spostamento del dispositivo di scorrimento
description: Come descritto in informazioni sui controlli TrackBar, è possibile impostare parte dell'intervallo TrackBar come intervallo di selezione. Uno degli scopi di un intervallo di selezione potrebbe essere quello di limitare lo spostamento del dispositivo di scorrimento, facendo in modo che alcune parti dell'intervallo completo non superino i limiti.
ms.assetid: 9DD8BB11-EC6F-4695-BA56-5061F6EA5436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5414ddf72c44dcaed85afde349f0b9f813ed0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855706"
---
# <a name="how-to-limit-slider-movement"></a>Come limitare lo spostamento del dispositivo di scorrimento

Come descritto in [informazioni sui controlli TrackBar](trackbar-controls.md), è possibile impostare parte dell'intervallo TrackBar come intervallo di selezione. Uno degli scopi di un intervallo di selezione potrebbe essere quello di limitare lo spostamento del dispositivo di scorrimento, facendo in modo che alcune parti dell'intervallo completo non superino i limiti.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="limit-slider-movement"></a>Limita movimento dispositivo di scorrimento

Il codice di esempio seguente limita lo spostamento del dispositivo di scorrimento reimpostando la posizione del dispositivo di scorrimento ogni volta che viene spostato al di fuori dell'intervallo di selezione.


```
case WM_HSCROLL:
    {
        HWND hTrackbar = GetDlgItem(hDlg, IDC_SLIDER1);
        
        if (hTrackbar == (HWND)lParam)
        {
            int newPos    = SendMessage(hTrackbar, TBM_GETPOS, 0, 0);
            int selStart  = SendMessage(hTrackbar, TBM_GETSELSTART, 0, 0);
            int selEnd    = SendMessage(hTrackbar, TBM_GETSELEND, 0, 0);
            
            if (newPos > selEnd)
            {
                SendMessage(hTrackbar, TBM_SETPOS, (WPARAM)TRUE, (LPARAM)selEnd);
            }
            
            else if (newPos < selStart)
            {
                SendMessage(hTrackbar, TBM_SETPOS, (WPARAM)TRUE, (LPARAM)selStart);
            }
        }
        
        break;
    }
```



## <a name="remarks"></a>Commenti

Questo frammento di codice fa parte di una procedura della finestra di dialogo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di controlli TrackBar](using-trackbar-controls.md)
</dt> </dl>

 

 




