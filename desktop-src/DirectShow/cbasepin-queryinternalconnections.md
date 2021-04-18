---
description: "Il metodo QueryInternalConnections recupera i pin connessi internamente a questo pin (all'interno del filtro). Questo metodo implementa il metodo IPin:: QueryInternalConnections."
ms.assetid: 08344fc5-38b2-4dbe-8ef9-30d2fcd64187
title: Metodo CBasePin. QueryInternalConnections (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryInternalConnections
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99a636295fc87347a1735ab028b6de342e887d55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328261"
---
# <a name="cbasepinqueryinternalconnections-method"></a><span data-ttu-id="4002a-104">CBasePin. QueryInternalConnections, metodo</span><span class="sxs-lookup"><span data-stu-id="4002a-104">CBasePin.QueryInternalConnections method</span></span>

<span data-ttu-id="4002a-105">Il `QueryInternalConnections` metodo recupera i pin connessi internamente a questo pin (all'interno del filtro).</span><span class="sxs-lookup"><span data-stu-id="4002a-105">The `QueryInternalConnections` method retrieves the pins that are connected internally to this pin (within the filter).</span></span> <span data-ttu-id="4002a-106">Questo metodo implementa il metodo [**Ipin:: QueryInternalConnections**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) .</span><span class="sxs-lookup"><span data-stu-id="4002a-106">This method implements the [**IPin::QueryInternalConnections**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4002a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4002a-107">Syntax</span></span>


```C++
HRESULT QueryInternalConnections(
   IPin  *apPin,
   ULONG *nPin
);
```



## <a name="parameters"></a><span data-ttu-id="4002a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4002a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4002a-109">*apPin*</span><span class="sxs-lookup"><span data-stu-id="4002a-109">*apPin*</span></span> 
</dt> <dd>

<span data-ttu-id="4002a-110">Indirizzo di una matrice di puntatori [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="4002a-110">Address of an array of [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) pointers.</span></span>

</dd> <dt>

<span data-ttu-id="4002a-111">*nPin*</span><span class="sxs-lookup"><span data-stu-id="4002a-111">*nPin*</span></span> 
</dt> <dd>

<span data-ttu-id="4002a-112">In input, specifica la dimensione della matrice.</span><span class="sxs-lookup"><span data-stu-id="4002a-112">On input, specifies the size of the array.</span></span> <span data-ttu-id="4002a-113">Quando il metodo restituisce, il valore viene impostato sul numero di puntatori restituiti nella matrice.</span><span class="sxs-lookup"><span data-stu-id="4002a-113">When the method returns, the value is set to the number of pointers returned in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4002a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4002a-114">Return value</span></span>

<span data-ttu-id="4002a-115">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="4002a-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="4002a-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4002a-116">Return code</span></span>                                                                               | <span data-ttu-id="4002a-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4002a-117">Description</span></span>                         |
|-------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="4002a-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="4002a-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="4002a-119">Dimensioni della matrice insufficienti.</span><span class="sxs-lookup"><span data-stu-id="4002a-119">Insufficient array size.</span></span><br/> |
| <dl> <span data-ttu-id="4002a-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4002a-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="4002a-121">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4002a-121">Success.</span></span><br/>                 |
| <dl> <span data-ttu-id="4002a-122"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="4002a-122"><dt>**E\_FAIL**</dt></span></span> </dl>    | <span data-ttu-id="4002a-123">Esito negativo.</span><span class="sxs-lookup"><span data-stu-id="4002a-123">Failure.</span></span><br/>                 |
| <dl> <span data-ttu-id="4002a-124"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="4002a-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="4002a-125">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="4002a-125">Not implemented.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="4002a-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="4002a-126">Remarks</span></span>

<span data-ttu-id="4002a-127">In alcuni filtri i pin di input corrispondono a specifici pin di output.</span><span class="sxs-lookup"><span data-stu-id="4002a-127">On some filters, input pins correspond to particular output pins.</span></span> <span data-ttu-id="4002a-128">Per ogni pin, questo metodo riempie una matrice con puntatori ai pin corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="4002a-128">For each pin, this method fills an array with pointers to the corresponding pins.</span></span> <span data-ttu-id="4002a-129">Se ogni pin di input fornisce dati per ogni pin di output, restituire E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="4002a-129">If every input pin provides data for every output pin, return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="4002a-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4002a-130">Requirements</span></span>



| <span data-ttu-id="4002a-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4002a-131">Requirement</span></span> | <span data-ttu-id="4002a-132">Valore</span><span class="sxs-lookup"><span data-stu-id="4002a-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4002a-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4002a-133">Header</span></span><br/>  | <dl> <span data-ttu-id="4002a-134"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4002a-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4002a-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="4002a-135">Library</span></span><br/> | <dl> <span data-ttu-id="4002a-136"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4002a-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4002a-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4002a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4002a-138">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="4002a-138">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




