---
description: Oltre a tracciare linee o curve, le applicazioni possono disegnare combinazioni di output di linee e curve chiamando una singola funzione. Ad esempio, un'applicazione può tracciare il contorno di un grafico a torta chiamando la funzione AngleArc.
ms.assetid: 0abcc20c-ba89-4eb4-bbd1-7ea27d367fb8
title: Linee e curve combinate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ee6aaa3e7a1be580e36c01fb44c81296e894d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978735"
---
# <a name="combined-lines-and-curves"></a><span data-ttu-id="966a0-104">Linee e curve combinate</span><span class="sxs-lookup"><span data-stu-id="966a0-104">Combined Lines and Curves</span></span>

<span data-ttu-id="966a0-105">Oltre a tracciare linee o curve, le applicazioni possono disegnare combinazioni di output di linee e curve chiamando una singola funzione.</span><span class="sxs-lookup"><span data-stu-id="966a0-105">In addition to drawing lines or curves, applications can draw combinations of line and curve output by calling a single function.</span></span> <span data-ttu-id="966a0-106">Ad esempio, un'applicazione può tracciare il contorno di un grafico a torta chiamando la funzione [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) .</span><span class="sxs-lookup"><span data-stu-id="966a0-106">For example, an application can draw the outline of a pie chart by calling the [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) function.</span></span>

<span data-ttu-id="966a0-107">La funzione [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) disegna un arco lungo il perimetro di un cerchio e disegna una linea che connette il punto iniziale dell'arco al centro del cerchio.</span><span class="sxs-lookup"><span data-stu-id="966a0-107">The [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) function draws an arc along a circle's perimeter and draws a line connecting the starting point of the arc to the circle's center.</span></span> <span data-ttu-id="966a0-108">Oltre a usare la funzione **AngleArc** , un'applicazione può combinare anche l'output a curva linea e irregolare usando la funzione di [**politraccia**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw) .</span><span class="sxs-lookup"><span data-stu-id="966a0-108">In addition to using the **AngleArc** function, an application can also combine line and irregular curve output by using the [**PolyDraw**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw) function.</span></span>

 

 



