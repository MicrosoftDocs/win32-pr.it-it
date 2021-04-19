---
description: Chiamato da un qualsiasi hit shader per rifiutare l'hit e terminare lo shader.
ms.assetid: ''
title: IgnoreHit (funzione)
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IgnoreHit
api_type:
- NA
ms.openlocfilehash: 66d450ce5a03e07e779ca5131443cdf67398cf19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305194"
---
# <a name="ignorehit-function"></a><span data-ttu-id="cf4a3-103">IgnoreHit (funzione)</span><span class="sxs-lookup"><span data-stu-id="cf4a3-103">IgnoreHit function</span></span>

<span data-ttu-id="cf4a3-104">Chiamato da un [qualsiasi hit shader](any-hit-shader.md) per rifiutare l'hit e terminare lo shader.</span><span class="sxs-lookup"><span data-stu-id="cf4a3-104">Called from an [any hit shader](any-hit-shader.md) to reject the hit and end the shader.</span></span> <span data-ttu-id="cf4a3-105">La ricerca di hit prosegue senza eseguire il commit della distanza e degli attributi per l'hit corrente.</span><span class="sxs-lookup"><span data-stu-id="cf4a3-105">The hit search continues on without committing the distance and attributes for the current hit.</span></span>  <span data-ttu-id="cf4a3-106">La chiamata [**ReportHit**](reporthit-function.md) nell' [intersezione shader](intersection-shader.md), se presente, restituirà false.</span><span class="sxs-lookup"><span data-stu-id="cf4a3-106">The [**ReportHit**](reporthit-function.md) call in the [intersection shader](intersection-shader.md), if there is one, will return false.</span></span>  <span data-ttu-id="cf4a3-107">Tutte le modifiche apportate al payload del raggio fino a questo punto in qualsiasi hit shader vengono mantenute.</span><span class="sxs-lookup"><span data-stu-id="cf4a3-107">Any modifications made to the ray payload up to this point in the any hit shader are preserved.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf4a3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cf4a3-108">Syntax</span></span>

```
void IgnoreHit();

```


## <a name="return-value"></a><span data-ttu-id="cf4a3-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cf4a3-109">Return Value</span></span>

<span data-ttu-id="cf4a3-110">**void**</span><span class="sxs-lookup"><span data-stu-id="cf4a3-110">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="cf4a3-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="cf4a3-111">Remarks</span></span>

<span data-ttu-id="cf4a3-112">Questa funzione può essere chiamata dai seguenti tipi di shader raytracing:</span><span class="sxs-lookup"><span data-stu-id="cf4a3-112">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="cf4a3-113">**Qualsiasi hit shader**</span><span class="sxs-lookup"><span data-stu-id="cf4a3-113">**Any Hit Shader**</span></span>](any-hit-shader.md)




## <a name="see-also"></a><span data-ttu-id="cf4a3-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cf4a3-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf4a3-115">Guida di riferimento a Direct3D 12 raytracing HLSL</span><span class="sxs-lookup"><span data-stu-id="cf4a3-115">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




