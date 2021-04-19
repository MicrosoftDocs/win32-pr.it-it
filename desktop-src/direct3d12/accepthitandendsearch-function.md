---
description: Usato in un qualsiasi hit shader per confermare l'hit corrente e quindi arrestare la ricerca di altri riscontri per il raggio.
ms.assetid: ''
title: AcceptHitAndEndSearch (funzione)
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- AcceptHitAndEndSearch
api_type:
- NA
ms.openlocfilehash: 25bbac15a26beb535a91155cdd4c411c3c669e0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304925"
---
# <a name="accepthitandendsearch-function"></a><span data-ttu-id="2d09a-103">AcceptHitAndEndSearch (funzione)</span><span class="sxs-lookup"><span data-stu-id="2d09a-103">AcceptHitAndEndSearch function</span></span>

<span data-ttu-id="2d09a-104">Usato in un [qualsiasi hit shader](any-hit-shader.md) per confermare l'hit corrente e quindi arrestare la ricerca di altri riscontri per il raggio.</span><span class="sxs-lookup"><span data-stu-id="2d09a-104">Used in an [any hit shader](any-hit-shader.md) to commit the current hit and then stop searching for more hits for the ray.</span></span> <span data-ttu-id="2d09a-105">Se è in esecuzione un'intersezione dello shader, l'esecuzione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="2d09a-105">If there is an intersection shader running, it's execution stops.</span></span>  <span data-ttu-id="2d09a-106">L'esecuzione passa all' [hit shader più vicino](closest-hit-shader.md), se abilitato, con il riscontro più vicino registrato fino a questo punto.</span><span class="sxs-lookup"><span data-stu-id="2d09a-106">Execution passes to the [closest hit shader](closest-hit-shader.md), if enabled, with the closest hit recorded so far.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d09a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d09a-107">Syntax</span></span>

```
void AcceptHitAndEndSearch();
```




## <a name="return-value"></a><span data-ttu-id="2d09a-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2d09a-108">Return Value</span></span>

<span data-ttu-id="2d09a-109">**void**</span><span class="sxs-lookup"><span data-stu-id="2d09a-109">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="2d09a-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d09a-110">Remarks</span></span>

<span data-ttu-id="2d09a-111">Questa funzione può essere chiamata dai seguenti tipi di shader raytracing:</span><span class="sxs-lookup"><span data-stu-id="2d09a-111">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="2d09a-112">**Richiamabile shader**</span><span class="sxs-lookup"><span data-stu-id="2d09a-112">**Callable Shader**</span></span>](callable-shader.md)
* [<span data-ttu-id="2d09a-113">**Hit shader più vicino**</span><span class="sxs-lookup"><span data-stu-id="2d09a-113">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="2d09a-114">**Lo shader manca**</span><span class="sxs-lookup"><span data-stu-id="2d09a-114">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="2d09a-115">**Shader di generazione del Ray**</span><span class="sxs-lookup"><span data-stu-id="2d09a-115">**Ray Generation Shader**</span></span>](ray-generation-shader.md)



## <a name="see-also"></a><span data-ttu-id="2d09a-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d09a-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d09a-117">Guida di riferimento a Direct3D 12 raytracing HLSL</span><span class="sxs-lookup"><span data-stu-id="2d09a-117">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




