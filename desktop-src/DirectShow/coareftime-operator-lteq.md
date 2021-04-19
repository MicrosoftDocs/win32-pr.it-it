---
description: Questo operatore verifica se un'ora di riferimento è maggiore o uguale a un'altra.
ms.assetid: 1182db5b-2d58-4abb-b9ec-f14c3de5a942
title: Metodo COARefTime. operator<= (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator<=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b4d7c8f212f175760473e5cfe2fdcbd85c4f89f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330302"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="586ef-103">Metodo COARefTime. operator<=</span><span class="sxs-lookup"><span data-stu-id="586ef-103">COARefTime.operator<= method</span></span>

<span data-ttu-id="586ef-104">Questo operatore verifica se un'ora di riferimento è maggiore o uguale a un'altra.</span><span class="sxs-lookup"><span data-stu-id="586ef-104">This operator tests if one reference time is greater than or equal to another.</span></span>

## <a name="syntax"></a><span data-ttu-id="586ef-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="586ef-105">Syntax</span></span>


```C++
BOOL operator<=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="586ef-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="586ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="586ef-107">*RT* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="586ef-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="586ef-108">Riferimento all'oggetto **COARefTime** da confrontare.</span><span class="sxs-lookup"><span data-stu-id="586ef-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="586ef-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="586ef-109">Return value</span></span>

<span data-ttu-id="586ef-110">Restituisce **true** se l'oggetto è maggiore o uguale a *RT*.</span><span class="sxs-lookup"><span data-stu-id="586ef-110">Returns **TRUE** if this object is greater than or equal to *rt*.</span></span> <span data-ttu-id="586ef-111">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="586ef-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="586ef-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="586ef-112">Requirements</span></span>



| <span data-ttu-id="586ef-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="586ef-113">Requirement</span></span> | <span data-ttu-id="586ef-114">Valore</span><span class="sxs-lookup"><span data-stu-id="586ef-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="586ef-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="586ef-115">Header</span></span><br/>  | <dl> <span data-ttu-id="586ef-116"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="586ef-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="586ef-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="586ef-117">Library</span></span><br/> | <dl> <span data-ttu-id="586ef-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="586ef-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="586ef-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="586ef-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="586ef-120">**Classe COARefTime**</span><span class="sxs-lookup"><span data-stu-id="586ef-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




