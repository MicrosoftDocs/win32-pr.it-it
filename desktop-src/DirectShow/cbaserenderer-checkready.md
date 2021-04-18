---
description: Il metodo CheckReady esegue una query per determinare se una transizione di stato è stata completata.
ms.assetid: dfa669ed-a5ab-498e-9fc2-ff15d6ddbc13
title: Metodo CBaseRenderer. CheckReady (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CheckReady
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 28c0c8bcb6efb0e3cbd648c1e45d36e8b18d4b74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329399"
---
# <a name="cbaserenderercheckready-method"></a><span data-ttu-id="18a66-103">CBaseRenderer. CheckReady, metodo</span><span class="sxs-lookup"><span data-stu-id="18a66-103">CBaseRenderer.CheckReady method</span></span>

<span data-ttu-id="18a66-104">Il `CheckReady` metodo esegue una query per determinare se una transizione di stato è stata completata.</span><span class="sxs-lookup"><span data-stu-id="18a66-104">The `CheckReady` method queries whether a state transition is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="18a66-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="18a66-105">Syntax</span></span>


```C++
BOOL CheckReady();
```



## <a name="parameters"></a><span data-ttu-id="18a66-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="18a66-106">Parameters</span></span>

<span data-ttu-id="18a66-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="18a66-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="18a66-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="18a66-108">Return value</span></span>

<span data-ttu-id="18a66-109">Restituisce **true** se la transizione di stato è completa oppure **false** se il filtro è ancora in fase di transizione a un nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="18a66-109">Returns **TRUE** if the state transition is complete, or **FALSE** if the filter is still transitioning to a new state.</span></span>

## <a name="requirements"></a><span data-ttu-id="18a66-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18a66-110">Requirements</span></span>



| <span data-ttu-id="18a66-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="18a66-111">Requirement</span></span> | <span data-ttu-id="18a66-112">Valore</span><span class="sxs-lookup"><span data-stu-id="18a66-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18a66-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="18a66-113">Header</span></span><br/>  | <dl> <span data-ttu-id="18a66-114"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="18a66-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="18a66-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="18a66-115">Library</span></span><br/> | <dl> <span data-ttu-id="18a66-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="18a66-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18a66-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18a66-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18a66-118">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="18a66-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="18a66-119">**CBaseRenderer:: nobattistrada**</span><span class="sxs-lookup"><span data-stu-id="18a66-119">**CBaseRenderer::NotReady**</span></span>](cbaserenderer-notready.md)
</dt> <dt>

[<span data-ttu-id="18a66-120">**CBaseRenderer:: Ready**</span><span class="sxs-lookup"><span data-stu-id="18a66-120">**CBaseRenderer::Ready**</span></span>](cbaserenderer-ready.md)
</dt> </dl>

 

 




