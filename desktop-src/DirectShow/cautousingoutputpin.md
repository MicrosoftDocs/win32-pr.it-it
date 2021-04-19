---
description: La classe CAutoUsingOutputPin ottiene e rilascia l'accesso a un oggetto CDynamicOutputPin.
ms.assetid: 4ded5d18-4b14-4574-ad1f-73b886a51fac
title: Classe CAutoUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b664267ce2ff0dbbeeba8bc74708c9c67e185ae4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331820"
---
# <a name="cautousingoutputpin-class"></a><span data-ttu-id="4271d-103">Classe CAutoUsingOutputPin</span><span class="sxs-lookup"><span data-stu-id="4271d-103">CAutoUsingOutputPin class</span></span>

<span data-ttu-id="4271d-104">La classe **CAutoUsingOutputPin** ottiene e rilascia l'accesso a un oggetto [**CDynamicOutputPin**](cdynamicoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="4271d-104">The **CAutoUsingOutputPin** class obtains and releases access to a [**CDynamicOutputPin**](cdynamicoutputpin.md) object.</span></span>

<span data-ttu-id="4271d-105">**CAutoUsingOutputPin** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4271d-105">**CAutoUsingOutputPin** has these types of members:</span></span>



| <span data-ttu-id="4271d-106">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="4271d-106">Public Methods</span></span>                                                           | <span data-ttu-id="4271d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4271d-107">Description</span></span>                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="4271d-108">**CAutoUsingOutputPin**</span><span class="sxs-lookup"><span data-stu-id="4271d-108">**CAutoUsingOutputPin**</span></span>](cautousingoutputpin-cautousingoutputpin.md)   | <span data-ttu-id="4271d-109">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="4271d-109">Constructor method.</span></span> <span data-ttu-id="4271d-110">Ottiene l'accesso al pin specificato.</span><span class="sxs-lookup"><span data-stu-id="4271d-110">Obtains access to the specified pin.</span></span> |
| [<span data-ttu-id="4271d-111">**~ CAutoUsingOutputPin**</span><span class="sxs-lookup"><span data-stu-id="4271d-111">**~CAutoUsingOutputPin**</span></span>](cautousingoutputpin--cautousingoutputpin.md) | <span data-ttu-id="4271d-112">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="4271d-112">Destructor method.</span></span> <span data-ttu-id="4271d-113">Ottiene l'accesso al pin specificato.</span><span class="sxs-lookup"><span data-stu-id="4271d-113">Obtains access to the specified pin.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="4271d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="4271d-114">Remarks</span></span>

<span data-ttu-id="4271d-115">Quando vengono chiamati determinati metodi su [**CDynamicOutputPin**](cdynamicoutputpin.md), il chiamante deve ottenere l'accesso al pin e quindi rilasciare tale accesso.</span><span class="sxs-lookup"><span data-stu-id="4271d-115">When certain methods are called on [**CDynamicOutputPin**](cdynamicoutputpin.md), the caller must obtain access to the pin and then release that access.</span></span> <span data-ttu-id="4271d-116">Per ottenere l'accesso, il chiamante usa il metodo [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="4271d-116">To obtain access, the caller uses the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method.</span></span> <span data-ttu-id="4271d-117">Per rilasciare l'accesso, viene chiamato il metodo [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="4271d-117">To release access, it calls the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method.</span></span> <span data-ttu-id="4271d-118">La classe **CAutoUsingOutputPin** è una classe helper che gestisce queste attività nei relativi metodi di costruttore e distruttore.</span><span class="sxs-lookup"><span data-stu-id="4271d-118">The **CAutoUsingOutputPin** class is a helper class that handles these tasks in its constructor and destructor methods.</span></span> <span data-ttu-id="4271d-119">Nell'esempio di codice seguente viene illustrato come utilizzare questa classe:</span><span class="sxs-lookup"><span data-stu-id="4271d-119">The following code example shows how to use this class:</span></span>


```
CDynamicOutputPin *pPin;
HRESULT hr = S_OK;  // Important! Initialize to S_OK.

// TODO: Obtain a pointer to the pin (not shown).

// Scope for lock.
{
    // Hold lock on pin.
    CAutoUsingOutputPin UsingPin(pPin, &hr)

    if (SUCCEEDED(hr)) 
    {

        // Safe to use the pin.
        hr = pPin->Deliver(pSample);

    }

} // Object goes out of scope here.

// No longer safe to use the pin.
```



## <a name="requirements"></a><span data-ttu-id="4271d-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4271d-120">Requirements</span></span>



| <span data-ttu-id="4271d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4271d-121">Requirement</span></span> | <span data-ttu-id="4271d-122">Valore</span><span class="sxs-lookup"><span data-stu-id="4271d-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4271d-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4271d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4271d-124"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4271d-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4271d-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="4271d-125">Library</span></span><br/> | <dl> <span data-ttu-id="4271d-126"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4271d-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4271d-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4271d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4271d-128">Riferimento alla classe di base</span><span class="sxs-lookup"><span data-stu-id="4271d-128">Base Class Reference</span></span>](base-class-reference.md)
</dt> </dl>

 

 




