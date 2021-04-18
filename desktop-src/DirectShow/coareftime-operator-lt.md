---
description: Questo operatore verifica se un tempo di riferimento è minore di un altro.
ms.assetid: 709fb861-a836-4a20-8c93-c0e8ab79f377
title: Metodo COARefTime. operator< (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator<
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c61403b959f8b5ee19e9ba0d9cd0ab4db54c124
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330303"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="bed7c-103">Metodo COARefTime. operator<</span><span class="sxs-lookup"><span data-stu-id="bed7c-103">COARefTime.operator< method</span></span>

<span data-ttu-id="bed7c-104">Questo operatore verifica se un tempo di riferimento è minore di un altro.</span><span class="sxs-lookup"><span data-stu-id="bed7c-104">This operator tests if one reference time is less than another.</span></span>

## <a name="syntax"></a><span data-ttu-id="bed7c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bed7c-105">Syntax</span></span>


```C++
BOOL operator<(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="bed7c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bed7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bed7c-107">*RT* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="bed7c-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="bed7c-108">Riferimento all'oggetto **COARefTime** da confrontare.</span><span class="sxs-lookup"><span data-stu-id="bed7c-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bed7c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bed7c-109">Return value</span></span>

<span data-ttu-id="bed7c-110">Restituisce **true** se l'oggetto è rigorosamente minore di *RT*.</span><span class="sxs-lookup"><span data-stu-id="bed7c-110">Returns **TRUE** if this object is strictly less than *rt*.</span></span> <span data-ttu-id="bed7c-111">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="bed7c-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bed7c-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bed7c-112">Requirements</span></span>



| <span data-ttu-id="bed7c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="bed7c-113">Requirement</span></span> | <span data-ttu-id="bed7c-114">Valore</span><span class="sxs-lookup"><span data-stu-id="bed7c-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bed7c-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bed7c-115">Header</span></span><br/>  | <dl> <span data-ttu-id="bed7c-116"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bed7c-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bed7c-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="bed7c-117">Library</span></span><br/> | <dl> <span data-ttu-id="bed7c-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bed7c-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bed7c-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bed7c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bed7c-120">**Classe COARefTime**</span><span class="sxs-lookup"><span data-stu-id="bed7c-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




