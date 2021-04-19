---
description: "Il metodo Clone crea una copia dell'enumeratore con lo stesso stato di enumerazione. Questo metodo implementa il metodo IEnumMediaTypes:: clone."
ms.assetid: 3b4eb29e-48fc-4f00-a5f3-597b9aa94ce1
title: Metodo CEnumMediaTypes. Clone (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Clone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43f051bf90afa231d3b677045468f26d06d55150
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329853"
---
# <a name="cenummediatypesclone-method"></a><span data-ttu-id="d1d27-104">Metodo CEnumMediaTypes. Clone</span><span class="sxs-lookup"><span data-stu-id="d1d27-104">CEnumMediaTypes.Clone method</span></span>

<span data-ttu-id="d1d27-105">Il `Clone` metodo crea una copia dell'enumeratore con lo stesso stato di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="d1d27-105">The `Clone` method makes a copy of the enumerator with the same enumeration state.</span></span> <span data-ttu-id="d1d27-106">Questo metodo implementa il metodo [**IEnumMediaTypes:: Clone**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-clone) .</span><span class="sxs-lookup"><span data-stu-id="d1d27-106">This method implements the [**IEnumMediaTypes::Clone**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-clone) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1d27-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d1d27-107">Syntax</span></span>


```C++
HRESULT Clone(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="d1d27-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d1d27-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1d27-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="d1d27-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="d1d27-110">Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) del nuovo enumeratore.</span><span class="sxs-lookup"><span data-stu-id="d1d27-110">Address of a variable that receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface of the new enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1d27-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d1d27-111">Return value</span></span>

<span data-ttu-id="d1d27-112">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d1d27-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="d1d27-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d1d27-113">Return code</span></span>                                                                                                | <span data-ttu-id="d1d27-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1d27-114">Description</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d1d27-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d1d27-115"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="d1d27-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="d1d27-116">Success.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="d1d27-117"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="d1d27-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>              | <span data-ttu-id="d1d27-118">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="d1d27-118">Insufficient memory.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="d1d27-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="d1d27-119"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="d1d27-120">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="d1d27-120">**NULL** pointer argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="d1d27-121"><dt>**non \_ \_ \_ \_ sincronizzato con VFW E enum \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d1d27-121"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="d1d27-122">Lo stato del PIN è stato modificato ed è ora incoerente con l'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="d1d27-122">The pin's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d1d27-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1d27-123">Requirements</span></span>



| <span data-ttu-id="d1d27-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1d27-124">Requirement</span></span> | <span data-ttu-id="d1d27-125">Valore</span><span class="sxs-lookup"><span data-stu-id="d1d27-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1d27-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d1d27-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d1d27-127"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1d27-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d1d27-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="d1d27-128">Library</span></span><br/> | <dl> <span data-ttu-id="d1d27-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d1d27-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1d27-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1d27-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1d27-131">**Classe CEnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="d1d27-131">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




