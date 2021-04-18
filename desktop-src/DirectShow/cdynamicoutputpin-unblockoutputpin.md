---
description: Il metodo UnblockOutputPin Sblocca il PIN. Quando il PIN viene sbloccato, può fornire esempi, modificare il formato di output e riconnettersi.
ms.assetid: ea6e6312-8c7f-44db-ac7f-165dc45dec23
title: Metodo CDynamicOutputPin. UnblockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.UnblockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60bcde3ccad01e19f3802e2cd19f0f6b873380ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331645"
---
# <a name="cdynamicoutputpinunblockoutputpin-method"></a><span data-ttu-id="7ddf0-104">CDynamicOutputPin. UnblockOutputPin, metodo</span><span class="sxs-lookup"><span data-stu-id="7ddf0-104">CDynamicOutputPin.UnblockOutputPin method</span></span>

<span data-ttu-id="7ddf0-105">Il `UnblockOutputPin` metodo sblocca il PIN.</span><span class="sxs-lookup"><span data-stu-id="7ddf0-105">The `UnblockOutputPin` method unblocks the pin.</span></span> <span data-ttu-id="7ddf0-106">Quando il PIN viene sbloccato, può fornire esempi, modificare il formato di output e riconnettersi.</span><span class="sxs-lookup"><span data-stu-id="7ddf0-106">When the pin is unblocked, it can deliver samples, change its output format, and reconnect itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ddf0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ddf0-107">Syntax</span></span>


```C++
HRESULT UnblockOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="7ddf0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ddf0-108">Parameters</span></span>

<span data-ttu-id="7ddf0-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="7ddf0-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7ddf0-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ddf0-110">Return value</span></span>

<span data-ttu-id="7ddf0-111">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="7ddf0-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="7ddf0-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7ddf0-112">Return code</span></span>                                                                             | <span data-ttu-id="7ddf0-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ddf0-113">Description</span></span>                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="7ddf0-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="7ddf0-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="7ddf0-115">Il PIN è già stato sbloccato.</span><span class="sxs-lookup"><span data-stu-id="7ddf0-115">Pin was already unblocked.</span></span><br/> |
| <dl> <span data-ttu-id="7ddf0-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7ddf0-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="7ddf0-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="7ddf0-117">Success.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="7ddf0-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ddf0-118">Requirements</span></span>



| <span data-ttu-id="7ddf0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ddf0-119">Requirement</span></span> | <span data-ttu-id="7ddf0-120">Valore</span><span class="sxs-lookup"><span data-stu-id="7ddf0-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ddf0-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ddf0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7ddf0-122"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ddf0-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7ddf0-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="7ddf0-123">Library</span></span><br/> | <dl> <span data-ttu-id="7ddf0-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7ddf0-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ddf0-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ddf0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ddf0-126">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="7ddf0-126">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




