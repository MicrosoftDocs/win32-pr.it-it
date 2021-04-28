---
description: 'Metodo CBasePin.GetMediaType: il metodo GetMediaType recupera un tipo di supporto preferito, in base al valore di indice.'
ms.assetid: 96f102b0-e2d1-49a1-84af-aa4622cae2a9
title: Metodo CBasePin.GetMediaType (Amfilter.h)
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
ms.openlocfilehash: 186f2eddbedf4eb0565a4ca66ff4ed7e5b080090
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099369"
---
# <a name="cbasepingetmediatype-method"></a><span data-ttu-id="e4c6b-103">Metodo CBasePin.GetMediaType</span><span class="sxs-lookup"><span data-stu-id="e4c6b-103">CBasePin.GetMediaType method</span></span>

<span data-ttu-id="e4c6b-104">Il `GetMediaType` metodo recupera un tipo di supporto preferito, in base al valore di indice.</span><span class="sxs-lookup"><span data-stu-id="e4c6b-104">The `GetMediaType` method retrieves a preferred media type, by index value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4c6b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4c6b-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="e4c6b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4c6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4c6b-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="e4c6b-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="e4c6b-108">Valore di indice in base zero.</span><span class="sxs-lookup"><span data-stu-id="e4c6b-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="e4c6b-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="e4c6b-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="e4c6b-110">Puntatore a un [**oggetto CMediaType**](cmediatype.md) che riceve il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="e4c6b-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4c6b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4c6b-111">Return value</span></span>

<span data-ttu-id="e4c6b-112">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="e4c6b-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e4c6b-113">I valori possibili includono quelli nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e4c6b-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="e4c6b-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e4c6b-114">Return code</span></span>                                                                                            | <span data-ttu-id="e4c6b-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4c6b-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e4c6b-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e4c6b-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="e4c6b-117">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="e4c6b-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="e4c6b-118"><dt>**VFW \_ S \_ NO \_ MORE \_ ITEMS**</dt></span><span class="sxs-lookup"><span data-stu-id="e4c6b-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="e4c6b-119">Indice non compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="e4c6b-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="e4c6b-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e4c6b-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="e4c6b-121">Indice minore di zero.</span><span class="sxs-lookup"><span data-stu-id="e4c6b-121">Index less than zero.</span></span><br/> |
| <dl> <span data-ttu-id="e4c6b-122"><dt>**E \_ IMPREVISTO**</dt></span><span class="sxs-lookup"><span data-stu-id="e4c6b-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="e4c6b-123">Errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="e4c6b-123">Unexpected error.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="e4c6b-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4c6b-124">Remarks</span></span>

<span data-ttu-id="e4c6b-125">Dall'elenco dei tipi di supporti preferiti, questo metodo restituisce il tipo con un valore di indice *iPosition*.</span><span class="sxs-lookup"><span data-stu-id="e4c6b-125">From the pin's list of preferred media types, this method returns the type with an index value of *iPosition*.</span></span> <span data-ttu-id="e4c6b-126">La [**classe CEnumMediaTypes**](cenummediatypes.md) chiama questo metodo per enumerare i tipi di supporti preferiti.</span><span class="sxs-lookup"><span data-stu-id="e4c6b-126">The [**CEnumMediaTypes**](cenummediatypes.md) class calls this method to enumerate preferred media types.</span></span>

<span data-ttu-id="e4c6b-127">La classe base restituisce E \_ UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="e4c6b-127">The base class returns E\_UNEXPECTED.</span></span> <span data-ttu-id="e4c6b-128">Eseguire l'override di questo metodo nella classe derivata.</span><span class="sxs-lookup"><span data-stu-id="e4c6b-128">Override this method in your derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4c6b-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4c6b-129">Requirements</span></span>



| <span data-ttu-id="e4c6b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4c6b-130">Requirement</span></span> | <span data-ttu-id="e4c6b-131">Valore</span><span class="sxs-lookup"><span data-stu-id="e4c6b-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4c6b-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e4c6b-132">Header</span></span><br/>  | <dl> <span data-ttu-id="e4c6b-133"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4c6b-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e4c6b-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="e4c6b-134">Library</span></span><br/> | <dl> <span data-ttu-id="e4c6b-135"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e4c6b-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4c6b-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4c6b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4c6b-137">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="e4c6b-137">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




