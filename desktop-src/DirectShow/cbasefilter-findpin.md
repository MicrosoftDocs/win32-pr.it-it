---
description: "Metodo CBaseFilter.FindPin: il metodo FindPin recupera il segnaposto con l'identificatore specificato. Questo metodo implementa il metodo IBaseFilter::FindPin."
ms.assetid: 152e4ff3-2809-4c57-b9c8-f51fc50b3703
title: Metodo CBaseFilter.FindPin (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2bbef9b051a42597b2585a432f544eead4e2e0a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099819"
---
# <a name="cbasefilterfindpin-method"></a><span data-ttu-id="fd416-104">Metodo CBaseFilter.FindPin</span><span class="sxs-lookup"><span data-stu-id="fd416-104">CBaseFilter.FindPin method</span></span>

<span data-ttu-id="fd416-105">Il `FindPin` metodo recupera il pin con l'identificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="fd416-105">The `FindPin` method retrieves the pin with the specified identifier.</span></span> <span data-ttu-id="fd416-106">Questo metodo implementa il [**metodo IBaseFilter::FindPin.**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin)</span><span class="sxs-lookup"><span data-stu-id="fd416-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd416-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd416-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="fd416-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fd416-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd416-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="fd416-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="fd416-110">Puntatore a una stringa Unicode con terminazione Null costante che identifica il segnaposto.</span><span class="sxs-lookup"><span data-stu-id="fd416-110">Pointer to a constant, null-terminated Unicode string that identifies the pin.</span></span>

</dd> <dt>

<span data-ttu-id="fd416-111">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="fd416-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="fd416-112">Indirizzo di una variabile che riceve un puntatore [**all'interfaccia IPin del**](/windows/desktop/api/Strmif/nn-strmif-ipin) pin.</span><span class="sxs-lookup"><span data-stu-id="fd416-112">Address of a variable that receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd416-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fd416-113">Return value</span></span>

<span data-ttu-id="fd416-114">Restituisce uno dei valori **HRESULT** seguenti.</span><span class="sxs-lookup"><span data-stu-id="fd416-114">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="fd416-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="fd416-115">Return code</span></span>                                                                                       | <span data-ttu-id="fd416-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd416-116">Description</span></span>                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="fd416-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fd416-117"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="fd416-118">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="fd416-118">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="fd416-119"><dt>**PUNTATORE \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="fd416-119"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="fd416-120">Argomento del puntatore **NULL.**</span><span class="sxs-lookup"><span data-stu-id="fd416-120">**NULL** pointer argument.</span></span><br/>     |
| <dl> <span data-ttu-id="fd416-121"><dt>**VFW \_ E \_ NON \_ TROVATO**</dt></span><span class="sxs-lookup"><span data-stu-id="fd416-121"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="fd416-122">Impossibile trovare un segnaposto corrispondente.</span><span class="sxs-lookup"><span data-stu-id="fd416-122">Could not find a matching pin.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fd416-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd416-123">Remarks</span></span>

<span data-ttu-id="fd416-124">Questo metodo chiama il [**metodo CBasePin::Name**](cbasepin-name.md) per confrontare il nome di ogni segnaposto con la stringa specificata dal *parametro Id.*</span><span class="sxs-lookup"><span data-stu-id="fd416-124">This method calls the [**CBasePin::Name**](cbasepin-name.md) method to compare each pin's name against the string specified by the *Id* parameter.</span></span>

<span data-ttu-id="fd416-125">Se il metodo ha esito positivo, **l'interfaccia IPin** ha un conteggio dei riferimenti in sospeso.</span><span class="sxs-lookup"><span data-stu-id="fd416-125">If the method succeeds, the **IPin** interface has an outstanding reference count.</span></span> <span data-ttu-id="fd416-126">Al termine, assicurarsi di rilasciarlo.</span><span class="sxs-lookup"><span data-stu-id="fd416-126">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd416-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd416-127">Requirements</span></span>



| <span data-ttu-id="fd416-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd416-128">Requirement</span></span> | <span data-ttu-id="fd416-129">Valore</span><span class="sxs-lookup"><span data-stu-id="fd416-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd416-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fd416-130">Header</span></span><br/>  | <dl> <span data-ttu-id="fd416-131"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="fd416-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fd416-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="fd416-132">Library</span></span><br/> | <dl> <span data-ttu-id="fd416-133"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="fd416-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd416-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd416-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd416-135">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="fd416-135">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




