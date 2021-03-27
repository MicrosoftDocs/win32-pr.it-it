---
description: Una torta è un'area delimitata dall'intersezione di una curva di ellisse e due radiali. Nella figura seguente viene illustrato un grafico a torta creato utilizzando la funzione Pie.
ms.assetid: 9ba7834e-02d2-4335-94c3-ab2f5c355619
title: Informazioni su torte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2184276fc208827ddac82fd7f4cacec3ddb20f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049738"
---
# <a name="about-pies"></a><span data-ttu-id="0d84f-104">Informazioni su torte</span><span class="sxs-lookup"><span data-stu-id="0d84f-104">About Pies</span></span>

<span data-ttu-id="0d84f-105">Una *torta* è un'area delimitata dall'intersezione di una curva di ellisse e due radiali.</span><span class="sxs-lookup"><span data-stu-id="0d84f-105">A *pie* is a region bounded by the intersection of an ellipse curve and two radials.</span></span> <span data-ttu-id="0d84f-106">Nella figura seguente viene illustrato un grafico a torta creato utilizzando la funzione [**Pie**](/windows/desktop/api/Wingdi/nf-wingdi-pie) .</span><span class="sxs-lookup"><span data-stu-id="0d84f-106">The following illustration shows a pie drawn by using the [**Pie**](/windows/desktop/api/Wingdi/nf-wingdi-pie) function.</span></span>

![illustrazione che mostra un'ellisse con una torta ombreggiata](images/csfsh-03.png)

<span data-ttu-id="0d84f-108">Quando si chiama [**torta**](/windows/win32/api/wingdi/nf-wingdi-pie), un'applicazione fornisce le coordinate degli angoli superiore sinistro e inferiore destro del rettangolo di delimitazione dell'ellisse, nonché le coordinate di due punti che definiscono due radiali.</span><span class="sxs-lookup"><span data-stu-id="0d84f-108">When calling [**Pie**](/windows/win32/api/wingdi/nf-wingdi-pie), an application supplies the coordinates of the upper-left and lower-right corners of the ellipse's bounding rectangle, as well as the coordinates of two points defining two radials.</span></span>

<span data-ttu-id="0d84f-109">Quando il sistema disegna la parte curva della torta, usa la direzione di arco corrente per il contesto di dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="0d84f-109">When the system draws the curved part of the pie, it uses the current arc direction for the given device context.</span></span> <span data-ttu-id="0d84f-110">La direzione di arco predefinita è in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="0d84f-110">The default arc direction is counterclockwise.</span></span> <span data-ttu-id="0d84f-111">Un'applicazione può reimpostare la direzione dell'arco chiamando la funzione [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) .</span><span class="sxs-lookup"><span data-stu-id="0d84f-111">An application can reset the arc direction by calling the [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) function.</span></span>

 

 
