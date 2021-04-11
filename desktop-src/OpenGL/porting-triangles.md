---
title: Triangoli di porting
description: È possibile creare tre tipi di triangoli in triangoli separati di OpenGL, strisce triangolari e ventole a triangolo.
ms.assetid: 48617892-c9a0-4c67-b42e-afa4243023e7
keywords:
- Porting di IRIS GL, triangoli
- porting da IRIS GL, triangoli
- porting in OpenGL da IRIS GL, triangoli
- Porting OpenGL da IRIS GL, triangoli
- funzioni di disegno, triangoli
- triangoli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad0c7a0af4b538bb951cf0d1c5f2e12b2e1badda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330988"
---
# <a name="porting-triangles"></a><span data-ttu-id="6783e-109">Triangoli di porting</span><span class="sxs-lookup"><span data-stu-id="6783e-109">Porting Triangles</span></span>

<span data-ttu-id="6783e-110">È possibile creare tre tipi di triangoli in OpenGL: triangoli separati, strisce triangolari e ventole di triangolo.</span><span class="sxs-lookup"><span data-stu-id="6783e-110">You can draw three types of triangles in OpenGL: separate triangles, triangle strips, and triangle fans.</span></span>

<span data-ttu-id="6783e-111">OpenGL non ha un equivalente per la funzione **swaptmesh** di Iris GL.</span><span class="sxs-lookup"><span data-stu-id="6783e-111">OpenGL has no equivalent for the IRIS GL **swaptmesh** function.</span></span> <span data-ttu-id="6783e-112">È possibile ottenere lo stesso effetto usando una combinazione di triangoli, strisce triangolari e ventole di triangolo.</span><span class="sxs-lookup"><span data-stu-id="6783e-112">You can achieve the same effect using a combination of triangles, triangle strips, and triangle fans.</span></span>

<span data-ttu-id="6783e-113">La tabella seguente elenca le funzioni di IRIS GL per il disegno di triangoli e le relative funzioni OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="6783e-113">The following table lists the IRIS GL functions for drawing triangles and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="6783e-114">Funzione IRIS GL</span><span class="sxs-lookup"><span data-stu-id="6783e-114">IRIS GL function</span></span>           | <span data-ttu-id="6783e-115">Parametro glBegin equivalente</span><span class="sxs-lookup"><span data-stu-id="6783e-115">Equivalent glBegin parameter</span></span> | <span data-ttu-id="6783e-116">Significato</span><span class="sxs-lookup"><span data-stu-id="6783e-116">Meaning</span></span>                                       |
|----------------------------|------------------------------|-----------------------------------------------|
|                            | <span data-ttu-id="6783e-117">triangoli GL \_</span><span class="sxs-lookup"><span data-stu-id="6783e-117">GL\_TRIANGLES</span></span>                | <span data-ttu-id="6783e-118">Triple di vertici interpretati come triangoli.</span><span class="sxs-lookup"><span data-stu-id="6783e-118">Triples of vertices interpreted as triangles.</span></span> |
| <span data-ttu-id="6783e-119">**bgntmesh**, **endtmesh**</span><span class="sxs-lookup"><span data-stu-id="6783e-119">**bgntmesh**, **endtmesh**</span></span> | <span data-ttu-id="6783e-120">\_striscia del triangolo GL \_</span><span class="sxs-lookup"><span data-stu-id="6783e-120">GL\_TRIANGLE\_STRIP</span></span>          | <span data-ttu-id="6783e-121">Strisce collegate di triangoli.</span><span class="sxs-lookup"><span data-stu-id="6783e-121">Linked strips of triangles.</span></span>                   |
|                            | <span data-ttu-id="6783e-122">\_ventola del triangolo GL \_</span><span class="sxs-lookup"><span data-stu-id="6783e-122">GL\_TRIANGLE\_FAN</span></span>            | <span data-ttu-id="6783e-123">Fan collegati di triangoli.</span><span class="sxs-lookup"><span data-stu-id="6783e-123">Linked fans of triangles.</span></span>                     |



 

<span data-ttu-id="6783e-124">??</span><span class="sxs-lookup"><span data-stu-id="6783e-124">??</span></span>

 

 




