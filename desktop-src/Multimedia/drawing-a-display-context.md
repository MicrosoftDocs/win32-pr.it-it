---
title: Creazione di un contesto di visualizzazione
description: Creazione di un contesto di visualizzazione
ms.assetid: c3328375-faa3-4b29-a155-8a25cc62269f
keywords:
- DrawDib, contesto di dispositivo (DC)
- DrawDib, disegno di controller di dominio
- DrawDibRealize (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1c79c2b7bb938cc34527b23cfc66fda6d19503
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044682"
---
# <a name="drawing-a-display-context"></a><span data-ttu-id="97877-106">Creazione di un contesto di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="97877-106">Drawing a Display Context</span></span>

<span data-ttu-id="97877-107">Nell'esempio seguente viene preparato un controller di dominio DrawDib utilizzando la funzione [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) prima di visualizzare diverse immagini in una sequenza bitmap.</span><span class="sxs-lookup"><span data-stu-id="97877-107">The following example prepares a DrawDib DC by using the [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) function prior to displaying several images in a bitmap sequence.</span></span>


```C++
hdc = GetDC(hwnd); 
DrawDibBegin(hdd, hdc, dxDest, dyDest, lpbi, dxSrc, dySrc, NULL); 
DrawDibRealize(hdd, hdc, fBackground); 
DrawDibDraw(hdd, hdc, xDst, yDst, dxDst, dyDst, lpbi, lpBits, 
    xSrc, ySrc, dxSrc, dySrc, DDF_SAME_DRAW|DDF_SAME_HDC); 
DrawDibDraw(hdd, hdc, xDst, yDst, dxDst, dyDst, lpbi, lpBits, 
    xSrc, ySrc, dxSrc, dySrc, DDF_SAME_DRAW|DDF_SAME_HDC); 
DrawDibDraw(hdd, hdc, xDst, yDst, dxDst, dyDst, lpbi, lpBits, 
    xSrc, ySrc, dxSrc, dySrc, DDF_SAME_DRAW|DDF_SAME_HDC); 
ReleaseDC(hwnd, hdc); 

```



## <a name="related-topics"></a><span data-ttu-id="97877-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="97877-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97877-109">Uso di DrawDib</span><span class="sxs-lookup"><span data-stu-id="97877-109">Using DrawDib</span></span>](using-drawdib.md)
</dt> </dl>

 

 




