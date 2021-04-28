---
description: Costruttore CBaseFilter.CBaseFilter(const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID, HRESULT \* ) - Metodo costruttore.
ms.assetid: 705a075e-3f0f-4e7d-94b6-3458f87b6718
title: Costruttore CBaseFilter.CBaseFilter(const *TCHAR, LPUNKNOWN, CCritSec,* REFCLSID, HRESULT*) (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.CBaseFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f85fc666d299d5e120f71cfeaec5fc2f88e72761
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120109"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-hresult-constructor"></a><span data-ttu-id="22e35-103">Costruttore CBaseFilter.CBaseFilter(const \* TCHAR, LPUNKNOWN, CCritSec, \* REFCLSID, \* HRESULT)</span><span class="sxs-lookup"><span data-stu-id="22e35-103">CBaseFilter.CBaseFilter(const TCHAR\*, LPUNKNOWN, CCritSec\*, REFCLSID, HRESULT\*) constructor</span></span>

<span data-ttu-id="22e35-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="22e35-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="22e35-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="22e35-105">Syntax</span></span>


```C++
CBaseFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="22e35-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="22e35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22e35-107">*Pname*</span><span class="sxs-lookup"><span data-stu-id="22e35-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="22e35-108">Puntatore a una stringa contenente il nome del filtro, a scopo di debug.</span><span class="sxs-lookup"><span data-stu-id="22e35-108">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="22e35-109">*Punk*</span><span class="sxs-lookup"><span data-stu-id="22e35-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="22e35-110">Puntatore al proprietario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="22e35-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="22e35-111">Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown dell'oggetto** aggregatore.</span><span class="sxs-lookup"><span data-stu-id="22e35-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="22e35-112">In caso contrario, impostare questo parametro su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="22e35-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="22e35-113">*Plock*</span><span class="sxs-lookup"><span data-stu-id="22e35-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="22e35-114">Puntatore a un [**blocco CCritSec,**](ccritsec.md) utilizzato per serializzare le modifiche dello stato.</span><span class="sxs-lookup"><span data-stu-id="22e35-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="22e35-115">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="22e35-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="22e35-116">Identificatore di classe (CLSID) del filtro.</span><span class="sxs-lookup"><span data-stu-id="22e35-116">Class identifier (CLSID) of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="22e35-117">*Phr*</span><span class="sxs-lookup"><span data-stu-id="22e35-117">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="22e35-118">Puntatore a un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="22e35-118">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="22e35-119">Il costruttore ignora questo parametro.</span><span class="sxs-lookup"><span data-stu-id="22e35-119">The constructor ignores this parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="22e35-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="22e35-120">Remarks</span></span>

<span data-ttu-id="22e35-121">Per l'oggetto sezione critica, è in genere necessario eseguire una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="22e35-121">For the critical section object, you would typically do one of the following:</span></span>

-   <span data-ttu-id="22e35-122">Derivare una classe che eredita **sia CBaseFilter** che **CCritSec.**</span><span class="sxs-lookup"><span data-stu-id="22e35-122">Derive a class that inherits both **CBaseFilter** and **CCritSec**.</span></span> <span data-ttu-id="22e35-123">Per *pLock*, passare il `this` puntatore .</span><span class="sxs-lookup"><span data-stu-id="22e35-123">For *pLock*, pass the `this` pointer.</span></span>
-   <span data-ttu-id="22e35-124">Derivare una classe che eredita **CBaseFilter** e contiene una **variabile membro CCritSec.**</span><span class="sxs-lookup"><span data-stu-id="22e35-124">Derive a class that inherits **CBaseFilter** and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="22e35-125">Per *pLock*, passare l'indirizzo di tale variabile.</span><span class="sxs-lookup"><span data-stu-id="22e35-125">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="22e35-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22e35-126">Requirements</span></span>



| <span data-ttu-id="22e35-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="22e35-127">Requirement</span></span> | <span data-ttu-id="22e35-128">Valore</span><span class="sxs-lookup"><span data-stu-id="22e35-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22e35-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="22e35-129">Header</span></span><br/>  | <dl> <span data-ttu-id="22e35-130"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="22e35-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="22e35-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="22e35-131">Library</span></span><br/> | <dl> <span data-ttu-id="22e35-132"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="22e35-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22e35-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="22e35-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22e35-134">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="22e35-134">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




