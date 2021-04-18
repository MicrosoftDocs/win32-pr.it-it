---
title: Funzioni (hit testing touch)
description: Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per le funzioni di hit testing.
ms.assetid: C7275A12-4F76-485D-896F-3CCB8CE92F8E
keywords:
- interazione dell'utente
- input
- indicatore di misura
- tocco
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 03fcb4fb3fbe4f56e288703316f4b6e3ff02bba4
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/26/2021
ms.locfileid: "106334021"
---
# <a name="touch-hit-testing-functions"></a><span data-ttu-id="dfbcf-107">Funzioni di hit testing tocco</span><span class="sxs-lookup"><span data-stu-id="dfbcf-107">Touch Hit Testing functions</span></span>

<span data-ttu-id="dfbcf-108">Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per le [funzioni di hit testing](functions.md).</span><span class="sxs-lookup"><span data-stu-id="dfbcf-108">The topics in this section provide the reference specifications for [Touch Hit Testing functions](functions.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dfbcf-109">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="dfbcf-109">In this section</span></span>

| <span data-ttu-id="dfbcf-110">Argomento</span><span class="sxs-lookup"><span data-stu-id="dfbcf-110">Topic</span></span> | <span data-ttu-id="dfbcf-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dfbcf-111">Description</span></span> |
| --- | --- |
| [<span data-ttu-id="dfbcf-112">**EvaluateProximityToPolygon**</span><span class="sxs-lookup"><span data-stu-id="dfbcf-112">**EvaluateProximityToPolygon**</span></span>](/windows/win32/api/winuser/nf-winuser-evaluateproximitytopolygon)<br/> | <span data-ttu-id="dfbcf-113">Restituisce il Punteggio di un poligono come destinazione del tocco probabile (rispetto a tutti gli altri poligoni che intersecano l'area di contatto tocco) e un punto di tocco regolato all'interno del poligono.</span><span class="sxs-lookup"><span data-stu-id="dfbcf-113">Returns the score of a polygon as the probable touch target (compared to all other polygons that intersect the touch contact area) and an adjusted touch point within the polygon.</span></span> <br/> |
| [<span data-ttu-id="dfbcf-114">**EvaluateProximityToRect**</span><span class="sxs-lookup"><span data-stu-id="dfbcf-114">**EvaluateProximityToRect**</span></span>](/windows/win32/api/winuser/nf-winuser-evaluateproximitytorect)<br/> | <span data-ttu-id="dfbcf-115">Restituisce il Punteggio di un rettangolo come destinazione del tocco probabile, rispetto a tutti gli altri rettangoli che intersecano l'area di contatto tocco e a un punto di tocco regolato all'interno del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="dfbcf-115">Returns the score of a rectangle as the probable touch target, compared to all other rectangles that intersect the touch contact area, and an adjusted touch point within the rectangle.</span></span> <br/> |
| [<span data-ttu-id="dfbcf-116">**PackTouchHitTestingProximityEvaluation**</span><span class="sxs-lookup"><span data-stu-id="dfbcf-116">**PackTouchHitTestingProximityEvaluation**</span></span>](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation)<br/> | <span data-ttu-id="dfbcf-117">Restituisce il Punteggio di valutazione di prossimità e le coordinate del punto di tocco modificate come valore compresso per il callback del [messaggio WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) .</span><span class="sxs-lookup"><span data-stu-id="dfbcf-117">Returns the proximity evaluation score and the adjusted touch-point coordinates as a packed value for the [WM_TOUCHHITTESTING message](../inputmsg/wm-touchhittesting.md) callback.</span></span> <br/> |
| [<span data-ttu-id="dfbcf-118">**RegisterTouchHitTestingWindow**</span><span class="sxs-lookup"><span data-stu-id="dfbcf-118">**RegisterTouchHitTestingWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow)<br/> | <span data-ttu-id="dfbcf-119">Registra una finestra per elaborare la notifica di [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md)</span><span class="sxs-lookup"><span data-stu-id="dfbcf-119">Registers a window to process the [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) notification</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="dfbcf-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dfbcf-120">Related topics</span></span>

[<span data-ttu-id="dfbcf-121">Riferimento all'hit testing tocco</span><span class="sxs-lookup"><span data-stu-id="dfbcf-121">Touch Hit Testing Reference</span></span>](touchhittest-reference.md)
