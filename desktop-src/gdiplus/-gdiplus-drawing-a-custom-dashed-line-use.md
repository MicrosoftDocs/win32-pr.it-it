---
description: In Windows GDI+ sono disponibili diversi stili di trattini elencati nell'enumerazione DashStyle. Se gli stili Dash standard non soddisfano le proprie esigenze, è possibile creare un modello Dash personalizzato.
ms.assetid: 0e75de3b-1006-4c8f-875c-eeb0782f24b0
title: Disegno di una linea tratteggiata personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e108dcd6b32a47befcdd99d1f23e90c33d08446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988087"
---
# <a name="drawing-a-custom-dashed-line"></a><span data-ttu-id="98372-104">Disegno di una linea tratteggiata personalizzata</span><span class="sxs-lookup"><span data-stu-id="98372-104">Drawing a Custom Dashed Line</span></span>

<span data-ttu-id="98372-105">In Windows GDI+ sono disponibili diversi stili di trattini elencati nell'enumerazione [**DashStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-dashstyle) .</span><span class="sxs-lookup"><span data-stu-id="98372-105">Windows GDI+ provides several dash styles that are listed in the [**DashStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-dashstyle) enumeration.</span></span> <span data-ttu-id="98372-106">Se gli stili Dash standard non soddisfano le proprie esigenze, è possibile creare un modello Dash personalizzato.</span><span class="sxs-lookup"><span data-stu-id="98372-106">If those standard dash styles don't suit your needs, you can create a custom dash pattern.</span></span>

<span data-ttu-id="98372-107">Per creare una linea tratteggiata personalizzata, inserire le lunghezze dei trattini e degli spazi in una matrice e passare l'indirizzo della matrice come argomento al metodo [**Pen:: SetDashPattern**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setdashpattern) di un oggetto [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="98372-107">To draw a custom dashed line, put the lengths of the dashes and spaces in an array and pass the address of the array as an argument to the [**Pen::SetDashPattern**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setdashpattern) method of a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="98372-108">Nell'esempio seguente viene disegnata una linea tratteggiata personalizzata in base alla matrice {5, 2, 15, 4}.</span><span class="sxs-lookup"><span data-stu-id="98372-108">The following example draws a custom dashed line based on the array {5, 2, 15, 4}.</span></span> <span data-ttu-id="98372-109">Se si moltiplicano gli elementi della matrice in base alla larghezza della penna di 5, si ottengono {25, 10, 75, 20}.</span><span class="sxs-lookup"><span data-stu-id="98372-109">If you multiply the elements of the array by the pen width of 5, you get {25, 10, 75, 20}.</span></span> <span data-ttu-id="98372-110">I trattini visualizzati si alternano con una lunghezza compresa tra 25 e 75 e gli spazi si alternano con una lunghezza compresa tra 10 e 20.</span><span class="sxs-lookup"><span data-stu-id="98372-110">The displayed dashes alternate in length between 25 and 75, and the spaces alternate in length between 10 and 20.</span></span>


```
REAL dashValues[4] = {5, 2, 15, 4};
Pen blackPen(Color(255, 0, 0, 0), 5);
blackPen.SetDashPattern(dashValues, 4);
stat = graphics.DrawLine(&blackPen, Point(5, 5), Point(405, 5));
```



<span data-ttu-id="98372-111">Nella figura seguente viene illustrata la linea tratteggiata risultante.</span><span class="sxs-lookup"><span data-stu-id="98372-111">The following illustration shows the resulting dashed line.</span></span> <span data-ttu-id="98372-112">Si noti che il trattino finale deve essere più breve di 25 unità in modo che la riga possa terminare in corrispondenza di (405, 5).</span><span class="sxs-lookup"><span data-stu-id="98372-112">Note that the final dash has to be shorter than 25 units so that the line can end at (405, 5).</span></span>

![illustrazione che mostra una linea tratteggiata; ogni segmento è una linea breve seguita da un lungo](images/pens6.png)

 

 



