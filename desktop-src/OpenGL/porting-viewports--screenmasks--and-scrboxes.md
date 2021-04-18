---
title: Porting di viewport, Screenmasks e Scrboxes
description: Le funzioni viewport GL seguenti non hanno un equivalente OpenGL
ms.assetid: 223e9b5b-1ddd-45a6-8489-b262d0207a5a
keywords:
- Porting di IRIS GL, funzioni viewport
- porting da IRIS GL, funzioni viewport
- porting in OpenGL da IRIS GL, funzioni viewport
- Porting OpenGL da IRIS GL, funzioni viewport
- funzioni viewport
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b3429a0d154f4ef62a12d767c6497099ac09751
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297985"
---
# <a name="porting-viewports-screenmasks-and-scrboxes"></a><span data-ttu-id="a1cfb-108">Porting di viewport, Screenmasks e Scrboxes</span><span class="sxs-lookup"><span data-stu-id="a1cfb-108">Porting Viewports, Screenmasks, and Scrboxes</span></span>

<span data-ttu-id="a1cfb-109">Le funzioni viewport GL seguenti non hanno un equivalente OpenGL:</span><span class="sxs-lookup"><span data-stu-id="a1cfb-109">The following IRIS GL viewport functions have no OpenGL equivalent:</span></span>

-   <span data-ttu-id="a1cfb-110">**reshapeviewport**</span><span class="sxs-lookup"><span data-stu-id="a1cfb-110">**reshapeviewport**</span></span>
-   <span data-ttu-id="a1cfb-111">**scrbox**</span><span class="sxs-lookup"><span data-stu-id="a1cfb-111">**scrbox**</span></span>
-   <span data-ttu-id="a1cfb-112">**getscrbox**</span><span class="sxs-lookup"><span data-stu-id="a1cfb-112">**getscrbox**</span></span>

<span data-ttu-id="a1cfb-113">Con la funzione del **viewport** di Iris GL, è necessario specificare le coordinate x (in pixel) per la sinistra e la destra di un rettangolo del viewport e le coordinate y per la parte superiore e inferiore.</span><span class="sxs-lookup"><span data-stu-id="a1cfb-113">With the IRIS GL **viewport** function, you specify the x coordinates (in pixels) for the left and right of a viewport rectangle and the y coordinates for the top and bottom.</span></span> <span data-ttu-id="a1cfb-114">Con la funzione OpenGL [**glViewport**](glviewport.md) , tuttavia, si specificano le coordinate x e y (in pixel) dell'angolo inferiore sinistro del rettangolo del viewport insieme alla relativa larghezza e altezza.</span><span class="sxs-lookup"><span data-stu-id="a1cfb-114">With the OpenGL [**glViewport**](glviewport.md) function, however, you specify the x and y coordinates (in pixels) of the lower-left corner of the viewport rectangle along with its width and height.</span></span>

<span data-ttu-id="a1cfb-115">La tabella seguente elenca le funzioni viewport GL di IRIS e le relative funzioni OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="a1cfb-115">The following table lists IRIS GL viewport functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="a1cfb-116">Funzione IRIS GL</span><span class="sxs-lookup"><span data-stu-id="a1cfb-116">IRIS GL function</span></span>                          | <span data-ttu-id="a1cfb-117">OpenGL (funzione)</span><span class="sxs-lookup"><span data-stu-id="a1cfb-117">OpenGL function</span></span>                                                                                         | <span data-ttu-id="a1cfb-118">Significato</span><span class="sxs-lookup"><span data-stu-id="a1cfb-118">Meaning</span></span>                      |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="a1cfb-119">**viewport** (a sinistra, a destra, in basso, in alto)</span><span class="sxs-lookup"><span data-stu-id="a1cfb-119">**viewport** ( left, right, bottom, top )</span></span> | <span data-ttu-id="a1cfb-120">[**glViewport**](glviewport.md) (x, y, larghezza, altezza)</span><span class="sxs-lookup"><span data-stu-id="a1cfb-120">[**glViewport**](glviewport.md) ( x, y, width, height )</span></span>                                                | <span data-ttu-id="a1cfb-121">Imposta il viewport.</span><span class="sxs-lookup"><span data-stu-id="a1cfb-121">Sets the viewport.</span></span>           |
| <span data-ttu-id="a1cfb-122">**popviewportpushviewport**</span><span class="sxs-lookup"><span data-stu-id="a1cfb-122">**popviewportpushviewport**</span></span><br/>    | <span data-ttu-id="a1cfb-123">[**glPopAttrib**](glpopattrib.md)[**glPushAttrib**](glpushattrib.md) (bit del viewport per GL \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="a1cfb-123">[**glPopAttrib**](glpopattrib.md)[**glPushAttrib**](glpushattrib.md) ( GL\_VIEWPORT\_BIT )</span></span><br/> | <span data-ttu-id="a1cfb-124">Inserisce e estrae lo stack.</span><span class="sxs-lookup"><span data-stu-id="a1cfb-124">Pushes and pops the stack.</span></span>   |
| <span data-ttu-id="a1cfb-125">**getViewport**</span><span class="sxs-lookup"><span data-stu-id="a1cfb-125">**getviewport**</span></span>                           | <span data-ttu-id="a1cfb-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ riquadro di visualizzazione GL)</span><span class="sxs-lookup"><span data-stu-id="a1cfb-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_VIEWPORT )</span></span>               | <span data-ttu-id="a1cfb-127">Restituisce le dimensioni del viewport.</span><span class="sxs-lookup"><span data-stu-id="a1cfb-127">Returns viewport dimensions.</span></span> |



 

<span data-ttu-id="a1cfb-128">??</span><span class="sxs-lookup"><span data-stu-id="a1cfb-128">??</span></span>

 

 





