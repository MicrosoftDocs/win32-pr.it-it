---
title: Uso di funzioni di anti-aliasing
description: La tabella seguente elenca le funzioni di anti-aliasing di IRIS GL e le relative funzioni OpenGL equivalenti.
ms.assetid: d54990b6-5645-4389-82ca-7d7f0a7fd7e9
keywords:
- Porting di IRIS GL, anti-aliasing
- porting da IRIS GL, anti-aliasing
- porting in OpenGL da IRIS GL, anti-aliasing
- Porting OpenGL da IRIS GL, anti-aliasing
- anti-aliasing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896d02dec050c72e59762ff5ee139b0bd091d9a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221233"
---
# <a name="using-antialiasing-functions"></a><span data-ttu-id="66c7b-108">Uso di funzioni di anti-aliasing</span><span class="sxs-lookup"><span data-stu-id="66c7b-108">Using Antialiasing Functions</span></span>

<span data-ttu-id="66c7b-109">La tabella seguente elenca le funzioni di anti-aliasing di IRIS GL e le relative funzioni OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="66c7b-109">The following table lists IRIS GL antialiasing functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="66c7b-110">Funzione IRIS GL</span><span class="sxs-lookup"><span data-stu-id="66c7b-110">IRIS GL function</span></span> | <span data-ttu-id="66c7b-111">OpenGL (funzione)</span><span class="sxs-lookup"><span data-stu-id="66c7b-111">OpenGL function</span></span>                                      | <span data-ttu-id="66c7b-112">Significato</span><span class="sxs-lookup"><span data-stu-id="66c7b-112">Meaning</span></span>                           |
|------------------|------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="66c7b-113">**pntsmooth**</span><span class="sxs-lookup"><span data-stu-id="66c7b-113">**pntsmooth**</span></span>    | <span data-ttu-id="66c7b-114">[**glEnable**](glenable.md) ( \_ punto GL \_ smussato)</span><span class="sxs-lookup"><span data-stu-id="66c7b-114">[**glEnable**](glenable.md) ( GL\_POINT\_SMOOTH )</span></span>   | <span data-ttu-id="66c7b-115">Abilita l'anti-aliasing dei punti.</span><span class="sxs-lookup"><span data-stu-id="66c7b-115">Enables antialiasing of points.</span></span>   |
| <span data-ttu-id="66c7b-116">**linesmooth**</span><span class="sxs-lookup"><span data-stu-id="66c7b-116">**linesmooth**</span></span>   | <span data-ttu-id="66c7b-117">**glEnable**( \_ linea GL \_ smussata)</span><span class="sxs-lookup"><span data-stu-id="66c7b-117">**glEnable**( GL\_LINE\_SMOOTH )</span></span>                     | <span data-ttu-id="66c7b-118">Abilita l'anti-aliasing delle righe.</span><span class="sxs-lookup"><span data-stu-id="66c7b-118">Enables antialiasing of lines.</span></span>    |
| <span data-ttu-id="66c7b-119">**con uniformità**</span><span class="sxs-lookup"><span data-stu-id="66c7b-119">**polysmooth**</span></span>   | <span data-ttu-id="66c7b-120">[**glEnable**](glenable.md) ( \_ arrotondamento del poligono GL \_ )</span><span class="sxs-lookup"><span data-stu-id="66c7b-120">[**glEnable**](glenable.md) ( GL\_POLYGON\_SMOOTH )</span></span> | <span data-ttu-id="66c7b-121">Abilita l'anti-aliasing dei poligoni.</span><span class="sxs-lookup"><span data-stu-id="66c7b-121">Enables antialiasing of polygons.</span></span> |



 

<span data-ttu-id="66c7b-122">Usare le chiamate [**glDisable**](gldisable.md) equivalenti per disattivare l'anti-aliasing.</span><span class="sxs-lookup"><span data-stu-id="66c7b-122">Use the equivalent [**glDisable**](gldisable.md) calls to turn off antialiasing.</span></span>

<span data-ttu-id="66c7b-123">In IRIS GL è possibile controllare la qualità dell'anti-aliasing chiamando:</span><span class="sxs-lookup"><span data-stu-id="66c7b-123">In IRIS GL, you can control the quality of the antialiasing by calling:</span></span>


```C++
linesmooth(SML_ON + SML_SMOOTHER);
```



<span data-ttu-id="66c7b-124">OpenGL fornisce un [**glHint**](glhint.md)controluse simile:</span><span class="sxs-lookup"><span data-stu-id="66c7b-124">OpenGL provides similar controluse [**glHint**](glhint.md):</span></span>


```C++
glHint(GL_POINT_SMOOTH_HINT, hintMode); 
glHint(GL_LINE_SMOOTH_HINT, hintMode); 
glHint(GL_POLYGON_SMOOTH_HINT, hintMode);
```



<span data-ttu-id="66c7b-125">dove *hintMode* è uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="66c7b-125">where *hintMode* is one of the following:</span></span>

-   <span data-ttu-id="66c7b-126">GL \_ più gradevole (usare la migliore smussatura della qualità).</span><span class="sxs-lookup"><span data-stu-id="66c7b-126">GL\_NICEST (Use the highest quality smoothing.)</span></span>
-   <span data-ttu-id="66c7b-127">GL \_ più veloce (usare la smussatura più efficiente).</span><span class="sxs-lookup"><span data-stu-id="66c7b-127">GL\_FASTEST (Use the most efficient smoothing.)</span></span>
-   <span data-ttu-id="66c7b-128">GL \_ dont \_ care</span><span class="sxs-lookup"><span data-stu-id="66c7b-128">GL\_DONT\_CARE</span></span>

<span data-ttu-id="66c7b-129">IRIS GL consente anche la correzione finale chiamando:</span><span class="sxs-lookup"><span data-stu-id="66c7b-129">IRIS GL also permits end-correction by calling:</span></span>


```C++
linesmooth(SML_ON +  SML_END_CORRECT);
```



<span data-ttu-id="66c7b-130">OpenGL non ha un equivalente per questa funzione.</span><span class="sxs-lookup"><span data-stu-id="66c7b-130">OpenGL has no equivalent for this function.</span></span>

 

 




