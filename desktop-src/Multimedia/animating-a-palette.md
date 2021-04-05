---
title: Animazione di una tavolozza
description: Animazione di una tavolozza
ms.assetid: 89493cc3-eca9-407f-99c2-903fba16992c
keywords:
- DrawDib, tavolozze
- DrawDibRealize (funzione)
- DrawDibDraw (funzione)
- DrawDibChangePalette (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e023ba8ee2c4791ebc8c3f2ac7ebf9a198f4a5ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726727"
---
# <a name="animating-a-palette"></a><span data-ttu-id="13cd8-107">Animazione di una tavolozza</span><span class="sxs-lookup"><span data-stu-id="13cd8-107">Animating a Palette</span></span>

<span data-ttu-id="13cd8-108">Nell'esempio seguente viene animata una tavolozza utilizzando le funzioni [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize), [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette)e [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) .</span><span class="sxs-lookup"><span data-stu-id="13cd8-108">The following example animates a palette by using the [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize), [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette), and [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) functions.</span></span>

<span data-ttu-id="13cd8-109">È possibile modificare i colori di una bitmap usando la funzione [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) in combinazione con [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette).</span><span class="sxs-lookup"><span data-stu-id="13cd8-109">You can change the colors of a bitmap by using the [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) function in combination with [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette).</span></span> <span data-ttu-id="13cd8-110">Per consentire le modifiche della tavolozza, specificare prima di tutto il \_ flag DDF animate nella chiamata a **DrawDibBegin**.</span><span class="sxs-lookup"><span data-stu-id="13cd8-110">First, to allow palette changes, specify the DDF\_ANIMATE flag in the call to **DrawDibBegin**.</span></span> <span data-ttu-id="13cd8-111">In secondo luogo, impostare i valori della tabella dei colori dalle voci della tavolozza usando **DrawDibChangePalette**.</span><span class="sxs-lookup"><span data-stu-id="13cd8-111">Second, set the color table values from the palette entries by using **DrawDibChangePalette**.</span></span>

<span data-ttu-id="13cd8-112">Ad esempio, se *lppe* è un indirizzo della matrice [PaletteEntry](/previous-versions//ms532623(v=vs.85)) contenente i nuovi colori e *lpbi* è la struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) utilizzata in [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) o [**DRAWDIBDRAW**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw), il frammento seguente aggiorna la tabella dei colori DIB.</span><span class="sxs-lookup"><span data-stu-id="13cd8-112">For example, if *lppe* is an address of the [PALETTEENTRY](/previous-versions//ms532623(v=vs.85)) array containing the new colors, and *lpbi* is the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure used in [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) or [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw), the following fragment updates the DIB color table.</span></span>


```C++
hdc = GetDC(hwnd); 
DrawDibBegin(hdd, ....., DDF_ANIMATE); 
DrawDibRealize(hdd, hdc, fBackground); 
DrawDibDraw(hdd, hdc, ...., DDF_SAME_DRAW|DDF_SAME_HDC); 
 
// Call to change color. 
DrawDibChangePalette(hDD, iStart, iLen, lppe); 
. 
. 
. 
ReleaseDC(hwnd, hdc); 

```



## <a name="related-topics"></a><span data-ttu-id="13cd8-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="13cd8-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13cd8-114">Uso di DrawDib</span><span class="sxs-lookup"><span data-stu-id="13cd8-114">Using DrawDib</span></span>](using-drawdib.md)
</dt> </dl>

 

 