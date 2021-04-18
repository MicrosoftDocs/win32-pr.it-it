---
description: Il metodo SetAbortSignal imposta un flag che indica se arrestare il rendering e rifiutare ulteriori esempi.
ms.assetid: 2dbf3b4d-e285-4d17-a77c-01a16c09d148
title: Metodo CBaseRenderer. SetAbortSignal (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetAbortSignal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70527d5e43ccab4df7b2110a33df8d813bd16d28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329533"
---
# <a name="cbaserenderersetabortsignal-method"></a><span data-ttu-id="82321-103">CBaseRenderer. SetAbortSignal, metodo</span><span class="sxs-lookup"><span data-stu-id="82321-103">CBaseRenderer.SetAbortSignal method</span></span>

<span data-ttu-id="82321-104">Il `SetAbortSignal` metodo imposta un flag che indica se arrestare il rendering e rifiutare ulteriori esempi.</span><span class="sxs-lookup"><span data-stu-id="82321-104">The `SetAbortSignal` method sets a flag which indicates whether to stop rendering and reject further samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="82321-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82321-105">Syntax</span></span>


```C++
void SetAbortSignal(
   BOOL bAbort
);
```



## <a name="parameters"></a><span data-ttu-id="82321-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="82321-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82321-107">*bAbort*</span><span class="sxs-lookup"><span data-stu-id="82321-107">*bAbort*</span></span> 
</dt> <dd>

<span data-ttu-id="82321-108">Valore booleano che indica se arrestare il rendering.</span><span class="sxs-lookup"><span data-stu-id="82321-108">Boolean value indicating whether to stop rendering.</span></span> <span data-ttu-id="82321-109">Se **true**, il filtro non eseguirà il rendering di altri esempi.</span><span class="sxs-lookup"><span data-stu-id="82321-109">If **TRUE**, the filter will not render any more samples.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82321-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="82321-110">Return value</span></span>

<span data-ttu-id="82321-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="82321-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82321-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="82321-112">Remarks</span></span>

<span data-ttu-id="82321-113">Questo metodo imposta il flag [**CBaseRenderer:: m \_ bAbort**](cbaserenderer-m-babort.md) .</span><span class="sxs-lookup"><span data-stu-id="82321-113">This method sets the [**CBaseRenderer::m\_bAbort**](cbaserenderer-m-babort.md) flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="82321-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82321-114">Requirements</span></span>



| <span data-ttu-id="82321-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="82321-115">Requirement</span></span> | <span data-ttu-id="82321-116">Valore</span><span class="sxs-lookup"><span data-stu-id="82321-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82321-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="82321-117">Header</span></span><br/>  | <dl> <span data-ttu-id="82321-118"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="82321-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="82321-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="82321-119">Library</span></span><br/> | <dl> <span data-ttu-id="82321-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="82321-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82321-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82321-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82321-122">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="82321-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




