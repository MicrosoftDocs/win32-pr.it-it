---
description: Questo operatore moltiplica un'ora di riferimento per un valore.
ms.assetid: f575fd41-1d3e-43a6-abf8-8e64093e408e
title: Metodo COARefTime. Operator * (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator*
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c62a4282f7a43ba3d7ba35daf81530f8b246be32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330293"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="4d480-103">Metodo COARefTime. Operator \*</span><span class="sxs-lookup"><span data-stu-id="4d480-103">COARefTime.operator\* method</span></span>

<span data-ttu-id="4d480-104">Questo operatore moltiplica un'ora di riferimento per un valore.</span><span class="sxs-lookup"><span data-stu-id="4d480-104">This operator multiplies a reference time by a value.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d480-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d480-105">Syntax</span></span>


```C++
COARefTime operator*(
   LONG l
);
```



## <a name="parameters"></a><span data-ttu-id="4d480-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4d480-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d480-107">*l*</span><span class="sxs-lookup"><span data-stu-id="4d480-107">*l*</span></span> 
</dt> <dd>

<span data-ttu-id="4d480-108">Moltiplicatore.</span><span class="sxs-lookup"><span data-stu-id="4d480-108">Multiplier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d480-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4d480-109">Return value</span></span>

<span data-ttu-id="4d480-110">Restituisce un nuovo oggetto **COARefTime** uguale al prodotto di questo oggetto e **l**.</span><span class="sxs-lookup"><span data-stu-id="4d480-110">Returns a new **COARefTime** object equal to the product of this object and **l**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d480-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d480-111">Requirements</span></span>



| <span data-ttu-id="4d480-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d480-112">Requirement</span></span> | <span data-ttu-id="4d480-113">Valore</span><span class="sxs-lookup"><span data-stu-id="4d480-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d480-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4d480-114">Header</span></span><br/>  | <dl> <span data-ttu-id="4d480-115"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4d480-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4d480-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="4d480-116">Library</span></span><br/> | <dl> <span data-ttu-id="4d480-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4d480-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d480-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d480-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d480-119">**Classe COARefTime**</span><span class="sxs-lookup"><span data-stu-id="4d480-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




