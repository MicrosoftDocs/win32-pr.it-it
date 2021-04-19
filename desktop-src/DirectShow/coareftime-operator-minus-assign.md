---
description: Questo operatore sottrae un'ora di riferimento da un'altra e imposta questo oggetto sul risultato.
ms.assetid: 573b6f6b-7634-4e78-872c-f869b59a75e2
title: Metodo COARefTime. Operator-= (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator-=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 29afc98da01351f63df45997b8cc338e17a1234c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330300"
---
# <a name="coareftimeoperator--method"></a><span data-ttu-id="c1799-103">Metodo COARefTime. operator-=</span><span class="sxs-lookup"><span data-stu-id="c1799-103">COARefTime.operator-= method</span></span>

<span data-ttu-id="c1799-104">Questo operatore sottrae un'ora di riferimento da un'altra e imposta questo oggetto sul risultato.</span><span class="sxs-lookup"><span data-stu-id="c1799-104">This operator subtracts one reference time from another, and sets this object to the result.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1799-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1799-105">Syntax</span></span>


```C++
COARefTime& operator-=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="c1799-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c1799-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1799-107">*RT* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="c1799-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c1799-108">Riferimento all'oggetto **COARefTime** da sottrarre.</span><span class="sxs-lookup"><span data-stu-id="c1799-108">Reference to the **COARefTime** object to subtract.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1799-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c1799-109">Return value</span></span>

<span data-ttu-id="c1799-110">Restituisce un riferimento all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c1799-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1799-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1799-111">Requirements</span></span>



| <span data-ttu-id="c1799-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1799-112">Requirement</span></span> | <span data-ttu-id="c1799-113">Valore</span><span class="sxs-lookup"><span data-stu-id="c1799-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1799-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c1799-114">Header</span></span><br/>  | <dl> <span data-ttu-id="c1799-115"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1799-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c1799-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="c1799-116">Library</span></span><br/> | <dl> <span data-ttu-id="c1799-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c1799-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1799-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1799-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1799-119">**Classe COARefTime**</span><span class="sxs-lookup"><span data-stu-id="c1799-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




