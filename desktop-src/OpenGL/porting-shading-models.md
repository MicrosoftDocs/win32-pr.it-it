---
title: Porting di modelli di ombreggiatura
description: Analogamente a IRIS GL, OpenGL consente di passare da un'ombreggiatura Smooth (Gouraud) a un'ombreggiatura semplice e viceversa. La tabella seguente elenca le funzioni di ombreggiatura e dithering di IRIS GL e le relative funzioni OpenGL equivalenti.
ms.assetid: 93e8f437-381f-4620-ad6f-52ce830d99b6
keywords:
- Porting di IRIS GL, ombreggiatura
- porting da IRIS GL, ombreggiatura
- porting in OpenGL da IRIS GL, ombreggiatura
- Porting OpenGL da IRIS GL, ombreggiatura
- ombreggiatura uniforme
- Ombreggiatura Gouraud
- ombreggiatura flat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124bb002f6f133b4d47dd40e1a0e8738c512ce99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331004"
---
# <a name="porting-shading-models"></a><span data-ttu-id="6b212-111">Porting di modelli di ombreggiatura</span><span class="sxs-lookup"><span data-stu-id="6b212-111">Porting Shading Models</span></span>

<span data-ttu-id="6b212-112">Analogamente a IRIS GL, OpenGL consente di passare da un'ombreggiatura Smooth (Gouraud) a un'ombreggiatura semplice e viceversa.</span><span class="sxs-lookup"><span data-stu-id="6b212-112">Like IRIS GL, OpenGL lets you switch between smooth (Gouraud) shading and flat shading.</span></span> <span data-ttu-id="6b212-113">La tabella seguente elenca le funzioni di ombreggiatura e dithering di IRIS GL e le relative funzioni OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="6b212-113">The following table lists the IRIS GL shading and dithering functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="6b212-114">Funzione IRIS GL</span><span class="sxs-lookup"><span data-stu-id="6b212-114">IRIS GL function</span></span>                                   | <span data-ttu-id="6b212-115">OpenGL (funzione)</span><span class="sxs-lookup"><span data-stu-id="6b212-115">OpenGL function</span></span>                                                                                    | <span data-ttu-id="6b212-116">Significato</span><span class="sxs-lookup"><span data-stu-id="6b212-116">Meaning</span></span>                      |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="6b212-117">**shademodel**(Flat)</span><span class="sxs-lookup"><span data-stu-id="6b212-117">**shademodel**(FLAT)</span></span>                               | <span data-ttu-id="6b212-118">[**glShadeModel**](glshademodel.md) (GL \_ Flat)</span><span class="sxs-lookup"><span data-stu-id="6b212-118">[**glShadeModel**](glshademodel.md) ( GL\_FLAT )</span></span>                                                  | <span data-ttu-id="6b212-119">Esegue l'ombreggiatura piatta.</span><span class="sxs-lookup"><span data-stu-id="6b212-119">Does flat shading.</span></span>           |
| <span data-ttu-id="6b212-120">**shademodel**(Gouraud)</span><span class="sxs-lookup"><span data-stu-id="6b212-120">**shademodel**(GOURAUD)</span></span>                            | <span data-ttu-id="6b212-121">**glShadeModel**(GL \_ Smooth)</span><span class="sxs-lookup"><span data-stu-id="6b212-121">**glShadeModel**( GL\_SMOOTH )</span></span>                                                                     | <span data-ttu-id="6b212-122">Esegue un'ombreggiatura uniforme.</span><span class="sxs-lookup"><span data-stu-id="6b212-122">Does smooth shading.</span></span>         |
| <span data-ttu-id="6b212-123">**Ottiene**</span><span class="sxs-lookup"><span data-stu-id="6b212-123">**getsm**</span></span>                                          | <span data-ttu-id="6b212-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ modello di ombreggiatura GL \_ )</span><span class="sxs-lookup"><span data-stu-id="6b212-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_SHADE\_MODEL )</span></span>      | <span data-ttu-id="6b212-125">Restituisce il modello di ombreggiatura corrente.</span><span class="sxs-lookup"><span data-stu-id="6b212-125">Returns current shade model.</span></span> |
| <span data-ttu-id="6b212-126">**dithering (DT** \_ on) **dithering**(DT \_ disattivato)</span><span class="sxs-lookup"><span data-stu-id="6b212-126">**dither**(DT\_ON) **dither**(DT\_OFF)</span></span> <br/> | <span data-ttu-id="6b212-127">[**glEnable**](glenable.md) ( \_ dithering GL)[**glDisable**](gldisable.md)( \_ dithering GL)</span><span class="sxs-lookup"><span data-stu-id="6b212-127">[**glEnable**](glenable.md) ( GL\_DITHER )[**glDisable**](gldisable.md)( GL\_DITHER )</span></span><br/> | <span data-ttu-id="6b212-128">Attiva/disattiva la dithering.</span><span class="sxs-lookup"><span data-stu-id="6b212-128">Turns dithering on/off.</span></span>      |



 

<span data-ttu-id="6b212-129">??</span><span class="sxs-lookup"><span data-stu-id="6b212-129">??</span></span>

 

 





