---
description: Questo operatore divide un'ora di riferimento per un valore.
ms.assetid: fb2e2a4b-dc0b-42e3-86c7-8aa2c60daedc
title: Metodo COARefTime. Operator/(Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator/
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e1e4d7b7adb881ac11988a2d2c46946ff6cddcc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330238"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="d94ef-103">COARefTime. Operator/(metodo)</span><span class="sxs-lookup"><span data-stu-id="d94ef-103">COARefTime.operator/ method</span></span>

<span data-ttu-id="d94ef-104">Questo operatore divide un'ora di riferimento per un valore.</span><span class="sxs-lookup"><span data-stu-id="d94ef-104">This operator divides a reference time by a value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d94ef-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d94ef-105">Syntax</span></span>


```C++
COARefTime operator/(
   LONG l
);
```



## <a name="parameters"></a><span data-ttu-id="d94ef-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d94ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d94ef-107">*l*</span><span class="sxs-lookup"><span data-stu-id="d94ef-107">*l*</span></span> 
</dt> <dd>

<span data-ttu-id="d94ef-108">Divisore.</span><span class="sxs-lookup"><span data-stu-id="d94ef-108">Divisor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d94ef-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d94ef-109">Return value</span></span>

<span data-ttu-id="d94ef-110">Restituisce un nuovo oggetto **COARefTime** uguale al quoziente di questo oggetto e **l**.</span><span class="sxs-lookup"><span data-stu-id="d94ef-110">Returns a new **COARefTime** object equal to the quotient of this object and **l**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d94ef-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d94ef-111">Requirements</span></span>



| <span data-ttu-id="d94ef-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d94ef-112">Requirement</span></span> | <span data-ttu-id="d94ef-113">Valore</span><span class="sxs-lookup"><span data-stu-id="d94ef-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d94ef-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d94ef-114">Header</span></span><br/>  | <dl> <span data-ttu-id="d94ef-115"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d94ef-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d94ef-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="d94ef-116">Library</span></span><br/> | <dl> <span data-ttu-id="d94ef-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d94ef-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d94ef-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d94ef-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d94ef-119">**Classe COARefTime**</span><span class="sxs-lookup"><span data-stu-id="d94ef-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




