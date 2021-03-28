---
description: "La classe Graphics fornisce un'ampia gamma di metodi di disegno, inclusi quelli mostrati nell'elenco seguente:"
ms.assetid: d3c8d16c-858a-42a9-a512-3fcfa144f5fc
title: Utilizzo di un oggetto Pen per creare linee e forme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904f53149038d6109365adddc11d3c37881a8def
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129054"
---
# <a name="using-a-pen-to-draw-lines-and-shapes"></a><span data-ttu-id="94cb5-103">Utilizzo di un oggetto Pen per creare linee e forme</span><span class="sxs-lookup"><span data-stu-id="94cb5-103">Using a Pen to Draw Lines and Shapes</span></span>

<span data-ttu-id="94cb5-104">La classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fornisce un'ampia gamma di metodi di disegno, inclusi quelli mostrati nell'elenco seguente:</span><span class="sxs-lookup"><span data-stu-id="94cb5-104">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides a variety of drawing methods including those shown in the following list:</span></span>

-   <span data-ttu-id="94cb5-105">[Metodi DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))</span><span class="sxs-lookup"><span data-stu-id="94cb5-105">[DrawLine Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))</span></span>
-   <span data-ttu-id="94cb5-106">[Metodi DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inconstrectf_))</span><span class="sxs-lookup"><span data-stu-id="94cb5-106">[DrawRectangle Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inconstrectf_))</span></span>
-   <span data-ttu-id="94cb5-107">[Metodi DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrectf_))</span><span class="sxs-lookup"><span data-stu-id="94cb5-107">[DrawEllipse Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrectf_))</span></span>
-   <span data-ttu-id="94cb5-108">[Metodi DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal))</span><span class="sxs-lookup"><span data-stu-id="94cb5-108">[DrawArc Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal))</span></span>
-   [<span data-ttu-id="94cb5-109">**Grafica::D rawPath**</span><span class="sxs-lookup"><span data-stu-id="94cb5-109">**Graphics::DrawPath**</span></span>](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath)
-   <span data-ttu-id="94cb5-110">[Metodi DrawCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint))</span><span class="sxs-lookup"><span data-stu-id="94cb5-110">[DrawCurve Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint))</span></span>
-   <span data-ttu-id="94cb5-111">[Metodi DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inconstpointf__inconstpointf__inconstpointf__inconstpointf_))</span><span class="sxs-lookup"><span data-stu-id="94cb5-111">[DrawBezier Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inconstpointf__inconstpointf__inconstpointf__inconstpointf_))</span></span>

<span data-ttu-id="94cb5-112">Uno degli argomenti passati a un metodo di disegno di questo tipo è l'indirizzo di un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="94cb5-112">One of the arguments that you pass to such a drawing method is the address of a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span>

<span data-ttu-id="94cb5-113">Negli argomenti seguenti viene illustrato in modo più dettagliato l'utilizzo delle penne:</span><span class="sxs-lookup"><span data-stu-id="94cb5-113">The following topics cover the use of pens in more detail:</span></span>

-   [<span data-ttu-id="94cb5-114">Uso di una penna per disegnare linee e rettangoli</span><span class="sxs-lookup"><span data-stu-id="94cb5-114">Using a Pen to Draw Lines and Rectangles</span></span>](-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use.md)
-   [<span data-ttu-id="94cb5-115">Impostazione della larghezza e dell'allineamento della penna</span><span class="sxs-lookup"><span data-stu-id="94cb5-115">Setting Pen Width and Alignment</span></span>](-gdiplus-setting-pen-width-and-alignment-use.md)
-   [<span data-ttu-id="94cb5-116">Disegno di una linea con estremità di riga</span><span class="sxs-lookup"><span data-stu-id="94cb5-116">Drawing a Line with Line Caps</span></span>](-gdiplus-drawing-a-line-with-line-caps-use.md)
-   [<span data-ttu-id="94cb5-117">Unione di linee</span><span class="sxs-lookup"><span data-stu-id="94cb5-117">Joining Lines</span></span>](-gdiplus-joining-lines-use.md)
-   [<span data-ttu-id="94cb5-118">Disegno di una linea tratteggiata personalizzata</span><span class="sxs-lookup"><span data-stu-id="94cb5-118">Drawing a Custom Dashed Line</span></span>](-gdiplus-drawing-a-custom-dashed-line-use.md)
-   [<span data-ttu-id="94cb5-119">Disegno di una linea riempita con una trama</span><span class="sxs-lookup"><span data-stu-id="94cb5-119">Drawing a Line Filled with a Texture</span></span>](-gdiplus-drawing-a-line-filled-with-a-texture-use.md)

 

 



