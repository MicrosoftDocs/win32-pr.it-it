---
description: Questo operatore aggiunge due tempi di riferimento e imposta questo oggetto sul risultato.
ms.assetid: 6d29014b-0e31-497e-8326-e3fefc022227
title: Metodo COARefTime. Operator + = (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator+=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a03d9e98c3c2f2ca09c3f90f2cb0867d976e02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330290"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="5fc60-103">COARefTime. Operator + = (metodo)</span><span class="sxs-lookup"><span data-stu-id="5fc60-103">COARefTime.operator+= method</span></span>

<span data-ttu-id="5fc60-104">Questo operatore aggiunge due tempi di riferimento e imposta questo oggetto sul risultato.</span><span class="sxs-lookup"><span data-stu-id="5fc60-104">This operator adds two reference times, and sets this object to the result.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fc60-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5fc60-105">Syntax</span></span>


```C++
COARefTime& operator+=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="5fc60-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5fc60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fc60-107">*RT* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="5fc60-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="5fc60-108">Riferimento all'oggetto **COARefTime** da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="5fc60-108">Reference to the **COARefTime** object to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fc60-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5fc60-109">Return value</span></span>

<span data-ttu-id="5fc60-110">Restituisce un riferimento all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5fc60-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fc60-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5fc60-111">Requirements</span></span>



| <span data-ttu-id="5fc60-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fc60-112">Requirement</span></span> | <span data-ttu-id="5fc60-113">Valore</span><span class="sxs-lookup"><span data-stu-id="5fc60-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fc60-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5fc60-114">Header</span></span><br/>  | <dl> <span data-ttu-id="5fc60-115"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5fc60-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5fc60-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="5fc60-116">Library</span></span><br/> | <dl> <span data-ttu-id="5fc60-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5fc60-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fc60-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5fc60-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fc60-119">**Classe COARefTime**</span><span class="sxs-lookup"><span data-stu-id="5fc60-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




