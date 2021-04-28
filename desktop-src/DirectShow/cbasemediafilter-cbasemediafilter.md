---
description: 'Costruttore CBaseMediaFilter.CBaseMediaFilter : metodo del costruttore.'
ms.assetid: 91290f58-a77b-447f-aa2a-bbee067f5a98
title: Costruttore CBaseMediaFilter.CBaseMediaFilter (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.CBaseMediaFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f123c7af29c6420de6004132180eba8dbf33fa72
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096319"
---
# <a name="cbasemediafiltercbasemediafilter-constructor"></a><span data-ttu-id="7d927-103">Costruttore CBaseMediaFilter.CBaseMediaFilter</span><span class="sxs-lookup"><span data-stu-id="7d927-103">CBaseMediaFilter.CBaseMediaFilter constructor</span></span>

<span data-ttu-id="7d927-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="7d927-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d927-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7d927-105">Syntax</span></span>


```C++
CBaseMediaFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="7d927-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7d927-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d927-107">*Pname*</span><span class="sxs-lookup"><span data-stu-id="7d927-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="7d927-108">Puntatore a una stringa contenente il nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7d927-108">Pointer to a string containing the name of the object.</span></span>

</dd> <dt>

<span data-ttu-id="7d927-109">*Punk*</span><span class="sxs-lookup"><span data-stu-id="7d927-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="7d927-110">Puntatore al proprietario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="7d927-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="7d927-111">Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown dell'oggetto** aggregatore.</span><span class="sxs-lookup"><span data-stu-id="7d927-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="7d927-112">In caso contrario, impostare questo parametro su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="7d927-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7d927-113">*Plock*</span><span class="sxs-lookup"><span data-stu-id="7d927-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="7d927-114">Puntatore a un [**blocco CCritSec,**](ccritsec.md) utilizzato per serializzare le modifiche dello stato.</span><span class="sxs-lookup"><span data-stu-id="7d927-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="7d927-115">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="7d927-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="7d927-116">Identificatore di classe dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7d927-116">Class identifier of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d927-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="7d927-117">Remarks</span></span>

<span data-ttu-id="7d927-118">Se un altro oggetto contiene o aggrega `CBaseMediaFilter` l'oggetto, il **blocco CCritSec** potrebbe essere esterno all'oggetto. `CBaseMediaFilter`</span><span class="sxs-lookup"><span data-stu-id="7d927-118">If another object contains or aggregates the `CBaseMediaFilter` object, the **CCritSec** lock might be external to the `CBaseMediaFilter` object.</span></span> <span data-ttu-id="7d927-119">In tal caso, passare un puntatore al blocco in *pLock*.</span><span class="sxs-lookup"><span data-stu-id="7d927-119">In that case, pass a pointer to the lock in *pLock*.</span></span>

<span data-ttu-id="7d927-120">In caso contrario, è possibile:</span><span class="sxs-lookup"><span data-stu-id="7d927-120">Otherwise, you can:</span></span>

-   <span data-ttu-id="7d927-121">Derivare una classe che eredita sia `CBaseMediaFilter` che **CCritSec**.</span><span class="sxs-lookup"><span data-stu-id="7d927-121">Derive a class that inherits both `CBaseMediaFilter` and **CCritSec**.</span></span> <span data-ttu-id="7d927-122">Per *pLock*, passare il puntatore this.</span><span class="sxs-lookup"><span data-stu-id="7d927-122">For *pLock*, pass the this pointer.</span></span>
-   <span data-ttu-id="7d927-123">Derivare una classe che eredita `CBaseMediaFilter` e contiene una variabile membro **CCritSec.**</span><span class="sxs-lookup"><span data-stu-id="7d927-123">Derive a class that inherits `CBaseMediaFilter` and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="7d927-124">Per *pLock*, passare l'indirizzo di tale variabile.</span><span class="sxs-lookup"><span data-stu-id="7d927-124">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d927-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d927-125">Requirements</span></span>



| <span data-ttu-id="7d927-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d927-126">Requirement</span></span> | <span data-ttu-id="7d927-127">Valore</span><span class="sxs-lookup"><span data-stu-id="7d927-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d927-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d927-128">Header</span></span><br/>  | <dl> <span data-ttu-id="7d927-129"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="7d927-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7d927-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="7d927-130">Library</span></span><br/> | <dl> <span data-ttu-id="7d927-131"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7d927-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d927-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d927-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d927-133">**Classe CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="7d927-133">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




