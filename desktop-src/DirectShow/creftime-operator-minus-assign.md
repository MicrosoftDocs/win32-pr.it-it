---
description: L'operatore-= sottrae un'ora di riferimento da un'altra.
ms.assetid: 5b0ec72e-87d8-4562-96b1-40e4f5036fd4
title: Metodo CRefTime. Operator-= (Reftime. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator-=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bf66abe11d5c61edbb70118020d882c82b08847
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329048"
---
# <a name="creftimeoperator--method"></a><span data-ttu-id="95e8b-103">Metodo CRefTime. operator-=</span><span class="sxs-lookup"><span data-stu-id="95e8b-103">CRefTime.operator-= method</span></span>

<span data-ttu-id="95e8b-104">L'operatore-= sottrae un'ora di riferimento da un'altra.</span><span class="sxs-lookup"><span data-stu-id="95e8b-104">The -= operator subtracts one reference time from another.</span></span>

## <a name="syntax"></a><span data-ttu-id="95e8b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="95e8b-105">Syntax</span></span>


```C++
CRefTime& operator-=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="95e8b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="95e8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95e8b-107">*RT* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="95e8b-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="95e8b-108">Riferimento a un oggetto **CRefTime** .</span><span class="sxs-lookup"><span data-stu-id="95e8b-108">Reference to a **CRefTime** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95e8b-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="95e8b-109">Return value</span></span>

<span data-ttu-id="95e8b-110">Restituisce un riferimento all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="95e8b-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="95e8b-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95e8b-111">Requirements</span></span>



| <span data-ttu-id="95e8b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="95e8b-112">Requirement</span></span> | <span data-ttu-id="95e8b-113">Valore</span><span class="sxs-lookup"><span data-stu-id="95e8b-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95e8b-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="95e8b-114">Header</span></span><br/>  | <dl> <span data-ttu-id="95e8b-115"><dt>Reftime. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95e8b-115"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="95e8b-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="95e8b-116">Library</span></span><br/> | <dl> <span data-ttu-id="95e8b-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="95e8b-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




