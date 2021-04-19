---
description: Il metodo Invoke fornisce l'accesso alle proprietà e ai metodi esposti dall'oggetto.
ms.assetid: 3c03751d-239b-4cc5-bfab-8d1aed1074b8
title: Metodo CMediaPosition. Invoke (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3955848bf2a87e0983ddd7dc3bef48f157ae6648
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332330"
---
# <a name="cmediapositioninvoke-method"></a><span data-ttu-id="18a2a-103">Metodo CMediaPosition. Invoke</span><span class="sxs-lookup"><span data-stu-id="18a2a-103">CMediaPosition.Invoke method</span></span>

<span data-ttu-id="18a2a-104">Il `Invoke` metodo fornisce l'accesso alle proprietà e ai metodi esposti dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="18a2a-104">The `Invoke` method provides access to properties and methods exposed by the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="18a2a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="18a2a-105">Syntax</span></span>


```C++
HRESULT Invoke(
   DISPID     dispidMember,
   REFIID     riid,
   LCID       lcid,
   WORD       wFlags,
   DISPPARAMS *pdispparams,
   VARIANT    *pvarResult,
   EXCEPINFO  *pexcepinfo,
   UINT       *puArgErr
);
```



## <a name="parameters"></a><span data-ttu-id="18a2a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="18a2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18a2a-107">*dispidMember*</span><span class="sxs-lookup"><span data-stu-id="18a2a-107">*dispidMember*</span></span> 
</dt> <dd>

<span data-ttu-id="18a2a-108">Identificatore del membro.</span><span class="sxs-lookup"><span data-stu-id="18a2a-108">Identifier of the member.</span></span> <span data-ttu-id="18a2a-109">Usare [**CMediaPosition:: GetIDsOfNames**](cmediaposition-getidsofnames.md) per ottenere l'identificatore dispatch.</span><span class="sxs-lookup"><span data-stu-id="18a2a-109">Use [**CMediaPosition::GetIDsOfNames**](cmediaposition-getidsofnames.md) to obtain the dispatch identifier.</span></span>

</dd> <dt>

<span data-ttu-id="18a2a-110">*riid*</span><span class="sxs-lookup"><span data-stu-id="18a2a-110">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="18a2a-111">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="18a2a-111">Reserved for future use.</span></span> <span data-ttu-id="18a2a-112">Deve essere un IID \_ null.</span><span class="sxs-lookup"><span data-stu-id="18a2a-112">Must be IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="18a2a-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="18a2a-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="18a2a-114">Contesto delle impostazioni locali in cui interpretare gli argomenti.</span><span class="sxs-lookup"><span data-stu-id="18a2a-114">Locale context in which to interpret arguments.</span></span>

</dd> <dt>

<span data-ttu-id="18a2a-115">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="18a2a-115">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="18a2a-116">Flag che descrivono il contesto della chiamata.</span><span class="sxs-lookup"><span data-stu-id="18a2a-116">Flags describing the context of the call.</span></span>

</dd> <dt>

<span data-ttu-id="18a2a-117">*pDispParams*</span><span class="sxs-lookup"><span data-stu-id="18a2a-117">*pdispparams*</span></span> 
</dt> <dd>

<span data-ttu-id="18a2a-118">Puntatore a una struttura **DIPPARAMS** contenente gli argomenti.</span><span class="sxs-lookup"><span data-stu-id="18a2a-118">Pointer to a **DIPPARAMS** structure that contains the arguments.</span></span>

</dd> <dt>

<span data-ttu-id="18a2a-119">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="18a2a-119">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="18a2a-120">Puntatore a un **Variant** che riceve il risultato oppure **null** se il chiamante non prevede alcun risultato.</span><span class="sxs-lookup"><span data-stu-id="18a2a-120">Pointer to a **VARIANT** that receives the result, or **NULL** if the caller expects no result.</span></span>

</dd> <dt>

<span data-ttu-id="18a2a-121">*pexcepinfo*</span><span class="sxs-lookup"><span data-stu-id="18a2a-121">*pexcepinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="18a2a-122">Puntatore a una struttura che riceve informazioni sull'eccezione.</span><span class="sxs-lookup"><span data-stu-id="18a2a-122">Pointer to a structure that receives exception information.</span></span>

</dd> <dt>

<span data-ttu-id="18a2a-123">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="18a2a-123">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="18a2a-124">Puntatore a una variabile che riceve l'indice del primo argomento che causa un errore.</span><span class="sxs-lookup"><span data-stu-id="18a2a-124">Pointer to a variable that receives the index of the first argument that causes an error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18a2a-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="18a2a-125">Return value</span></span>

<span data-ttu-id="18a2a-126">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="18a2a-126">Returns an **HRESULT** value.</span></span> <span data-ttu-id="18a2a-127">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="18a2a-127">Possible values include the following.</span></span>



| <span data-ttu-id="18a2a-128">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="18a2a-128">Return code</span></span>                                                                                              | <span data-ttu-id="18a2a-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18a2a-129">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="18a2a-130"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="18a2a-130"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="18a2a-131">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="18a2a-131">Success.</span></span><br/>                              |
| <dl> <span data-ttu-id="18a2a-132"><dt>**DISP \_ E \_ UNKNOWNINTERFACE**</dt></span><span class="sxs-lookup"><span data-stu-id="18a2a-132"><dt>**DISP\_E\_UNKNOWNINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="18a2a-133">Il parametro *riid* non è IID \_ null</span><span class="sxs-lookup"><span data-stu-id="18a2a-133">The *riid* parameter is not IID\_NULL</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="18a2a-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18a2a-134">Requirements</span></span>



| <span data-ttu-id="18a2a-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="18a2a-135">Requirement</span></span> | <span data-ttu-id="18a2a-136">Valore</span><span class="sxs-lookup"><span data-stu-id="18a2a-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18a2a-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="18a2a-137">Header</span></span><br/>  | <dl> <span data-ttu-id="18a2a-138"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="18a2a-138"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="18a2a-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="18a2a-139">Library</span></span><br/> | <dl> <span data-ttu-id="18a2a-140"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="18a2a-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18a2a-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18a2a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18a2a-142">**Classe CMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="18a2a-142">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




