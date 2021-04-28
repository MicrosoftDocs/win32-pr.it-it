---
description: "Metodo CBaseOutputPin.EndFlush: il metodo EndFlush termina un'operazione di scaricamento. Questo metodo implementa il metodo IPin::EndFlush."
ms.assetid: c5c76cf8-1ca1-4fef-8776-7f4dcca32939
title: Metodo CBaseOutputPin.EndFlush (Amfilter.h)
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
ms.openlocfilehash: 53153c6dbd941390c7ef616ee36c56e01214c341
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099509"
---
# <a name="cbaseoutputpinendflush-method"></a><span data-ttu-id="fe0c8-104">Metodo CBaseOutputPin.EndFlush</span><span class="sxs-lookup"><span data-stu-id="fe0c8-104">CBaseOutputPin.EndFlush method</span></span>

<span data-ttu-id="fe0c8-105">Il `EndFlush` metodo termina un'operazione di scaricamento.</span><span class="sxs-lookup"><span data-stu-id="fe0c8-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="fe0c8-106">Questo metodo implementa il [**metodo IPin::EndFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)</span><span class="sxs-lookup"><span data-stu-id="fe0c8-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe0c8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe0c8-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="fe0c8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe0c8-108">Parameters</span></span>

<span data-ttu-id="fe0c8-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="fe0c8-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fe0c8-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe0c8-110">Return value</span></span>

<span data-ttu-id="fe0c8-111">Restituisce E \_ UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="fe0c8-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe0c8-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe0c8-112">Remarks</span></span>

<span data-ttu-id="fe0c8-113">Questo metodo deve essere chiamato solo sui pin di input, quindi **l'implementazione di CBaseOutputPin** restituisce E \_ UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="fe0c8-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe0c8-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe0c8-114">Requirements</span></span>



| <span data-ttu-id="fe0c8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe0c8-115">Requirement</span></span> | <span data-ttu-id="fe0c8-116">Valore</span><span class="sxs-lookup"><span data-stu-id="fe0c8-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe0c8-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe0c8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="fe0c8-118"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe0c8-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fe0c8-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="fe0c8-119">Library</span></span><br/> | <dl> <span data-ttu-id="fe0c8-120"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="fe0c8-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe0c8-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe0c8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe0c8-122">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="fe0c8-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




