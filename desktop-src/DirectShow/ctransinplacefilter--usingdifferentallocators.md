---
description: Il metodo UsingDifferentAllocators determina se i pin di input e di output utilizzano allocatori diversi.
ms.assetid: 75feaa6e-6395-4d47-ae92-10a857f8764b
title: Metodo CTransInPlaceFilter. UsingDifferentAllocators (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.UsingDifferentAllocators
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f20802836adb665614e2bbfb8cb79bdccd5a36ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332984"
---
# <a name="ctransinplacefilterusingdifferentallocators-method"></a><span data-ttu-id="b61e8-103">CTransInPlaceFilter. UsingDifferentAllocators, metodo</span><span class="sxs-lookup"><span data-stu-id="b61e8-103">CTransInPlaceFilter.UsingDifferentAllocators method</span></span>

<span data-ttu-id="b61e8-104">Il `UsingDifferentAllocators` metodo determina se i pin di input e di output utilizzano allocatori diversi.</span><span class="sxs-lookup"><span data-stu-id="b61e8-104">The `UsingDifferentAllocators` method determines whether the input and output pins are using different allocators.</span></span>

## <a name="syntax"></a><span data-ttu-id="b61e8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b61e8-105">Syntax</span></span>


```C++
BOOL UsingDifferentAllocators() const;
```



## <a name="parameters"></a><span data-ttu-id="b61e8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b61e8-106">Parameters</span></span>

<span data-ttu-id="b61e8-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b61e8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b61e8-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b61e8-108">Return value</span></span>

<span data-ttu-id="b61e8-109">Restituisce **true** se i pin di input e di output utilizzano allocatori diversi. in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="b61e8-109">Returns **TRUE** if the input and output pins are using different allocators, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b61e8-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b61e8-110">Requirements</span></span>



| <span data-ttu-id="b61e8-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="b61e8-111">Requirement</span></span> | <span data-ttu-id="b61e8-112">Valore</span><span class="sxs-lookup"><span data-stu-id="b61e8-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b61e8-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b61e8-113">Header</span></span><br/>  | <dl> <span data-ttu-id="b61e8-114"><dt>Transip. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b61e8-114"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b61e8-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="b61e8-115">Library</span></span><br/> | <dl> <span data-ttu-id="b61e8-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b61e8-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b61e8-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b61e8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b61e8-118">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="b61e8-118">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




