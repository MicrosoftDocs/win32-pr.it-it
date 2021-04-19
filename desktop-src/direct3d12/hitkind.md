---
description: Restituisce il valore passato come parametro HitKind a ReportHit.
ms.assetid: ''
title: HitKind
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HitKind
api_type:
- NA
ms.openlocfilehash: 81638996dbf69097154a2f1c235f6ab26c28dc8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304999"
---
# <a name="hitkind"></a><span data-ttu-id="f4dce-103">HitKind</span><span class="sxs-lookup"><span data-stu-id="f4dce-103">HitKind</span></span>

<span data-ttu-id="f4dce-104">Restituisce il valore passato come parametro **HitKind** a [**ReportHit**](reporthit-function.md).</span><span class="sxs-lookup"><span data-stu-id="f4dce-104">Returns the value passed as the **HitKind** parameter to [**ReportHit**](reporthit-function.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f4dce-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4dce-105">Syntax</span></span>

```
uint HitKind();

```



## <a name="remarks"></a><span data-ttu-id="f4dce-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="f4dce-106">Remarks</span></span>

<span data-ttu-id="f4dce-107">Se l'intersezione è stata segnalata dall'intersezione di un triangolo a funzione fissa, **HitKind** sarà uno dei front-end del **\_ triangolo di tipo \_ \_ \_ hit** (254) o il retro del **triangolo di \_ tipo \_ \_ \_ hit** (255).</span><span class="sxs-lookup"><span data-stu-id="f4dce-107">If the intersection was reported by fixed-function triangle intersection, **HitKind** will be one of **HIT\_KIND\_TRIANGLE\_FRONT\_FACE** (254) or **HIT\_KIND\_TRIANGLE\_BACK\_FACE** (255).</span></span>

<span data-ttu-id="f4dce-108">Questa funzione può essere chiamata dai seguenti tipi di shader raytracing:</span><span class="sxs-lookup"><span data-stu-id="f4dce-108">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="f4dce-109">**Qualsiasi hit shader**</span><span class="sxs-lookup"><span data-stu-id="f4dce-109">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="f4dce-110">**Hit shader più vicino**</span><span class="sxs-lookup"><span data-stu-id="f4dce-110">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="f4dce-111">**Intersezione shader**</span><span class="sxs-lookup"><span data-stu-id="f4dce-111">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="f4dce-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4dce-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4dce-113">Guida di riferimento a Direct3D 12 raytracing HLSL</span><span class="sxs-lookup"><span data-stu-id="f4dce-113">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




