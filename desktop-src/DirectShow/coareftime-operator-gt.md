---
description: Questo operatore verifica se un tempo di riferimento è maggiore di un altro.
ms.assetid: db281040-9bcf-41fc-95b4-5481ffc5061f
title: Metodo COARefTime. operator> (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator>
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c796bd5194c5bdb2dcbe260b803274962f81347
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333273"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="b7ad8-103">Metodo COARefTime. operator></span><span class="sxs-lookup"><span data-stu-id="b7ad8-103">COARefTime.operator> method</span></span>

<span data-ttu-id="b7ad8-104">Questo operatore verifica se un tempo di riferimento è maggiore di un altro.</span><span class="sxs-lookup"><span data-stu-id="b7ad8-104">This operator tests if one reference time is greater than another.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7ad8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7ad8-105">Syntax</span></span>


```C++
BOOL operator>(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="b7ad8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b7ad8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7ad8-107">*RT* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="b7ad8-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="b7ad8-108">Riferimento all'oggetto **COARefTime** da confrontare.</span><span class="sxs-lookup"><span data-stu-id="b7ad8-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7ad8-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b7ad8-109">Return value</span></span>

<span data-ttu-id="b7ad8-110">Restituisce **true** se l'oggetto è rigorosamente maggiore di *RT*.</span><span class="sxs-lookup"><span data-stu-id="b7ad8-110">Returns **TRUE** if this object is strictly greater than *rt*.</span></span> <span data-ttu-id="b7ad8-111">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="b7ad8-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7ad8-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7ad8-112">Requirements</span></span>



| <span data-ttu-id="b7ad8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7ad8-113">Requirement</span></span> | <span data-ttu-id="b7ad8-114">Valore</span><span class="sxs-lookup"><span data-stu-id="b7ad8-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7ad8-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7ad8-115">Header</span></span><br/>  | <dl> <span data-ttu-id="b7ad8-116"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b7ad8-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b7ad8-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="b7ad8-117">Library</span></span><br/> | <dl> <span data-ttu-id="b7ad8-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b7ad8-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7ad8-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7ad8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7ad8-120">**Classe COARefTime**</span><span class="sxs-lookup"><span data-stu-id="b7ad8-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




