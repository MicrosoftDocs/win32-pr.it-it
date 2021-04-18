---
description: "Il metodo EndFlush termina un'operazione di svuotamento. Questo metodo implementa il metodo IPin:: EndFlush."
ms.assetid: c5c76cf8-1ca1-4fef-8776-7f4dcca32939
title: Metodo CBaseOutputPin. EndFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b40bc7db4e8d290ae0cd7e26a9d751e44b0daa4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332063"
---
# <a name="cbaseoutputpinendflush-method"></a><span data-ttu-id="85c6f-104">CBaseOutputPin. EndFlush, metodo</span><span class="sxs-lookup"><span data-stu-id="85c6f-104">CBaseOutputPin.EndFlush method</span></span>

<span data-ttu-id="85c6f-105">Il `EndFlush` metodo termina un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="85c6f-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="85c6f-106">Questo metodo implementa il metodo [**Ipin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="85c6f-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="85c6f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85c6f-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="85c6f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="85c6f-108">Parameters</span></span>

<span data-ttu-id="85c6f-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="85c6f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="85c6f-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="85c6f-110">Return value</span></span>

<span data-ttu-id="85c6f-111">Restituisce E \_ imprevisto.</span><span class="sxs-lookup"><span data-stu-id="85c6f-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="85c6f-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="85c6f-112">Remarks</span></span>

<span data-ttu-id="85c6f-113">Questo metodo deve essere chiamato solo sui pin di input, pertanto l'implementazione di **CBaseOutputPin** restituisce E \_ imprevisto.</span><span class="sxs-lookup"><span data-stu-id="85c6f-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="85c6f-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85c6f-114">Requirements</span></span>



| <span data-ttu-id="85c6f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="85c6f-115">Requirement</span></span> | <span data-ttu-id="85c6f-116">Valore</span><span class="sxs-lookup"><span data-stu-id="85c6f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85c6f-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="85c6f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="85c6f-118"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85c6f-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="85c6f-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="85c6f-119">Library</span></span><br/> | <dl> <span data-ttu-id="85c6f-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="85c6f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85c6f-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85c6f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85c6f-122">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="85c6f-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




