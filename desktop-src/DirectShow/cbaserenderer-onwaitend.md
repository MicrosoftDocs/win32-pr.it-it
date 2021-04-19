---
description: Il metodo OnWaitEnd viene chiamato quando il filtro viene eseguito in attesa dell'ora di presentazione di un campione.
ms.assetid: 47ff8f79-da69-4dcf-8cbb-02c1b56e382e
title: Metodo CBaseRenderer. OnWaitEnd (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5a290ad5d39fc83a4213d1c8a32119b4caa9858
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333346"
---
# <a name="cbaserendereronwaitend-method"></a><span data-ttu-id="b5c90-103">CBaseRenderer. OnWaitEnd, metodo</span><span class="sxs-lookup"><span data-stu-id="b5c90-103">CBaseRenderer.OnWaitEnd method</span></span>

<span data-ttu-id="b5c90-104">Il `OnWaitEnd` metodo viene chiamato quando il filtro viene eseguito in attesa dell'ora di presentazione di un campione.</span><span class="sxs-lookup"><span data-stu-id="b5c90-104">The `OnWaitEnd` method is called when the filter is done waiting for a sample's presentation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5c90-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5c90-105">Syntax</span></span>


```C++
virtual void OnWaitEnd();
```



## <a name="parameters"></a><span data-ttu-id="b5c90-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5c90-106">Parameters</span></span>

<span data-ttu-id="b5c90-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b5c90-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b5c90-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5c90-108">Return value</span></span>

<span data-ttu-id="b5c90-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="b5c90-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5c90-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5c90-110">Remarks</span></span>

<span data-ttu-id="b5c90-111">Il metodo [**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md) chiama questo metodo quando ha terminato l'attesa dell'ora di presentazione di un campione.</span><span class="sxs-lookup"><span data-stu-id="b5c90-111">The [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md) method calls this method when it has finished waiting for a sample's presentation time.</span></span> <span data-ttu-id="b5c90-112">Questo metodo non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.</span><span class="sxs-lookup"><span data-stu-id="b5c90-112">This method does not do anything in the base class, but the derived class can override it.</span></span>

<span data-ttu-id="b5c90-113">Se si implementa il controllo della qualità, è possibile eseguire l'override di questo metodo insieme al metodo [**CBaseRenderer:: OnWaitStart**](cbaserenderer-onwaitstart.md) .</span><span class="sxs-lookup"><span data-stu-id="b5c90-113">If you are implementing quality control, you might override this method along with the [**CBaseRenderer::OnWaitStart**](cbaserenderer-onwaitstart.md) method.</span></span> <span data-ttu-id="b5c90-114">È possibile utilizzare questi metodi per tenere traccia delle prestazioni del filtro.</span><span class="sxs-lookup"><span data-stu-id="b5c90-114">You can use these methods to track the filter's performance.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5c90-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5c90-115">Requirements</span></span>



| <span data-ttu-id="b5c90-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5c90-116">Requirement</span></span> | <span data-ttu-id="b5c90-117">Valore</span><span class="sxs-lookup"><span data-stu-id="b5c90-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5c90-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5c90-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b5c90-119"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b5c90-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b5c90-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="b5c90-120">Library</span></span><br/> | <dl> <span data-ttu-id="b5c90-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b5c90-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5c90-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5c90-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5c90-123">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="b5c90-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




