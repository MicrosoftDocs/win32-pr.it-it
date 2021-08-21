---
title: Aggiunta di gestori di messaggi del riquadro
description: Aggiunta di gestori di messaggi del riquadro
ms.assetid: bfd77f42-6a9d-4195-b1a0-1688e44358e3
keywords:
- DrawDib, tavolozze
- Funzione DrawDibRealize
- Funzione DrawDibDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5b17512025cadf0e457b596a3bfc07399db4eb9185195f4c836ee154d5ff64a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808631"
---
# <a name="adding-palette-message-handlers"></a>Aggiunta di gestori di messaggi del riquadro

L'esempio seguente illustra semplici gestori di messaggi per i [**messaggi WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) e [**WM \_ QUERYNEWPALETTE.**](/windows/desktop/gdi/wm-querynewpalette) Nell'esempio viene [**utilizzata la funzione DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) per elaborare il **messaggio WM \_ QUERYNEWPALETTE.**

L'applicazione deve rispondere al [**messaggio WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) invalidando la finestra di destinazione per consentire alla funzione [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) di ridisegnare un'immagine. È necessario rispondere al [**messaggio WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) usando la [**funzione DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) per realizzare il riquadro.


```C++
case WM_PALETTECHANGED: 
    if ((HWND)wParam == hwnd) 
        break; 
case WM_QUERYNEWPALETTE: 
    hdc = GetDC(hwnd); 
    f = DrawDibRealize(hdd, hdc, FALSE) > 0; 
    ReleaseDC(hwnd, hdc); 
    if (f) 
        InvalidateRect(hwnd, NULL, TRUE); 
    break; 

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di DrawDib](using-drawdib.md)
</dt> </dl>

 

 