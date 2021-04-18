---
description: Questo operatore sottrae un'ora di riferimento da un'altra.
ms.assetid: 5691cd76-0d25-45c0-bb58-6668abe1db01
title: Metodo COARefTime. Operator-(Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator-
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e51ee8aaed69830a498d1d22cebdc3927987f045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327542"
---
# <a name="coareftimeoperator--method"></a><span data-ttu-id="789b3-103">COARefTime. Operator-(metodo)</span><span class="sxs-lookup"><span data-stu-id="789b3-103">COARefTime.operator- method</span></span>

<span data-ttu-id="789b3-104">Questo operatore sottrae un'ora di riferimento da un'altra.</span><span class="sxs-lookup"><span data-stu-id="789b3-104">This operator subtracts one reference time from another.</span></span>

## <a name="syntax"></a><span data-ttu-id="789b3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="789b3-105">Syntax</span></span>


```C++
COARefTime operator-(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="789b3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="789b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="789b3-107">*RT* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="789b3-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="789b3-108">Riferimento all'oggetto **COARefTime** da sottrarre.</span><span class="sxs-lookup"><span data-stu-id="789b3-108">Reference to the **COARefTime** object to subtract.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="789b3-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="789b3-109">Return value</span></span>

<span data-ttu-id="789b3-110">Restituisce un nuovo oggetto **COARefTime** uguale alla differenza dei tempi di riferimento.</span><span class="sxs-lookup"><span data-stu-id="789b3-110">Returns a new **COARefTime** object equal to the difference of the reference times.</span></span>

## <a name="requirements"></a><span data-ttu-id="789b3-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="789b3-111">Requirements</span></span>



| <span data-ttu-id="789b3-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="789b3-112">Requirement</span></span> | <span data-ttu-id="789b3-113">Valore</span><span class="sxs-lookup"><span data-stu-id="789b3-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="789b3-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="789b3-114">Header</span></span><br/>  | <dl> <span data-ttu-id="789b3-115"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="789b3-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="789b3-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="789b3-116">Library</span></span><br/> | <dl> <span data-ttu-id="789b3-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="789b3-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="789b3-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="789b3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="789b3-119">**Classe COARefTime**</span><span class="sxs-lookup"><span data-stu-id="789b3-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




