---
description: "Metodo CMediaEvent.Invoke: fornisce l'accesso alle proprietà e ai metodi esposti da un oggetto."
ms.assetid: 2b091b57-0855-489a-9a33-cfc75f63ad07
title: Metodo CMediaEvent.Invoke (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea812d0c7629b98d90f3f7e535d229c707452b23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095539"
---
# <a name="cmediaeventinvoke-method"></a><span data-ttu-id="bf0e0-103">Metodo CMediaEvent.Invoke</span><span class="sxs-lookup"><span data-stu-id="bf0e0-103">CMediaEvent.Invoke method</span></span>

<span data-ttu-id="bf0e0-104">Fornisce l'accesso a proprietà e metodi esposti da un oggetto.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-104">Provides access to properties and methods exposed by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf0e0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf0e0-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="bf0e0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf0e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf0e0-107">*dispidMember*</span><span class="sxs-lookup"><span data-stu-id="bf0e0-107">*dispidMember*</span></span> 
</dt> <dd>

<span data-ttu-id="bf0e0-108">Identificatore del membro.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-108">Identifier of the member.</span></span> <span data-ttu-id="bf0e0-109">Usare [**CMediaEvent::GetIDsOfNames**](cmediaevent-getidsofnames.md) o la documentazione dell'oggetto per ottenere l'identificatore dispatch.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-109">Use [**CMediaEvent::GetIDsOfNames**](cmediaevent-getidsofnames.md) or the object's documentation to obtain the dispatch identifier.</span></span>

</dd> <dt>

<span data-ttu-id="bf0e0-110">*Riid*</span><span class="sxs-lookup"><span data-stu-id="bf0e0-110">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="bf0e0-111">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-111">Reserved for future use.</span></span> <span data-ttu-id="bf0e0-112">Deve essere IID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-112">Must be IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="bf0e0-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="bf0e0-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="bf0e0-114">Contesto delle impostazioni locali in cui interpretare gli argomenti.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-114">Locale context in which to interpret arguments.</span></span>

</dd> <dt>

<span data-ttu-id="bf0e0-115">*Wflags*</span><span class="sxs-lookup"><span data-stu-id="bf0e0-115">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="bf0e0-116">Flag che descrivono il contesto della `CMediaEvent::Invoke` chiamata.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-116">Flags describing the context of the `CMediaEvent::Invoke` call.</span></span>

</dd> <dt>

<span data-ttu-id="bf0e0-117">*pdispparams*</span><span class="sxs-lookup"><span data-stu-id="bf0e0-117">*pdispparams*</span></span> 
</dt> <dd>

<span data-ttu-id="bf0e0-118">Puntatore a una struttura contenente una matrice di argomenti, una matrice di ID di invio di argomenti per argomenti denominati e conteggi per il numero di elementi nelle matrici.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-118">Pointer to a structure containing an array of arguments, an array of argument dispatch IDs for named arguments, and counts for the number of elements in the arrays.</span></span>

</dd> <dt>

<span data-ttu-id="bf0e0-119">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="bf0e0-119">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="bf0e0-120">Puntatore alla posizione in cui deve essere archiviato il risultato oppure **NULL** se il chiamante non prevede alcun risultato.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-120">Pointer to where the result is to be stored, or **NULL** if the caller expects no result.</span></span>

</dd> <dt>

<span data-ttu-id="bf0e0-121">*pexcepinfo*</span><span class="sxs-lookup"><span data-stu-id="bf0e0-121">*pexcepinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="bf0e0-122">Puntatore a una struttura contenente informazioni sull'eccezione.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-122">Pointer to a structure containing exception information.</span></span>

</dd> <dt>

<span data-ttu-id="bf0e0-123">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="bf0e0-123">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="bf0e0-124">Puntatore all'indice del primo argomento, all'interno della matrice **rgvarg** della struttura **DISPPARAMS,** che presenta un errore.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-124">Pointer to the index of the first argument, within the **DISPPARAMS** structure's **rgvarg** array, that has an error.</span></span> <span data-ttu-id="bf0e0-125">Per altre informazioni su **DISPPARAMS,** vedere Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-125">For more information on **DISPPARAMS**, see the Platform SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf0e0-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf0e0-126">Return value</span></span>

<span data-ttu-id="bf0e0-127">Restituisce DISP \_ E \_ UNKNOWNINTERFACE se *riid* non è IID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-127">Returns DISP\_E\_UNKNOWNINTERFACE if *riid* is not IID\_NULL.</span></span> <span data-ttu-id="bf0e0-128">Restituisce uno dei codici di errore da [**CMediaEvent::GetTypeInfo**](cmediaevent-gettypeinfo.md) se la chiamata non riesce.</span><span class="sxs-lookup"><span data-stu-id="bf0e0-128">Returns one of the error codes from [**CMediaEvent::GetTypeInfo**](cmediaevent-gettypeinfo.md) if the call fails.</span></span> <span data-ttu-id="bf0e0-129">In caso contrario, **restituisce il valore HRESULT** dalla chiamata a **IDispatch::Invoke.**</span><span class="sxs-lookup"><span data-stu-id="bf0e0-129">Otherwise, returns the **HRESULT** from the call to **IDispatch::Invoke**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf0e0-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf0e0-130">Requirements</span></span>



| <span data-ttu-id="bf0e0-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf0e0-131">Requirement</span></span> | <span data-ttu-id="bf0e0-132">Valore</span><span class="sxs-lookup"><span data-stu-id="bf0e0-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf0e0-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf0e0-133">Header</span></span><br/>  | <dl> <span data-ttu-id="bf0e0-134"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf0e0-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bf0e0-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="bf0e0-135">Library</span></span><br/> | <dl> <span data-ttu-id="bf0e0-136"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bf0e0-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf0e0-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf0e0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf0e0-138">**Classe CMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="bf0e0-138">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




