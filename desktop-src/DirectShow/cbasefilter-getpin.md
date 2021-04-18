---
description: Il metodo GetPin recupera un PIN. La classe CEnumPins chiama questo metodo per enumerare i pin sul filtro.
ms.assetid: e3ec3f11-1e7d-40b6-810e-3759f0511cb2
title: Metodo CBaseFilter. GetPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bb8341bfd86b96a7358fb23036b71844f77d17a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328947"
---
# <a name="cbasefiltergetpin-method"></a><span data-ttu-id="3e88d-104">CBaseFilter. GetPin, metodo</span><span class="sxs-lookup"><span data-stu-id="3e88d-104">CBaseFilter.GetPin method</span></span>

<span data-ttu-id="3e88d-105">Il metodo **GetPin** recupera un PIN.</span><span class="sxs-lookup"><span data-stu-id="3e88d-105">The **GetPin** method retrieves a pin.</span></span> <span data-ttu-id="3e88d-106">La classe [**CEnumPins**](cenumpins.md) chiama questo metodo per enumerare i pin sul filtro.</span><span class="sxs-lookup"><span data-stu-id="3e88d-106">The [**CEnumPins**](cenumpins.md) class calls this method to enumerate pins on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e88d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e88d-107">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="3e88d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e88d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e88d-109">*n*</span><span class="sxs-lookup"><span data-stu-id="3e88d-109">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="3e88d-110">Indice in base zero del PIN.</span><span class="sxs-lookup"><span data-stu-id="3e88d-110">The zero-based index of the pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e88d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e88d-111">Return value</span></span>

<span data-ttu-id="3e88d-112">Restituisce un puntatore all'oggetto [**CBasePin**](cbasepin.md) che implementa il PIN.</span><span class="sxs-lookup"><span data-stu-id="3e88d-112">Returns a pointer to the [**CBasePin**](cbasepin.md) object that implements the pin.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e88d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e88d-113">Remarks</span></span>

<span data-ttu-id="3e88d-114">È necessario implementare questo metodo virtuale puro nella classe derivata.</span><span class="sxs-lookup"><span data-stu-id="3e88d-114">You must implement this pure virtual method in your derived class.</span></span> <span data-ttu-id="3e88d-115">Restituisce un puntatore al pin *n* sul filtro, indicizzato da zero.</span><span class="sxs-lookup"><span data-stu-id="3e88d-115">Return a pointer to the *n* th pin on this filter, indexed from zero.</span></span> <span data-ttu-id="3e88d-116">È possibile scegliere un ordine di indicizzazione arbitrario, purché l'ordinamento sia corretto.</span><span class="sxs-lookup"><span data-stu-id="3e88d-116">You can choose an arbitrary indexing order, as long as the ordering is fixed.</span></span> <span data-ttu-id="3e88d-117">Se il filtro aggiunge o Elimina pin o le modifiche di ordinamento per altri motivi in fase di esecuzione, chiamare il metodo [**CBaseFilter:: IncrementPinVersion**](cbasefilter-incrementpinversion.md) .</span><span class="sxs-lookup"><span data-stu-id="3e88d-117">If the filter adds or deletes pins, or the ordering changes for some other reason at run time, call the [**CBaseFilter::IncrementPinVersion**](cbasefilter-incrementpinversion.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e88d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e88d-118">Requirements</span></span>



| <span data-ttu-id="3e88d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e88d-119">Requirement</span></span> | <span data-ttu-id="3e88d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3e88d-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e88d-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e88d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3e88d-122"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e88d-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3e88d-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="3e88d-123">Library</span></span><br/> | <dl> <span data-ttu-id="3e88d-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3e88d-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e88d-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e88d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e88d-126">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="3e88d-126">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




