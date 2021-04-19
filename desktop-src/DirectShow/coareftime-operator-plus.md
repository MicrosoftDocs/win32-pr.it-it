---
description: Questo operatore aggiunge due tempi di riferimento.
ms.assetid: 4dfc087a-ec4f-4a8a-8bd4-4da9e1699bcd
title: Metodo COARefTime. Operator + (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator+
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a6f5019c61d4c1baec47652db8842aa5085b675
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330289"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="bf22c-103">Metodo COARefTime. operator +</span><span class="sxs-lookup"><span data-stu-id="bf22c-103">COARefTime.operator+ method</span></span>

<span data-ttu-id="bf22c-104">Questo operatore aggiunge due tempi di riferimento.</span><span class="sxs-lookup"><span data-stu-id="bf22c-104">This operator adds two reference times.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf22c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf22c-105">Syntax</span></span>


```C++
COARefTime operator+(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="bf22c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf22c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf22c-107">*RT* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="bf22c-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="bf22c-108">Riferimento all'oggetto **COARefTime** da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="bf22c-108">Reference to the **COARefTime** object to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf22c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf22c-109">Return value</span></span>

<span data-ttu-id="bf22c-110">Restituisce un nuovo oggetto **COARefTime** uguale alla somma dei tempi di riferimento.</span><span class="sxs-lookup"><span data-stu-id="bf22c-110">Returns a new **COARefTime** object equal to the sum of the reference times.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf22c-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf22c-111">Requirements</span></span>



| <span data-ttu-id="bf22c-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf22c-112">Requirement</span></span> | <span data-ttu-id="bf22c-113">Valore</span><span class="sxs-lookup"><span data-stu-id="bf22c-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf22c-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf22c-114">Header</span></span><br/>  | <dl> <span data-ttu-id="bf22c-115"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf22c-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bf22c-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="bf22c-116">Library</span></span><br/> | <dl> <span data-ttu-id="bf22c-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bf22c-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf22c-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf22c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf22c-119">**Classe COARefTime**</span><span class="sxs-lookup"><span data-stu-id="bf22c-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




