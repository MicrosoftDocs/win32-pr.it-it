---
description: L'operatore assegna una nuova ora di riferimento e usa il parametro ' RT [Ref]'.
ms.assetid: e3a005c0-95d5-41e0-80bb-e70399a50dca
title: COARefTime. operator = Method (Ctlutil. h)-RT [Ref] parametro
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bad1e0d7ee63fe9bcfa7fc1664a7349e787d9927
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2021
ms.locfileid: "106323818"
---
# <a name="coareftimeoperator-method-ctlutilh---rt-ref-parameter"></a><span data-ttu-id="35fcc-103">COARefTime. operator = Method (Ctlutil. h)-RT [Ref] parametro</span><span class="sxs-lookup"><span data-stu-id="35fcc-103">COARefTime.operator= method (Ctlutil.h) - rt [ref] parameter</span></span>

<span data-ttu-id="35fcc-104">Questo operatore assegna una nuova ora di riferimento.</span><span class="sxs-lookup"><span data-stu-id="35fcc-104">This operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="35fcc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35fcc-105">Syntax</span></span>


```C++
COARefTime& operator=(
  [ref] const REFERENCE_TIME &rt
);
```



## <a name="parameters"></a><span data-ttu-id="35fcc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="35fcc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35fcc-107">*RT* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="35fcc-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="35fcc-108">Riferimento a un valore di [**\_ ora di riferimento**](reference-time.md) che specifica la nuova ora di riferimento in unità 100-nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="35fcc-108">Reference to a [**REFERENCE\_TIME**](reference-time.md) value that specifies the new reference time in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35fcc-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35fcc-109">Return value</span></span>

<span data-ttu-id="35fcc-110">Restituisce un riferimento all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="35fcc-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="35fcc-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35fcc-111">Requirements</span></span>

| <span data-ttu-id="35fcc-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="35fcc-112">Requirement</span></span>                    | <span data-ttu-id="35fcc-113">Valore</span><span class="sxs-lookup"><span data-stu-id="35fcc-113">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35fcc-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="35fcc-114">Header</span></span>  | <span data-ttu-id="35fcc-115">Ctlutil. h (include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="35fcc-115">Ctlutil.h (include Streams.h)</span></span>                                                                                   |
| <span data-ttu-id="35fcc-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="35fcc-116">Library</span></span> | <span data-ttu-id="35fcc-117">Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug)</span><span class="sxs-lookup"><span data-stu-id="35fcc-117">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="35fcc-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35fcc-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35fcc-119">**Classe COARefTime**</span><span class="sxs-lookup"><span data-stu-id="35fcc-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




