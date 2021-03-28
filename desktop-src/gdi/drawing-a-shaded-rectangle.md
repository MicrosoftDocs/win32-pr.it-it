---
description: Per creare un rettangolo ombreggiato, definire una matrice TRIVERTEX con due elementi e una singola struttura Rect della SFUMAtura \_ . Nell'esempio di codice riportato di seguito viene illustrato come creare un rettangolo ombreggiato utilizzando la funzione GradientFill con la \_ \_ modalità Rect Fill Gradient definita.
ms.assetid: a4277e22-03f8-470f-87e9-5aeab258b6d2
title: Disegno di un rettangolo ombreggiato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 665e76c730ada1bd8efc9967fd10e550f0aa2e8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528362"
---
# <a name="drawing-a-shaded-rectangle"></a><span data-ttu-id="fa814-104">Disegno di un rettangolo ombreggiato</span><span class="sxs-lookup"><span data-stu-id="fa814-104">Drawing a Shaded Rectangle</span></span>

<span data-ttu-id="fa814-105">Per creare un rettangolo ombreggiato, definire una matrice [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) con due elementi e una singola [**struttura \_ Rect della sfumatura**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect) .</span><span class="sxs-lookup"><span data-stu-id="fa814-105">To draw a shaded rectangle, define a [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) array with two elements and a single [**GRADIENT\_RECT**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect) structure.</span></span> <span data-ttu-id="fa814-106">Nell'esempio di codice riportato di seguito viene illustrato come creare un rettangolo ombreggiato utilizzando la funzione [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) con la \_ \_ modalità Rect Fill Gradient definita.</span><span class="sxs-lookup"><span data-stu-id="fa814-106">The following code example shows how to draw a shaded rectangle using the [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) function with the GRADIENT\_FILL\_RECT mode defined.</span></span>


```C++
// Create an array of TRIVERTEX structures that describe 
// positional and color values for each vertex. For a rectangle, 
// only two vertices need to be defined: upper-left and lower-right. 
TRIVERTEX vertex[2] ;
vertex[0].x     = 0;
vertex[0].y     = 0;
vertex[0].Red   = 0x0000;
vertex[0].Green = 0x8000;
vertex[0].Blue  = 0x8000;
vertex[0].Alpha = 0x0000;

vertex[1].x     = 300;
vertex[1].y     = 80; 
vertex[1].Red   = 0x0000;
vertex[1].Green = 0xd000;
vertex[1].Blue  = 0xd000;
vertex[1].Alpha = 0x0000;

// Create a GRADIENT_RECT structure that 
// references the TRIVERTEX vertices. 
GRADIENT_RECT gRect;
gRect.UpperLeft  = 0;
gRect.LowerRight = 1;

// Draw a shaded rectangle. 
GradientFill(hdc, vertex, 2, &gRect, 1, GRADIENT_FILL_RECT_H);
```



<span data-ttu-id="fa814-107">Nell'immagine seguente viene illustrato l'output del disegno dell'esempio di codice precedente.</span><span class="sxs-lookup"><span data-stu-id="fa814-107">The following image shows the drawing output of the preceding code example.</span></span>

![illustrazione che mostra un rettangolo con un riempimento sfumato da scuro sul lato sinistro alla luce sul lato destro](images/gradientfillrectangle.png)

## <a name="related-topics"></a><span data-ttu-id="fa814-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fa814-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa814-110">Panoramica di bitmap</span><span class="sxs-lookup"><span data-stu-id="fa814-110">Bitmaps Overview</span></span>](bitmaps.md)
</dt> <dt>

[<span data-ttu-id="fa814-111">Funzioni bitmap</span><span class="sxs-lookup"><span data-stu-id="fa814-111">Bitmap Functions</span></span>](bitmap-functions.md)
</dt> <dt>

[<span data-ttu-id="fa814-112">Disegno di un triangolo ombreggiato</span><span class="sxs-lookup"><span data-stu-id="fa814-112">Drawing a Shaded Triangle</span></span>](drawing-a-shaded-triangle.md)
</dt> <dt>

[<span data-ttu-id="fa814-113">**EMRGRADIENTFILL**</span><span class="sxs-lookup"><span data-stu-id="fa814-113">**EMRGRADIENTFILL**</span></span>](/windows/win32/api/wingdi/ns-wingdi-emrgradientfill)
</dt> <dt>

[<span data-ttu-id="fa814-114">**rettangolo SFUMAto \_**</span><span class="sxs-lookup"><span data-stu-id="fa814-114">**GRADIENT\_RECT**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)
</dt> <dt>

[<span data-ttu-id="fa814-115">**GradientFill**</span><span class="sxs-lookup"><span data-stu-id="fa814-115">**GradientFill**</span></span>](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill)
</dt> <dt>

[<span data-ttu-id="fa814-116">**Trivertice**</span><span class="sxs-lookup"><span data-stu-id="fa814-116">**TRIVERTEX**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-trivertex)
</dt> </dl>

 

 



