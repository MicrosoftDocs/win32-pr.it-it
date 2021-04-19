---
description: Questo operatore verifica la disuguaglianza tra due tempi di riferimento.
ms.assetid: c081fff2-d85e-409a-8902-4b2aa2c1fc78
title: Metodo COARefTime. Operator! = (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator!=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e93934d7b31715422f2cc091e606b681a57e7f61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330291"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="7834e-103">Metodo COARefTime. operator! =</span><span class="sxs-lookup"><span data-stu-id="7834e-103">COARefTime.operator!= method</span></span>

<span data-ttu-id="7834e-104">Questo operatore verifica la disuguaglianza tra due tempi di riferimento.</span><span class="sxs-lookup"><span data-stu-id="7834e-104">This operator tests for inequality between two reference times.</span></span>

## <a name="syntax"></a><span data-ttu-id="7834e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7834e-105">Syntax</span></span>


```C++
BOOL operator!=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="7834e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7834e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7834e-107">*RT* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="7834e-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="7834e-108">Riferimento all'oggetto **COARefTime** da confrontare.</span><span class="sxs-lookup"><span data-stu-id="7834e-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7834e-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7834e-109">Return value</span></span>

<span data-ttu-id="7834e-110">Restituisce **true** se i due oggetti non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="7834e-110">Returns **TRUE** if the two objects are not equal.</span></span> <span data-ttu-id="7834e-111">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="7834e-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7834e-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7834e-112">Requirements</span></span>



| <span data-ttu-id="7834e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7834e-113">Requirement</span></span> | <span data-ttu-id="7834e-114">Valore</span><span class="sxs-lookup"><span data-stu-id="7834e-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7834e-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7834e-115">Header</span></span><br/>  | <dl> <span data-ttu-id="7834e-116"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7834e-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7834e-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="7834e-117">Library</span></span><br/> | <dl> <span data-ttu-id="7834e-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7834e-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7834e-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7834e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7834e-120">**Classe COARefTime**</span><span class="sxs-lookup"><span data-stu-id="7834e-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




