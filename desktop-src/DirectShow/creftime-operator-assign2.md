---
description: L'operatore = assegna una nuova ora di riferimento. Questo metodo usa il parametro *ll* .
ms.assetid: 556c2e8a-4726-42ab-949d-9a028ebb1b95
title: Metodo CRefTime. Operator = (Reftime. h)-ll parametro
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d09cb957e06d8b075cff3d831a7f68fbbdf662a8
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334344"
---
# <a name="creftimeoperator-method-reftimeh---ll-parameter"></a><span data-ttu-id="252c6-104">Metodo CRefTime. Operator = (Reftime. h)-ll parametro</span><span class="sxs-lookup"><span data-stu-id="252c6-104">CRefTime.operator= method (Reftime.h) - ll parameter</span></span>

<span data-ttu-id="252c6-105">L'operatore = assegna una nuova ora di riferimento.</span><span class="sxs-lookup"><span data-stu-id="252c6-105">The = operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="252c6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="252c6-106">Syntax</span></span>


```C++
CRefTime& operator=(
   const LONGLONG ll
);
```



## <a name="parameters"></a><span data-ttu-id="252c6-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="252c6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="252c6-108">*ll*</span><span class="sxs-lookup"><span data-stu-id="252c6-108">*ll*</span></span> 
</dt> <dd>

<span data-ttu-id="252c6-109">Nuova ora di riferimento, in unità 100-nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="252c6-109">New reference time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="252c6-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="252c6-110">Return value</span></span>

<span data-ttu-id="252c6-111">Restituisce un riferimento all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="252c6-111">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="252c6-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="252c6-112">Requirements</span></span>



| <span data-ttu-id="252c6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="252c6-113">Requirement</span></span> | <span data-ttu-id="252c6-114">Valore</span><span class="sxs-lookup"><span data-stu-id="252c6-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="252c6-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="252c6-115">Header</span></span>  | <span data-ttu-id="252c6-116">Reftime. h (include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="252c6-116">Reftime.h (include Streams.h)</span></span>                                                                                   |
| <span data-ttu-id="252c6-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="252c6-117">Library</span></span> | <span data-ttu-id="252c6-118">Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug)</span><span class="sxs-lookup"><span data-stu-id="252c6-118">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |



 

 




