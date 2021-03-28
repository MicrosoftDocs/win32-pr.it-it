---
description: Un join a linee è l'area comune costituita da due righe le cui estremità soddisfano o si sovrappongono.
ms.assetid: 4ec3e76a-2531-4869-a5b0-c595198e8345
title: Unione di linee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2ab0bc53239b9a0d9327a26e25eed1c93c685b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567012"
---
# <a name="joining-lines"></a><span data-ttu-id="e45b8-103">Unione di linee</span><span class="sxs-lookup"><span data-stu-id="e45b8-103">Joining Lines</span></span>

<span data-ttu-id="e45b8-104">Un join a linee è l'area comune costituita da due righe le cui estremità soddisfano o si sovrappongono.</span><span class="sxs-lookup"><span data-stu-id="e45b8-104">A line join is the common area that is formed by two lines whose ends meet or overlap.</span></span> <span data-ttu-id="e45b8-105">In Windows GDI+ sono disponibili quattro stili di join a linee: Miter, smussato, arrotondato e Miter troncato.</span><span class="sxs-lookup"><span data-stu-id="e45b8-105">Windows GDI+ provides four line join styles: miter, bevel, round, and miter clipped.</span></span> <span data-ttu-id="e45b8-106">Lo stile di join a linee è una proprietà della classe [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="e45b8-106">Line join style is a property of the [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) class.</span></span> <span data-ttu-id="e45b8-107">Quando si specifica uno stile di join di riga per una penna e quindi si utilizza tale penna per tracciare un tracciato, lo stile di join specificato viene applicato a tutte le linee connesse del percorso.</span><span class="sxs-lookup"><span data-stu-id="e45b8-107">When you specify a line join style for a pen and then use that pen to draw a path, the specified join style is applied to all the connected lines in the path.</span></span>

<span data-ttu-id="e45b8-108">È possibile specificare lo stile di join a linee usando il metodo [**Pen:: SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) della classe [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="e45b8-108">You can specify the line join style by using the [**Pen::SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) method of the [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) class.</span></span> <span data-ttu-id="e45b8-109">Nell'esempio seguente viene illustrato un join a linee smussate tra una linea orizzontale e una linea verticale:</span><span class="sxs-lookup"><span data-stu-id="e45b8-109">The following example demonstrates a beveled line join between a horizontal line and a vertical line:</span></span>


```
GraphicsPath path;
Pen penJoin(Color(255, 0, 0, 255), 8);

path.StartFigure();
path.AddLine(Point(50, 200), Point(100, 200));
path.AddLine(Point(100, 200), Point(100, 250));

penJoin.SetLineJoin(LineJoinBevel);
graphics.DrawPath(&penJoin, &path);
```



<span data-ttu-id="e45b8-110">Nell'illustrazione seguente viene mostrato il join di linea smussato risultante.</span><span class="sxs-lookup"><span data-stu-id="e45b8-110">The following illustration shows the resulting beveled line join.</span></span>

![illustrazione che mostra due linee che si riuniscono a un angolo retto, con un join smussato](images/pens5.png)

<span data-ttu-id="e45b8-112">Nell'esempio precedente, il valore (**LineJoinBevel**) passato al metodo [**Pen:: SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) è un elemento dell'enumerazione [**LineJoin**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linejoin) .</span><span class="sxs-lookup"><span data-stu-id="e45b8-112">In the preceding example, the value (**LineJoinBevel**) passed to the [**Pen::SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) method is an element of the [**LineJoin**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linejoin) enumeration.</span></span>

 

 



