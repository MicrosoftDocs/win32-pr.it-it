---
description: 'Metodo CBaseOutputPin.EndOfStream: il metodo EndOfStream notifica al pin che non sono previsti dati aggiuntivi. Questo metodo implementa il metodo IPin::EndOfStream.'
ms.assetid: 5c3b5f90-4194-4d65-9f1a-55edf327e3b3
title: Metodo CBaseOutputPin.EndOfStream (Amfilter.h)
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
ms.openlocfilehash: c5f293b8026456618ad1196c491bce58cf481f07
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096149"
---
# <a name="cbaseoutputpinendofstream-method"></a><span data-ttu-id="5bdd6-104">Metodo CBaseOutputPin.EndOfStream</span><span class="sxs-lookup"><span data-stu-id="5bdd6-104">CBaseOutputPin.EndOfStream method</span></span>

<span data-ttu-id="5bdd6-105">Il `EndOfStream` metodo notifica al pin che non sono previsti dati aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="5bdd6-105">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="5bdd6-106">Questo metodo implementa il [**metodo IPin::EndOfStream.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)</span><span class="sxs-lookup"><span data-stu-id="5bdd6-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bdd6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5bdd6-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="5bdd6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5bdd6-108">Parameters</span></span>

<span data-ttu-id="5bdd6-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="5bdd6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5bdd6-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5bdd6-110">Return value</span></span>

<span data-ttu-id="5bdd6-111">Restituisce E \_ UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="5bdd6-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bdd6-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="5bdd6-112">Remarks</span></span>

<span data-ttu-id="5bdd6-113">Questo metodo deve essere chiamato solo sui pin di input, quindi l'implementazione **di CBaseOutputPin** restituisce E \_ UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="5bdd6-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bdd6-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5bdd6-114">Requirements</span></span>



| <span data-ttu-id="5bdd6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bdd6-115">Requirement</span></span> | <span data-ttu-id="5bdd6-116">Valore</span><span class="sxs-lookup"><span data-stu-id="5bdd6-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bdd6-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5bdd6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5bdd6-118"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="5bdd6-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5bdd6-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="5bdd6-119">Library</span></span><br/> | <dl> <span data-ttu-id="5bdd6-120"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5bdd6-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bdd6-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5bdd6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bdd6-122">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="5bdd6-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




