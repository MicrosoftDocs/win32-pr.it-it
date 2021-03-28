---
description: Per creare linee e rettangoli, sono necessari un oggetto Graphics e un oggetto Pen. L'oggetto Graphics fornisce il metodo DrawLine e l'oggetto Pen archivia le funzionalità della riga, ad esempio il colore e la larghezza.
ms.assetid: f2e4144f-f2f1-49db-bfdf-ffce3023b4cb
title: Uso di una penna per disegnare linee e rettangoli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b335caf7e2ecbad6bc49965ff757809c3b1179c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967196"
---
# <a name="using-a-pen-to-draw-lines-and-rectangles"></a><span data-ttu-id="e7628-104">Uso di una penna per disegnare linee e rettangoli</span><span class="sxs-lookup"><span data-stu-id="e7628-104">Using a Pen to Draw Lines and Rectangles</span></span>

<span data-ttu-id="e7628-105">Per creare linee e rettangoli, sono necessari un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="e7628-105">To draw lines and rectangles, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="e7628-106">L'oggetto **Graphics** fornisce il metodo [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) e l'oggetto **Pen** archivia le funzionalità della riga, ad esempio il colore e la larghezza.</span><span class="sxs-lookup"><span data-stu-id="e7628-106">The **Graphics** object provides the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method, and the **Pen** object stores features of the line, such as color and width.</span></span>

<span data-ttu-id="e7628-107">Nell'esempio seguente viene disegnata una riga da (20, 10) a (300, 100).</span><span class="sxs-lookup"><span data-stu-id="e7628-107">The following example draws a line from (20, 10) to (300, 100).</span></span> <span data-ttu-id="e7628-108">Si supponga che **Graphics** sia un oggetto [**grafico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) esistente.</span><span class="sxs-lookup"><span data-stu-id="e7628-108">Assume **graphics** is an existing [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>


```
Pen pen(Color(255, 0, 0, 0));
graphics.DrawLine(&pen, 20, 10, 300, 100);
```



<span data-ttu-id="e7628-109">La prima istruzione di codice usa il costruttore della classe [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) per creare una penna nera.</span><span class="sxs-lookup"><span data-stu-id="e7628-109">The first statement of code uses the [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) class constructor to create a black pen.</span></span> <span data-ttu-id="e7628-110">L'unico argomento passato al costruttore **Pen** è un oggetto [**color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="e7628-110">The one argument passed to the **Pen** constructor is a [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="e7628-111">I valori utilizzati per costruire l'oggetto **colore** , (255, 0, 0, 0), corrispondono ai componenti alfa, rosso, verde e blu del colore.</span><span class="sxs-lookup"><span data-stu-id="e7628-111">The values used to construct the **Color** object — (255, 0, 0, 0) — correspond to the alpha, red, green, and blue components of the color.</span></span> <span data-ttu-id="e7628-112">Questi valori definiscono una penna nera opaca.</span><span class="sxs-lookup"><span data-stu-id="e7628-112">These values define an opaque black pen.</span></span>

<span data-ttu-id="e7628-113">Nell'esempio seguente viene disegnato un rettangolo con l'angolo superiore sinistro in corrispondenza di (10, 10).</span><span class="sxs-lookup"><span data-stu-id="e7628-113">The following example draws a rectangle with its upper-left corner at (10, 10).</span></span> <span data-ttu-id="e7628-114">Il rettangolo ha una larghezza di 100 e un'altezza di 50.</span><span class="sxs-lookup"><span data-stu-id="e7628-114">The rectangle has a width of 100 and a height of 50.</span></span> <span data-ttu-id="e7628-115">Il secondo argomento passato al costruttore [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) indica che la lunghezza della penna è 5 pixel.</span><span class="sxs-lookup"><span data-stu-id="e7628-115">The second argument passed to the [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) constructor indicates that the pen width is 5 pixels.</span></span>


```
Pen blackPen(Color(255, 0, 0, 0), 5);
stat = graphics.DrawRectangle(&blackPen, 10, 10, 100, 50);
```



<span data-ttu-id="e7628-116">Quando il rettangolo viene disegnato, la penna viene centrata sul limite del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="e7628-116">When the rectangle is drawn, the pen is centered on the rectangle's boundary.</span></span> <span data-ttu-id="e7628-117">Poiché la larghezza della penna è 5, i lati del rettangolo vengono disegnati a 5 pixel di larghezza, in modo che 1 pixel venga disegnato sul limite, 2 pixel siano disegnati all'interno e 2 pixel vengono disegnati all'esterno.</span><span class="sxs-lookup"><span data-stu-id="e7628-117">Because the pen width is 5, the sides of the rectangle are drawn 5 pixels wide, such that 1 pixel is drawn on the boundary itself, 2 pixels are drawn on the inside, and 2 pixels are drawn on the outside.</span></span> <span data-ttu-id="e7628-118">Per altri dettagli sull'allineamento della penna, vedere [impostazione della larghezza e dell'allineamento della penna](-gdiplus-setting-pen-width-and-alignment-use.md).</span><span class="sxs-lookup"><span data-stu-id="e7628-118">For more details on pen alignment, see [Setting Pen Width and Alignment](-gdiplus-setting-pen-width-and-alignment-use.md).</span></span>

<span data-ttu-id="e7628-119">Nella figura seguente viene illustrato il rettangolo risultante.</span><span class="sxs-lookup"><span data-stu-id="e7628-119">The following illustration shows the resulting rectangle.</span></span> <span data-ttu-id="e7628-120">Le linee tratteggiate indicano dove sarebbe stato disegnato il rettangolo se la lunghezza della penna era un pixel.</span><span class="sxs-lookup"><span data-stu-id="e7628-120">The dotted lines show where the rectangle would have been drawn if the pen width had been one pixel.</span></span> <span data-ttu-id="e7628-121">La visualizzazione ingrandita dell'angolo superiore sinistro del rettangolo indica che le linee nere spesse sono centrate su tali linee tratteggiate.</span><span class="sxs-lookup"><span data-stu-id="e7628-121">The enlarged view of the upper-left corner of the rectangle shows that the thick black lines are centered on those dotted lines.</span></span>

![illustrazione di un rettangolo disegnato con una linea nera spessa che racchiude una linea sottile, grigia tratteggiata](images/pens1.png)

 

 



