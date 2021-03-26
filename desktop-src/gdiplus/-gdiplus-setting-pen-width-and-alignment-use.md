---
description: 'Quando si crea un oggetto Pen, è possibile specificare la larghezza della penna come uno degli argomenti per il costruttore. È anche possibile modificare la larghezza della penna usando il metodo Pen:: sewidth.'
ms.assetid: b529ba0b-1786-4925-88bd-1a8369fc368c
title: Impostazione della larghezza e dell'allineamento della penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca59895cc73480b054302091342c8f8f4f410b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104559521"
---
# <a name="setting-pen-width-and-alignment"></a><span data-ttu-id="7d593-104">Impostazione della larghezza e dell'allineamento della penna</span><span class="sxs-lookup"><span data-stu-id="7d593-104">Setting Pen Width and Alignment</span></span>

<span data-ttu-id="7d593-105">Quando si crea un oggetto [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) , è possibile specificare la larghezza della penna come uno degli argomenti per il costruttore.</span><span class="sxs-lookup"><span data-stu-id="7d593-105">When you create a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) object, you can supply the pen width as one of the arguments to the constructor.</span></span> <span data-ttu-id="7d593-106">È anche possibile modificare la larghezza della penna usando il metodo [**Pen:: sewidth**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setwidth) .</span><span class="sxs-lookup"><span data-stu-id="7d593-106">You can also change the pen width by using the [**Pen::SetWidth**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setwidth) method.</span></span>

<span data-ttu-id="7d593-107">Una linea teorica ha una larghezza pari a zero.</span><span class="sxs-lookup"><span data-stu-id="7d593-107">A theoretical line has a width of zero.</span></span> <span data-ttu-id="7d593-108">Quando si crea una linea, i pixel vengono centrati sulla linea teorica.</span><span class="sxs-lookup"><span data-stu-id="7d593-108">When you draw a line, the pixels are centered on the theoretical line.</span></span> <span data-ttu-id="7d593-109">Nell'esempio seguente la riga specificata viene disegnata due volte: una volta con una penna nera di larghezza 1 e una volta con una penna verde di larghezza 10.</span><span class="sxs-lookup"><span data-stu-id="7d593-109">The following example draws a specified line twice: once with a black pen of width 1 and once with a green pen of width 10.</span></span>


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the line with the wide green pen.
stat = graphics.DrawLine(&greenPen, 10, 100, 100, 50);

// Draw the same line with the thin black pen.
stat = graphics.DrawLine(&blackPen, 10, 100, 100, 50);
```



<span data-ttu-id="7d593-110">Nella figura seguente viene illustrato l'output del codice precedente.</span><span class="sxs-lookup"><span data-stu-id="7d593-110">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="7d593-111">I pixel verdi e i pixel neri sono centrati sulla linea teorica.</span><span class="sxs-lookup"><span data-stu-id="7d593-111">The green pixels and the black pixels are centered on the theoretical line.</span></span>

![<span data-ttu-id="7d593-112">illustrazione che mostra una linea sottile, diagonale, nera circondata da una linea verde ampia</span><span class="sxs-lookup"><span data-stu-id="7d593-112">illustration showing a thin, diagonal, black line surrounded by a wide, green line</span></span> ](images/pens1a.png)

<span data-ttu-id="7d593-113">Nell'esempio seguente viene disegnato un rettangolo specificato due volte: una volta con una penna nera di larghezza 1 e una volta con una penna verde di larghezza 10.</span><span class="sxs-lookup"><span data-stu-id="7d593-113">The following example draws a specified rectangle twice: once with a black pen of width 1 and once with a green pen of width 10.</span></span> <span data-ttu-id="7d593-114">Il codice passa il valore **PenAlignmentCenter** (un elemento dell'enumerazione [**PenAlignment**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-penalignment) ) al metodo [**Pen:: sealignment**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setalignment) per specificare che i pixel disegnati con la penna verde sono centrati sul limite del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="7d593-114">The code passes the value **PenAlignmentCenter** (an element of the [**PenAlignment**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-penalignment) enumeration) to the [**Pen::SetAlignment**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setalignment) method to specify that the pixels drawn with the green pen are centered on the boundary of the rectangle.</span></span>


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the rectangle with the wide green pen.
stat = graphics.DrawRectangle(&greenPen, 10, 100, 50, 50);

// Draw the same rectangle with the thin black pen.
stat = graphics.DrawRectangle(&blackPen, 10, 100, 50, 50);
```



<span data-ttu-id="7d593-115">Nella figura seguente viene illustrato l'output del codice precedente.</span><span class="sxs-lookup"><span data-stu-id="7d593-115">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="7d593-116">I pixel verdi sono centrati sul rettangolo teorico, rappresentato dai pixel neri.</span><span class="sxs-lookup"><span data-stu-id="7d593-116">The green pixels are centered on the theoretical rectangle, which is represented by the black pixels.</span></span>

![illustrazione che mostra una linea nera sottile nella forma di un rettangolo, circondata da una linea verde più ampia](images/pens2.png)

<span data-ttu-id="7d593-118">È possibile modificare l'allineamento della penna verde modificando la terza istruzione nell'esempio precedente come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="7d593-118">You can change the green pen's alignment by modifying the third statement in the preceding example as follows:</span></span>


```
stat = greenPen.SetAlignment(PenAlignmentInset);
```



<span data-ttu-id="7d593-119">Ora i pixel nella linea verde ampia vengono visualizzati all'interno del rettangolo, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="7d593-119">Now the pixels in the wide green line appear on the inside of the rectangle as shown in the following illustration.</span></span>

![illustrazione che mostra una linea nera sottile nella forma di un rectange, che racchiude una linea verde ampia con la stessa forma](images/pens3.png)

 

 



