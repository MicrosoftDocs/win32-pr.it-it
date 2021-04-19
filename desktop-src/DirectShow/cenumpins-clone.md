---
description: "Il metodo Clone crea una copia dell'enumeratore con lo stesso stato di enumerazione. Questo metodo implementa il metodo IEnumPins:: clone."
ms.assetid: 6e44c970-b90a-4bdb-8c60-dd8f31516249
title: Metodo CEnumPins. Clone (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Clone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2aa3e4604b260779a5d203e75e8e0790a7378b11
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329838"
---
# <a name="cenumpinsclone-method"></a><span data-ttu-id="ccf04-104">Metodo CEnumPins. Clone</span><span class="sxs-lookup"><span data-stu-id="ccf04-104">CEnumPins.Clone method</span></span>

<span data-ttu-id="ccf04-105">Il `Clone` metodo crea una copia dell'enumeratore con lo stesso stato di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="ccf04-105">The `Clone` method makes a copy of the enumerator with the same enumeration state.</span></span> <span data-ttu-id="ccf04-106">Questo metodo implementa il metodo [**IEnumPins:: Clone**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-clone) .</span><span class="sxs-lookup"><span data-stu-id="ccf04-106">This method implements the [**IEnumPins::Clone**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-clone) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccf04-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ccf04-107">Syntax</span></span>


```C++
HRESULT Clone(
   IEnumPins **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="ccf04-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ccf04-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccf04-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="ccf04-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="ccf04-110">Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) del nuovo enumeratore.</span><span class="sxs-lookup"><span data-stu-id="ccf04-110">Address of a variable that receives a pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface of the new enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccf04-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ccf04-111">Return value</span></span>

<span data-ttu-id="ccf04-112">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ccf04-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="ccf04-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ccf04-113">Return code</span></span>                                                                                                | <span data-ttu-id="ccf04-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ccf04-114">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ccf04-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ccf04-115"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="ccf04-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ccf04-116">Success.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="ccf04-117"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="ccf04-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>              | <span data-ttu-id="ccf04-118">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="ccf04-118">Insufficient memory.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="ccf04-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="ccf04-119"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="ccf04-120">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="ccf04-120">**NULL** pointer argument.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="ccf04-121"><dt>**non \_ \_ \_ \_ sincronizzato con VFW E enum \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ccf04-121"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="ccf04-122">Lo stato del filtro è stato modificato ed è ora incoerente con l'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="ccf04-122">The filter's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ccf04-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ccf04-123">Requirements</span></span>



| <span data-ttu-id="ccf04-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccf04-124">Requirement</span></span> | <span data-ttu-id="ccf04-125">Valore</span><span class="sxs-lookup"><span data-stu-id="ccf04-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccf04-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ccf04-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ccf04-127"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ccf04-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ccf04-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="ccf04-128">Library</span></span><br/> | <dl> <span data-ttu-id="ccf04-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ccf04-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccf04-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ccf04-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccf04-131">**Classe CEnumPins**</span><span class="sxs-lookup"><span data-stu-id="ccf04-131">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




