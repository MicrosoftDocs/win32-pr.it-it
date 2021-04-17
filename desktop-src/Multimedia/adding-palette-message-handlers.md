---
title: Aggiunta di gestori di messaggi della tavolozza
description: Aggiunta di gestori di messaggi della tavolozza
ms.assetid: bfd77f42-6a9d-4195-b1a0-1688e44358e3
keywords:
- DrawDib, tavolozze
- DrawDibRealize (funzione)
- DrawDibDraw (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 679990dce5977430eb2a46fc3cd06622246d357f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398987"
---
# <a name="adding-palette-message-handlers"></a>Aggiunta di gestori di messaggi della tavolozza

Nell'esempio seguente vengono illustrati i semplici gestori di messaggi per i messaggi [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) e [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) . Nell'esempio viene usata la funzione [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) per elaborare il messaggio **WM \_ QUERYNEWPALETTE** .

L'applicazione deve rispondere al messaggio [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) invalidando la finestra di destinazione per consentire alla funzione [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) di ricreare un'immagine. È necessario rispondere al messaggio [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) usando la funzione [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) per realizzare la tavolozza.


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

 

 