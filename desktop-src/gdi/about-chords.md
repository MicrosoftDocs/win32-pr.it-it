---
description: Una corda è un'area delimitata dall'intersezione tra un'ellisse e un segmento di linea chiamato secante. La figura seguente mostra un accordo disegnato usando la funzione Chord.
ms.assetid: 9aa35b39-06f2-48bf-b32c-3e3e32fab68b
title: Informazioni sugli accordi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18d6310c47a503766e61b9c7936816a5891da89a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527703"
---
# <a name="about-chords"></a><span data-ttu-id="3daf9-104">Informazioni sugli accordi</span><span class="sxs-lookup"><span data-stu-id="3daf9-104">About Chords</span></span>

<span data-ttu-id="3daf9-105">Una *corda* è un'area delimitata dall'intersezione tra un'ellisse e un segmento di linea chiamato *secante*.</span><span class="sxs-lookup"><span data-stu-id="3daf9-105">A *chord* is a region bounded by the intersection of an ellipse and a line segment called a *secant*.</span></span> <span data-ttu-id="3daf9-106">La figura seguente mostra un accordo disegnato usando la funzione [**Chord**](/windows/desktop/api/Wingdi/nf-wingdi-chord) .</span><span class="sxs-lookup"><span data-stu-id="3daf9-106">The following illustration shows a chord drawn by using the [**Chord**](/windows/desktop/api/Wingdi/nf-wingdi-chord) function.</span></span>

![illustrazione di un Elipse, che mostra due radiali, una secante e una corda](images/csfsh-02.png)

<span data-ttu-id="3daf9-108">Quando si chiama [**Chord**](/windows/win32/api/wingdi/nf-wingdi-chord), un'applicazione fornisce le coordinate degli angoli superiore sinistro e inferiore destro del rettangolo di delimitazione dell'ellisse, nonché le coordinate di due punti che definiscono due radiali.</span><span class="sxs-lookup"><span data-stu-id="3daf9-108">When calling [**Chord**](/windows/win32/api/wingdi/nf-wingdi-chord), an application supplies the coordinates of the upper-left and lower-right corners of the ellipse's bounding rectangle, as well as the coordinates of two points defining two radials.</span></span> <span data-ttu-id="3daf9-109">Una radiale è una linea disegnata dal centro del rettangolo di delimitazione di un'ellisse a un punto nell'ellisse.</span><span class="sxs-lookup"><span data-stu-id="3daf9-109">A radial is a line drawn from the center of an ellipse's bounding rectangle to a point on the ellipse.</span></span>

<span data-ttu-id="3daf9-110">Quando il sistema disegna la parte curva della corda, esegue questa operazione utilizzando la direzione di arco corrente per il contesto di dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="3daf9-110">When the system draws the curved part of the chord, it does so by using the current arc direction for the specified device context.</span></span> <span data-ttu-id="3daf9-111">La direzione di arco predefinita è in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="3daf9-111">The default arc direction is counterclockwise.</span></span> <span data-ttu-id="3daf9-112">È possibile reimpostare la direzione dell'arco chiamando la funzione [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) .</span><span class="sxs-lookup"><span data-stu-id="3daf9-112">You can have your application reset the arc direction by calling the [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) function.</span></span>

 

 
