---
description: L'ombreggiatura uniforme è un metodo di ombreggiatura di un'area con una sfumatura di colore.
ms.assetid: 94f26d15-fb76-47ec-b805-f04975d41b43
title: Ombreggiatura uniforme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5b73738c03147083099a5070e61fe21ca5cac76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232550"
---
# <a name="smooth-shading"></a><span data-ttu-id="e2508-103">Ombreggiatura uniforme</span><span class="sxs-lookup"><span data-stu-id="e2508-103">Smooth Shading</span></span>

<span data-ttu-id="e2508-104">L' *ombreggiatura uniforme* è un metodo di ombreggiatura di un'area con una sfumatura di colore.</span><span class="sxs-lookup"><span data-stu-id="e2508-104">*Smooth shading* is a method of shading a region with a color gradient.</span></span> <span data-ttu-id="e2508-105">L'inclusione di informazioni sui colori, insieme ai limiti della primitiva di disegno, specifica la sfumatura di colore.</span><span class="sxs-lookup"><span data-stu-id="e2508-105">Including color information, along with the bounds of drawing primitive, specifies the color gradient.</span></span> <span data-ttu-id="e2508-106">GDI esegue l'interpolazione lineare del colore dell'interno della primitiva passata sugli endpoint dei colori.</span><span class="sxs-lookup"><span data-stu-id="e2508-106">GDI linearly interpolates the color of the inside of the primitive passed on the color endpoints.</span></span> <span data-ttu-id="e2508-107">Le informazioni sui vertici e sui colori sono incluse con le informazioni sulla posizione nella struttura [**trivertice**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) .</span><span class="sxs-lookup"><span data-stu-id="e2508-107">Color and vertex information is included with position information in the [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) structure.</span></span>

<span data-ttu-id="e2508-108">Utilizzare la funzione [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) per riempire un triangolo o una struttura Rectangle.</span><span class="sxs-lookup"><span data-stu-id="e2508-108">Use the [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) function to fill a triangle or rectangle structure.</span></span> <span data-ttu-id="e2508-109">Per riempire un triangolo con ombreggiatura uniforme, chiamare **GradientFill** con i tre endpoint triangolari.</span><span class="sxs-lookup"><span data-stu-id="e2508-109">To fill a triangle with smooth shading, call **GradientFill** with the three triangle endpoints.</span></span> <span data-ttu-id="e2508-110">Per riempire un rettangolo con ombreggiatura uniforme, chiamare **GradientFill** con le coordinate del rettangolo superiore sinistro e inferiore destro.</span><span class="sxs-lookup"><span data-stu-id="e2508-110">To fill a rectangle with smooth shading, call **GradientFill** with the upper-left and lower-right rectangle coordinates.</span></span> <span data-ttu-id="e2508-111">**GradientFill** fa riferimento alle strutture [**trivertice**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex), rettangolo [**\_ sfumato**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)e [**\_ triangolo sfumatura**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) .</span><span class="sxs-lookup"><span data-stu-id="e2508-111">**GradientFill** references the [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex), [**GRADIENT\_RECT**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect), and [**GRADIENT\_TRIANGLE**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) structures.</span></span>

<span data-ttu-id="e2508-112">Per un esempio, vedere [disegno di un triangolo ombreggiato](drawing-a-shaded-triangle.md).</span><span class="sxs-lookup"><span data-stu-id="e2508-112">For an example, see [Drawing a Shaded Triangle](drawing-a-shaded-triangle.md).</span></span>

 

 



