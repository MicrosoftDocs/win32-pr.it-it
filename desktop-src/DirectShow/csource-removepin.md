---
description: Il metodo RemovePin rimuove dal filtro un PIN specificato. Il metodo non elimina il PIN.
ms.assetid: 104eccfa-3fff-4f47-ba1b-3206eab9eef8
title: Metodo CSource. RemovePin (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.RemovePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b71ced14a6f92a3056ac4f42e55bc3858c578ff6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332208"
---
# <a name="csourceremovepin-method"></a><span data-ttu-id="7b0a6-104">CSource. RemovePin, metodo</span><span class="sxs-lookup"><span data-stu-id="7b0a6-104">CSource.RemovePin method</span></span>

<span data-ttu-id="7b0a6-105">Il `RemovePin` metodo rimuove un PIN specificato dal filtro.</span><span class="sxs-lookup"><span data-stu-id="7b0a6-105">The `RemovePin` method removes a specified pin from the filter.</span></span> <span data-ttu-id="7b0a6-106">Il metodo non elimina il PIN.</span><span class="sxs-lookup"><span data-stu-id="7b0a6-106">The method does not delete the pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b0a6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b0a6-107">Syntax</span></span>


```C++
HRESULT RemovePin(
   CSourceStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="7b0a6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b0a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b0a6-109">*pStream*</span><span class="sxs-lookup"><span data-stu-id="7b0a6-109">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="7b0a6-110">Puntatore all'oggetto [**CSourceStream**](csourcestream.md) che implementa il PIN.</span><span class="sxs-lookup"><span data-stu-id="7b0a6-110">Pointer to the [**CSourceStream**](csourcestream.md) object that implements the pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b0a6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b0a6-111">Return value</span></span>

<span data-ttu-id="7b0a6-112">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="7b0a6-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="7b0a6-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7b0a6-113">Return code</span></span>                                                                             | <span data-ttu-id="7b0a6-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b0a6-114">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="7b0a6-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7b0a6-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="7b0a6-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="7b0a6-116">Success.</span></span><br/>                              |
| <dl> <span data-ttu-id="7b0a6-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="7b0a6-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="7b0a6-118">Il filtro non contiene questo pin.</span><span class="sxs-lookup"><span data-stu-id="7b0a6-118">The filter does not contain this pin.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7b0a6-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b0a6-119">Remarks</span></span>

<span data-ttu-id="7b0a6-120">Il metodo del distruttore chiama questo metodo per rimuovere il pin di output dal filtro.</span><span class="sxs-lookup"><span data-stu-id="7b0a6-120">The destructor method calls this method, to remove the output pin from the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b0a6-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b0a6-121">Requirements</span></span>



| <span data-ttu-id="7b0a6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b0a6-122">Requirement</span></span> | <span data-ttu-id="7b0a6-123">Valore</span><span class="sxs-lookup"><span data-stu-id="7b0a6-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b0a6-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7b0a6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7b0a6-125"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7b0a6-125"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7b0a6-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="7b0a6-126">Library</span></span><br/> | <dl> <span data-ttu-id="7b0a6-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7b0a6-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b0a6-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b0a6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b0a6-129">**Classe CSource**</span><span class="sxs-lookup"><span data-stu-id="7b0a6-129">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




