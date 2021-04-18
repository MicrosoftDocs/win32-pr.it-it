---
description: 'Il metodo EndOfStream notifica al pin che non sono previsti dati aggiuntivi. Questo metodo implementa il metodo IPin:: EndOfStream.'
ms.assetid: 5c3b5f90-4194-4d65-9f1a-55edf327e3b3
title: Metodo CBaseOutputPin. EndOfStream (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e1cd903e811dbcd000ba202fc86c0fcb41bf221b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332234"
---
# <a name="cbaseoutputpinendofstream-method"></a><span data-ttu-id="789ec-104">CBaseOutputPin. EndOfStream, metodo</span><span class="sxs-lookup"><span data-stu-id="789ec-104">CBaseOutputPin.EndOfStream method</span></span>

<span data-ttu-id="789ec-105">Il `EndOfStream` metodo notifica al pin che non sono previsti dati aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="789ec-105">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="789ec-106">Questo metodo implementa il metodo [**Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .</span><span class="sxs-lookup"><span data-stu-id="789ec-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="789ec-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="789ec-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="789ec-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="789ec-108">Parameters</span></span>

<span data-ttu-id="789ec-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="789ec-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="789ec-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="789ec-110">Return value</span></span>

<span data-ttu-id="789ec-111">Restituisce E \_ imprevisto.</span><span class="sxs-lookup"><span data-stu-id="789ec-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="789ec-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="789ec-112">Remarks</span></span>

<span data-ttu-id="789ec-113">Questo metodo deve essere chiamato solo sui pin di input, pertanto l'implementazione di **CBaseOutputPin** restituisce E \_ imprevisto.</span><span class="sxs-lookup"><span data-stu-id="789ec-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="789ec-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="789ec-114">Requirements</span></span>



| <span data-ttu-id="789ec-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="789ec-115">Requirement</span></span> | <span data-ttu-id="789ec-116">Valore</span><span class="sxs-lookup"><span data-stu-id="789ec-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="789ec-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="789ec-117">Header</span></span><br/>  | <dl> <span data-ttu-id="789ec-118"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="789ec-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="789ec-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="789ec-119">Library</span></span><br/> | <dl> <span data-ttu-id="789ec-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="789ec-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="789ec-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="789ec-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="789ec-122">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="789ec-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




