---
description: "Metodo CMediaControl.Invoke: fornisce l'accesso alle proprietà e ai metodi esposti da un oggetto."
ms.assetid: 05006f1e-24ff-4ed2-8291-2ba48495fec0
title: Metodo CMediaControl.Invoke (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe077b2c69f603eef8737cbf7ea8c514e9b90c85
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085639"
---
# <a name="cmediacontrolinvoke-method"></a><span data-ttu-id="d3858-103">Metodo CMediaControl.Invoke</span><span class="sxs-lookup"><span data-stu-id="d3858-103">CMediaControl.Invoke method</span></span>

<span data-ttu-id="d3858-104">Fornisce l'accesso a proprietà e metodi esposti da un oggetto.</span><span class="sxs-lookup"><span data-stu-id="d3858-104">Provides access to properties and methods exposed by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3858-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3858-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="d3858-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d3858-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3858-107">*dispidMember*</span><span class="sxs-lookup"><span data-stu-id="d3858-107">*dispidMember*</span></span> 
</dt> <dd>

<span data-ttu-id="d3858-108">Identificatore del membro.</span><span class="sxs-lookup"><span data-stu-id="d3858-108">Identifier of the member.</span></span> <span data-ttu-id="d3858-109">Usare [**CMediaControl::GetIDsOfNames**](cmediacontrol-getidsofnames.md) o la documentazione dell'oggetto per ottenere l'identificatore di invio.</span><span class="sxs-lookup"><span data-stu-id="d3858-109">Use [**CMediaControl::GetIDsOfNames**](cmediacontrol-getidsofnames.md) or the object's documentation to obtain the dispatch identifier.</span></span>

</dd> <dt>

<span data-ttu-id="d3858-110">*Riid*</span><span class="sxs-lookup"><span data-stu-id="d3858-110">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="d3858-111">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="d3858-111">Reserved for future use.</span></span> <span data-ttu-id="d3858-112">Deve essere IID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="d3858-112">Must be IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="d3858-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="d3858-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="d3858-114">Contesto delle impostazioni locali in cui interpretare gli argomenti.</span><span class="sxs-lookup"><span data-stu-id="d3858-114">Locale context in which to interpret arguments.</span></span>

</dd> <dt>

<span data-ttu-id="d3858-115">*Wflags*</span><span class="sxs-lookup"><span data-stu-id="d3858-115">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="d3858-116">Flag che descrivono il contesto della `CMediaControl::Invoke` chiamata.</span><span class="sxs-lookup"><span data-stu-id="d3858-116">Flags describing the context of the `CMediaControl::Invoke` call.</span></span>

</dd> <dt>

<span data-ttu-id="d3858-117">*pdispparams*</span><span class="sxs-lookup"><span data-stu-id="d3858-117">*pdispparams*</span></span> 
</dt> <dd>

<span data-ttu-id="d3858-118">Puntatore a una struttura contenente una matrice di argomenti, una matrice di ID dispatch di argomenti per argomenti denominati e conteggi per il numero di elementi nelle matrici.</span><span class="sxs-lookup"><span data-stu-id="d3858-118">Pointer to a structure containing an array of arguments, an array of argument dispatch IDs for named arguments, and counts for number of elements in the arrays.</span></span>

</dd> <dt>

<span data-ttu-id="d3858-119">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="d3858-119">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="d3858-120">Puntatore alla posizione in cui deve essere archiviato il risultato oppure **NULL** se il chiamante non prevede alcun risultato.</span><span class="sxs-lookup"><span data-stu-id="d3858-120">Pointer to where the result is to be stored, or **NULL** if the caller expects no result.</span></span>

</dd> <dt>

<span data-ttu-id="d3858-121">*pexcepinfo*</span><span class="sxs-lookup"><span data-stu-id="d3858-121">*pexcepinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="d3858-122">Puntatore a una struttura contenente informazioni sull'eccezione.</span><span class="sxs-lookup"><span data-stu-id="d3858-122">Pointer to a structure containing exception information.</span></span>

</dd> <dt>

<span data-ttu-id="d3858-123">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="d3858-123">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="d3858-124">Puntatore all'indice del primo argomento, all'interno della matrice **rgvarg** della struttura **DISPPARAMS,** che contiene un errore.</span><span class="sxs-lookup"><span data-stu-id="d3858-124">Pointer to the index of the first argument, within the **DISPPARAMS** structure's **rgvarg** array, that has an error.</span></span> <span data-ttu-id="d3858-125">Per altre informazioni su **DISPPARAMS,** vedere Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="d3858-125">For more information on **DISPPARAMS**, see the Platform SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3858-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d3858-126">Return value</span></span>

<span data-ttu-id="d3858-127">Restituisce DISP \_ E \_ UNKNOWNINTERFACE se *riid* non è IID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="d3858-127">Returns DISP\_E\_UNKNOWNINTERFACE if *riid* is not IID\_NULL.</span></span> <span data-ttu-id="d3858-128">Restituisce uno dei codici di errore da [**CMediaControl::GetTypeInfo**](cmediacontrol-gettypeinfo.md) se la chiamata non riesce.</span><span class="sxs-lookup"><span data-stu-id="d3858-128">Returns one of the error codes from [**CMediaControl::GetTypeInfo**](cmediacontrol-gettypeinfo.md) if the call fails.</span></span> <span data-ttu-id="d3858-129">In caso contrario, **restituisce il valore HRESULT** dalla chiamata a **IDispatch::Invoke.**</span><span class="sxs-lookup"><span data-stu-id="d3858-129">Otherwise, returns the **HRESULT** from the call to **IDispatch::Invoke**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3858-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3858-130">Requirements</span></span>



| <span data-ttu-id="d3858-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3858-131">Requirement</span></span> | <span data-ttu-id="d3858-132">Valore</span><span class="sxs-lookup"><span data-stu-id="d3858-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3858-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3858-133">Header</span></span><br/>  | <dl> <span data-ttu-id="d3858-134"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3858-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d3858-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="d3858-135">Library</span></span><br/> | <dl> <span data-ttu-id="d3858-136"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d3858-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3858-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3858-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3858-138">**Classe CMediaControl**</span><span class="sxs-lookup"><span data-stu-id="d3858-138">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




