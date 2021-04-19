---
description: Il metodo GetMediaType recupera un tipo di supporto preferito, in base al valore di indice.
ms.assetid: 96f102b0-e2d1-49a1-84af-aa4622cae2a9
title: Metodo CBasePin. GetMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c54c5cd769a8efa0c720c7050cca45b00b8209e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333605"
---
# <a name="cbasepingetmediatype-method"></a><span data-ttu-id="1f447-103">CBasePin. GetMediaType, metodo</span><span class="sxs-lookup"><span data-stu-id="1f447-103">CBasePin.GetMediaType method</span></span>

<span data-ttu-id="1f447-104">Il `GetMediaType` metodo recupera un tipo di supporto preferito, in base al valore di indice.</span><span class="sxs-lookup"><span data-stu-id="1f447-104">The `GetMediaType` method retrieves a preferred media type, by index value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f447-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1f447-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="1f447-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1f447-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f447-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="1f447-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="1f447-108">Valore di indice in base zero.</span><span class="sxs-lookup"><span data-stu-id="1f447-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="1f447-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="1f447-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="1f447-110">Puntatore a un oggetto [**CMediaType**](cmediatype.md) che riceve il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="1f447-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f447-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1f447-111">Return value</span></span>

<span data-ttu-id="1f447-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1f447-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1f447-113">I valori possibili includono quelli nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="1f447-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="1f447-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="1f447-114">Return code</span></span>                                                                                            | <span data-ttu-id="1f447-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f447-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="1f447-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1f447-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="1f447-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="1f447-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="1f447-118"><dt>**\_non ci \_ sono \_ altri \_ elementi di VFW**</dt></span><span class="sxs-lookup"><span data-stu-id="1f447-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="1f447-119">Indice non compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="1f447-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="1f447-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1f447-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="1f447-121">Indice minore di zero.</span><span class="sxs-lookup"><span data-stu-id="1f447-121">Index less than zero.</span></span><br/> |
| <dl> <span data-ttu-id="1f447-122"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="1f447-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="1f447-123">Errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="1f447-123">Unexpected error.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="1f447-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="1f447-124">Remarks</span></span>

<span data-ttu-id="1f447-125">Dall'elenco dei tipi di supporto preferiti del PIN, questo metodo restituisce il tipo con un valore di indice *iPosition*.</span><span class="sxs-lookup"><span data-stu-id="1f447-125">From the pin's list of preferred media types, this method returns the type with an index value of *iPosition*.</span></span> <span data-ttu-id="1f447-126">La classe [**CEnumMediaTypes**](cenummediatypes.md) chiama questo metodo per enumerare i tipi di supporto preferiti.</span><span class="sxs-lookup"><span data-stu-id="1f447-126">The [**CEnumMediaTypes**](cenummediatypes.md) class calls this method to enumerate preferred media types.</span></span>

<span data-ttu-id="1f447-127">La classe base restituisce E \_ imprevisto.</span><span class="sxs-lookup"><span data-stu-id="1f447-127">The base class returns E\_UNEXPECTED.</span></span> <span data-ttu-id="1f447-128">Eseguire l'override di questo metodo nella classe derivata.</span><span class="sxs-lookup"><span data-stu-id="1f447-128">Override this method in your derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f447-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f447-129">Requirements</span></span>



| <span data-ttu-id="1f447-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f447-130">Requirement</span></span> | <span data-ttu-id="1f447-131">Valore</span><span class="sxs-lookup"><span data-stu-id="1f447-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f447-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1f447-132">Header</span></span><br/>  | <dl> <span data-ttu-id="1f447-133"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1f447-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1f447-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="1f447-134">Library</span></span><br/> | <dl> <span data-ttu-id="1f447-135"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1f447-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f447-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f447-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f447-137">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="1f447-137">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




