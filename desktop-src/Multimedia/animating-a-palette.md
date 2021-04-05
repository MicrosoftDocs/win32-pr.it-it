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
# <a name="animating-a-palette"></a>Animazione di una tavolozza

Nell'esempio seguente viene animata una tavolozza utilizzando le funzioni [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize), [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette)e [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) .

È possibile modificare i colori di una bitmap usando la funzione [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) in combinazione con [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette). Per consentire le modifiche della tavolozza, specificare prima di tutto il \_ flag DDF animate nella chiamata a **DrawDibBegin**. In secondo luogo, impostare i valori della tabella dei colori dalle voci della tavolozza usando **DrawDibChangePalette**.

Ad esempio, se *lppe* è un indirizzo della matrice [PaletteEntry](/previous-versions//ms532623(v=vs.85)) contenente i nuovi colori e *lpbi* è la struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) utilizzata in [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) o [**DRAWDIBDRAW**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw), il frammento seguente aggiorna la tabella dei colori DIB.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di DrawDib](using-drawdib.md)
</dt> </dl>

 

 