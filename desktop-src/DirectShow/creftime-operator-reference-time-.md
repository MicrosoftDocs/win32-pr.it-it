---
description: L' \_ operatore time () di riferimento esegue il cast dell'oggetto a un \_ tipo di dati time di riferimento.
ms.assetid: 36f51e03-a458-46e6-9657-977b263c127f
title: Metodo CRefTime. operator REFERENCE_TIME (Reftime. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3ceeeb00ba1de4f305f87ef3fe15e70a8d91457
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329046"
---
# <a name="creftimeoperator-reference_time-method"></a><span data-ttu-id="e5c38-103">Metodo time di riferimento CRefTime. Operator \_</span><span class="sxs-lookup"><span data-stu-id="e5c38-103">CRefTime.operator REFERENCE\_TIME method</span></span>

<span data-ttu-id="e5c38-104">L' `REFERENCE_TIME()` operatore esegue il cast dell'oggetto a un tipo di dati [**\_ time di riferimento**](reference-time.md) .</span><span class="sxs-lookup"><span data-stu-id="e5c38-104">The `REFERENCE_TIME()` operator casts the object to a [**REFERENCE\_TIME**](reference-time.md) data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5c38-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5c38-105">Syntax</span></span>


```C++
REFERENCE_TIME operator REFERENCE_TIME() const;
```



## <a name="parameters"></a><span data-ttu-id="e5c38-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e5c38-106">Parameters</span></span>

<span data-ttu-id="e5c38-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e5c38-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e5c38-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e5c38-108">Return value</span></span>

<span data-ttu-id="e5c38-109">Restituisce il valore di [**CRefTime:: m \_ Time**](creftime-m-time.md).</span><span class="sxs-lookup"><span data-stu-id="e5c38-109">Returns the value of [**CRefTime::m\_time**](creftime-m-time.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e5c38-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5c38-110">Remarks</span></span>

<span data-ttu-id="e5c38-111">Nell'esempio seguente viene illustrato come utilizzare questo operatore cast:</span><span class="sxs-lookup"><span data-stu-id="e5c38-111">The following example shows how to use this cast operator:</span></span>


```C++
CRefTime cRT(1000);
REFERENCE_TIME rt = (REFERENCE_TIME)cRT;
```



## <a name="requirements"></a><span data-ttu-id="e5c38-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5c38-112">Requirements</span></span>



| <span data-ttu-id="e5c38-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5c38-113">Requirement</span></span> | <span data-ttu-id="e5c38-114">Valore</span><span class="sxs-lookup"><span data-stu-id="e5c38-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5c38-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e5c38-115">Header</span></span><br/>  | <dl> <span data-ttu-id="e5c38-116"><dt>Reftime. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e5c38-116"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e5c38-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="e5c38-117">Library</span></span><br/> | <dl> <span data-ttu-id="e5c38-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e5c38-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




