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
# <a name="adding-palette-message-handlers"></a><span data-ttu-id="fbe07-106">Aggiunta di gestori di messaggi della tavolozza</span><span class="sxs-lookup"><span data-stu-id="fbe07-106">Adding Palette Message Handlers</span></span>

<span data-ttu-id="fbe07-107">Nell'esempio seguente vengono illustrati i semplici gestori di messaggi per i messaggi [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) e [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) .</span><span class="sxs-lookup"><span data-stu-id="fbe07-107">The following example illustrates simple message handlers for the [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) and [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) messages.</span></span> <span data-ttu-id="fbe07-108">Nell'esempio viene usata la funzione [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) per elaborare il messaggio **WM \_ QUERYNEWPALETTE** .</span><span class="sxs-lookup"><span data-stu-id="fbe07-108">The example uses the [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) function to process the **WM\_QUERYNEWPALETTE** message.</span></span>

<span data-ttu-id="fbe07-109">L'applicazione deve rispondere al messaggio [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) invalidando la finestra di destinazione per consentire alla funzione [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) di ricreare un'immagine.</span><span class="sxs-lookup"><span data-stu-id="fbe07-109">Your application should respond to the [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) message by invalidating the destination window to let the [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) function redraw an image.</span></span> <span data-ttu-id="fbe07-110">È necessario rispondere al messaggio [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) usando la funzione [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) per realizzare la tavolozza.</span><span class="sxs-lookup"><span data-stu-id="fbe07-110">You should respond to the [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) message by using the [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) function to realize the palette.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="fbe07-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fbe07-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbe07-112">Uso di DrawDib</span><span class="sxs-lookup"><span data-stu-id="fbe07-112">Using DrawDib</span></span>](using-drawdib.md)
</dt> </dl>

 

 