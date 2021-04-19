---
description: Il metodo OnWaitStart viene chiamato quando il filtro inizia ad attendere l'ora di presentazione di un campione.
ms.assetid: 598cd676-3afe-4ec9-ae38-83971412e6a7
title: Metodo CBaseRenderer. OnWaitStart (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c2f88f11e370c6d1962ae6076f4c8f5eecc31407
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333345"
---
# <a name="cbaserendereronwaitstart-method"></a><span data-ttu-id="425dd-103">CBaseRenderer. OnWaitStart, metodo</span><span class="sxs-lookup"><span data-stu-id="425dd-103">CBaseRenderer.OnWaitStart method</span></span>

<span data-ttu-id="425dd-104">Il `OnWaitStart` metodo viene chiamato quando il filtro inizia ad attendere l'ora di presentazione di un campione.</span><span class="sxs-lookup"><span data-stu-id="425dd-104">The `OnWaitStart` method is called when the filter starts waiting for a sample's presentation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="425dd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="425dd-105">Syntax</span></span>


```C++
virtual void OnWaitStart();
```



## <a name="parameters"></a><span data-ttu-id="425dd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="425dd-106">Parameters</span></span>

<span data-ttu-id="425dd-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="425dd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="425dd-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="425dd-108">Return value</span></span>

<span data-ttu-id="425dd-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="425dd-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="425dd-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="425dd-110">Remarks</span></span>

<span data-ttu-id="425dd-111">Il metodo [**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md) chiama questo metodo quando inizia ad attendere l'ora di presentazione di un campione.</span><span class="sxs-lookup"><span data-stu-id="425dd-111">The [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md) method calls this method when it begins waiting for a sample's presentation time.</span></span> <span data-ttu-id="425dd-112">Questo metodo non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.</span><span class="sxs-lookup"><span data-stu-id="425dd-112">This method does not do anything in the base class, but the derived class can override it.</span></span>

<span data-ttu-id="425dd-113">Se si implementa il controllo della qualità, è possibile eseguire l'override di questo metodo insieme al metodo [**CBaseRenderer:: OnWaitEnd**](cbaserenderer-onwaitend.md) .</span><span class="sxs-lookup"><span data-stu-id="425dd-113">If you are implementing quality control, you might override this method along with the [**CBaseRenderer::OnWaitEnd**](cbaserenderer-onwaitend.md) method.</span></span> <span data-ttu-id="425dd-114">È possibile utilizzare questi metodi per tenere traccia delle prestazioni del filtro.</span><span class="sxs-lookup"><span data-stu-id="425dd-114">You can use these methods to track the filter's performance.</span></span>

## <a name="requirements"></a><span data-ttu-id="425dd-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="425dd-115">Requirements</span></span>



| <span data-ttu-id="425dd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="425dd-116">Requirement</span></span> | <span data-ttu-id="425dd-117">Valore</span><span class="sxs-lookup"><span data-stu-id="425dd-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="425dd-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="425dd-118">Header</span></span><br/>  | <dl> <span data-ttu-id="425dd-119"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="425dd-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="425dd-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="425dd-120">Library</span></span><br/> | <dl> <span data-ttu-id="425dd-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="425dd-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="425dd-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="425dd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="425dd-123">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="425dd-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




