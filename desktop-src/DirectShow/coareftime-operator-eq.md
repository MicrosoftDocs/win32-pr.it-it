---
description: Questo operatore verifica l'uguaglianza tra due tempi di riferimento.
ms.assetid: a265f7c6-8334-4bb3-8cb7-c7918ebdf97a
title: Metodo COARefTime. Operator = = (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator==
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04b19f7b75be840a293920b36fe5ab63d30520d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333276"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="5b972-103">Metodo COARefTime. operator = =</span><span class="sxs-lookup"><span data-stu-id="5b972-103">COARefTime.operator== method</span></span>

<span data-ttu-id="5b972-104">Questo operatore verifica l'uguaglianza tra due tempi di riferimento.</span><span class="sxs-lookup"><span data-stu-id="5b972-104">This operator tests for equality between two reference times.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b972-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5b972-105">Syntax</span></span>


```C++
BOOL operator==(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="5b972-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5b972-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b972-107">*RT* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="5b972-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="5b972-108">Riferimento all'oggetto **COARefTime** da confrontare.</span><span class="sxs-lookup"><span data-stu-id="5b972-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b972-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5b972-109">Return value</span></span>

<span data-ttu-id="5b972-110">Restituisce **true** se i due oggetti sono uguali.</span><span class="sxs-lookup"><span data-stu-id="5b972-110">Returns **TRUE** if the two objects are equal.</span></span> <span data-ttu-id="5b972-111">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="5b972-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b972-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b972-112">Requirements</span></span>



| <span data-ttu-id="5b972-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b972-113">Requirement</span></span> | <span data-ttu-id="5b972-114">Valore</span><span class="sxs-lookup"><span data-stu-id="5b972-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b972-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b972-115">Header</span></span><br/>  | <dl> <span data-ttu-id="5b972-116"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b972-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5b972-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="5b972-117">Library</span></span><br/> | <dl> <span data-ttu-id="5b972-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5b972-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b972-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b972-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b972-120">**Classe COARefTime**</span><span class="sxs-lookup"><span data-stu-id="5b972-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




