---
title: Animazione di una tavolozza
description: Animazione di una tavolozza
ms.assetid: 89493cc3-eca9-407f-99c2-903fba16992c
keywords:
- DrawDib, tavolozze
- Funzione DrawDibRealize
- Funzione DrawDibDraw
- Funzione DrawDibChangePalette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be9613e4e648fad0b1fafe5d48d091ab13c9b6c358eda4a858c1d5517ab8fc5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808421"
---
# <a name="animating-a-palette"></a>Animazione di una tavolozza

Nell'esempio seguente viene animata una tavolozza usando le funzioni [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize), [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette)e [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) .

È possibile modificare i colori di una bitmap usando la [**funzione DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) in combinazione con [**DrawDibChangePalette.**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette) Prima di tutto, per consentire le modifiche alla tavolozza, specificare il flag DDF \_ ANIMATE nella chiamata a **DrawDibBegin.** Impostare quindi i valori della tabella dei colori dalle voci della tavolozza usando **DrawDibChangePalette.**

Ad esempio, se *lppe* è un indirizzo della matrice [PALETTEENTRY](/previous-versions//ms532623(v=vs.85)) contenente i nuovi colori e *lpbi* è la struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) usata in [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) o [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw), il frammento seguente aggiorna la tabella dei colori DIB.


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

 

 