---
description: Chiamato da un'intersezione shader per segnalare un'intersezione del raggio.
ms.assetid: ''
title: ReportHit (funzione)
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReportHit
api_type:
- NA
ms.openlocfilehash: 58d109f184974f76c533aaeee055f1ebf21d10eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305193"
---
# <a name="reporthit-function"></a><span data-ttu-id="1e283-103">ReportHit (funzione)</span><span class="sxs-lookup"><span data-stu-id="1e283-103">ReportHit function</span></span>

<span data-ttu-id="1e283-104">Chiamato da un'intersezione [shader](intersection-shader.md) per segnalare un'intersezione del raggio.</span><span class="sxs-lookup"><span data-stu-id="1e283-104">Called by an [intersection shader](intersection-shader.md) to report a ray intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e283-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1e283-105">Syntax</span></span>
<span data-ttu-id="1e283-106">Questa definizione di funzione intrinseca è equivalente al modello di funzione seguente:</span><span class="sxs-lookup"><span data-stu-id="1e283-106">This intrinsic function definition is equivalent to the following function template:</span></span>

```
template<attr_t>
bool ReportHit(float THit, uint HitKind, attr_t Attributes);
```



## <a name="parameters"></a><span data-ttu-id="1e283-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="1e283-107">Parameters</span></span>

`THit`

<span data-ttu-id="1e283-108">Valore float che specifica la distanza parametrica dell'intersezione.</span><span class="sxs-lookup"><span data-stu-id="1e283-108">A float value specifying the parametric distance of the intersection..</span></span>

`HitKind`

<span data-ttu-id="1e283-109">Unsigned Integer che identifica il tipo di hit che si è verificato.</span><span class="sxs-lookup"><span data-stu-id="1e283-109">An unsigned integer that identifies the type of hit that occurred.</span></span>  <span data-ttu-id="1e283-110">Si tratta di un valore specificato dall'utente compreso nell'intervallo 0-127.</span><span class="sxs-lookup"><span data-stu-id="1e283-110">This is a user-specified value in the range of 0-127.</span></span>  <span data-ttu-id="1e283-111">Il valore può essere letto da [tutti](any-hit-shader.md) gli hit shader hit o [Closer](closest-hit-shader.md) con la funzione intrinseca **HitKind** .</span><span class="sxs-lookup"><span data-stu-id="1e283-111">The value can be read by [any hit](any-hit-shader.md) or [closest hit](closest-hit-shader.md) shaders with the **HitKind** intrinsic.</span></span>

`Attributes`

<span data-ttu-id="1e283-112">Struttura della struttura dell' [**attributo di intersezione**](intersection-attributes.md) definita dall'utente che specifica gli attributi di intersezione.</span><span class="sxs-lookup"><span data-stu-id="1e283-112">The user-defined [**Intersection Attribute Structure**](intersection-attributes.md) structure specifying the intersection attributes.</span></span>  

## <a name="return-value"></a><span data-ttu-id="1e283-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1e283-113">Return Value</span></span>

<span data-ttu-id="1e283-114">**bool** True se il hit è stato accettato.</span><span class="sxs-lookup"><span data-stu-id="1e283-114">**bool** True if the hit was accepted.</span></span>  <span data-ttu-id="1e283-115">Un hit viene rifiutato se l'oggetto *SETI* non è compreso nell'intervallo corrente dei raggi o se qualsiasi hit shader chiama [**IgnoreHit**](ignorehit-function.md).</span><span class="sxs-lookup"><span data-stu-id="1e283-115">A hit is rejected if *THit* is outside the current ray interval, or the any hit shader calls [**IgnoreHit**](ignorehit-function.md).</span></span>  <span data-ttu-id="1e283-116">L'intervallo di raggi corrente è definito da **RayTMin** e **RayTCurrent**.</span><span class="sxs-lookup"><span data-stu-id="1e283-116">The current ray interval is defined by **RayTMin** and **RayTCurrent**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e283-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="1e283-117">Remarks</span></span>

<span data-ttu-id="1e283-118">Questa funzione può essere chiamata dai seguenti tipi di shader raytracing:</span><span class="sxs-lookup"><span data-stu-id="1e283-118">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="1e283-119">**Intersezione shader**</span><span class="sxs-lookup"><span data-stu-id="1e283-119">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="1e283-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e283-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e283-121">Guida di riferimento a Direct3D 12 raytracing HLSL</span><span class="sxs-lookup"><span data-stu-id="1e283-121">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




