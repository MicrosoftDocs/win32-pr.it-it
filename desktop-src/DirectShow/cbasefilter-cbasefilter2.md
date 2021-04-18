---
description: Metodo del costruttore.
ms.assetid: b6433ec9-6710-4c2f-968f-00e0d9f8c7a5
title: Costruttore CBaseFilter. CBaseFilter (const TCHAR *, LPUNKNOWN, CCritSec*, REFCLSID) (Amfilter. h)
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
ms.openlocfilehash: 40ac48a1fd28b9b50a8f1fa9c698ea5db49d97b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325080"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-constructor"></a><span data-ttu-id="c34db-103">Costruttore CBaseFilter. CBaseFilter (const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID)</span><span class="sxs-lookup"><span data-stu-id="c34db-103">CBaseFilter.CBaseFilter(const TCHAR\*, LPUNKNOWN, CCritSec\*, REFCLSID) constructor</span></span>

<span data-ttu-id="c34db-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="c34db-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c34db-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c34db-105">Syntax</span></span>


```C++
CBaseFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="c34db-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c34db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c34db-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="c34db-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="c34db-108">Puntatore a una stringa che contiene il nome del filtro, a scopo di debug.</span><span class="sxs-lookup"><span data-stu-id="c34db-108">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="c34db-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="c34db-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="c34db-110">Puntatore al proprietario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="c34db-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="c34db-111">Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown** dell'oggetto di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="c34db-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="c34db-112">In caso contrario, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="c34db-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c34db-113">*pLock*</span><span class="sxs-lookup"><span data-stu-id="c34db-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="c34db-114">Puntatore a un blocco [**CCritSec**](ccritsec.md) , usato per serializzare le modifiche di stato.</span><span class="sxs-lookup"><span data-stu-id="c34db-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="c34db-115">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="c34db-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="c34db-116">Identificatore di classe (CLSID) del filtro.</span><span class="sxs-lookup"><span data-stu-id="c34db-116">Class identifier (CLSID) of the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c34db-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="c34db-117">Remarks</span></span>

<span data-ttu-id="c34db-118">Per l'oggetto sezione critica, in genere si esegue una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c34db-118">For the critical section object, you would typically do one of the following:</span></span>

-   <span data-ttu-id="c34db-119">Derivare una classe che eredita sia **CBaseFilter** che **CCritSec**.</span><span class="sxs-lookup"><span data-stu-id="c34db-119">Derive a class that inherits both **CBaseFilter** and **CCritSec**.</span></span> <span data-ttu-id="c34db-120">Per *pLock*, passare il `this` puntatore.</span><span class="sxs-lookup"><span data-stu-id="c34db-120">For *pLock*, pass the `this` pointer.</span></span>
-   <span data-ttu-id="c34db-121">Derivare una classe che eredita **CBaseFilter** e contiene una variabile membro **CCritSec** .</span><span class="sxs-lookup"><span data-stu-id="c34db-121">Derive a class that inherits **CBaseFilter** and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="c34db-122">Per *pLock*, passare l'indirizzo della variabile.</span><span class="sxs-lookup"><span data-stu-id="c34db-122">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="c34db-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c34db-123">Requirements</span></span>



| <span data-ttu-id="c34db-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c34db-124">Requirement</span></span> | <span data-ttu-id="c34db-125">Valore</span><span class="sxs-lookup"><span data-stu-id="c34db-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c34db-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c34db-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c34db-127"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c34db-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c34db-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="c34db-128">Library</span></span><br/> | <dl> <span data-ttu-id="c34db-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c34db-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c34db-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c34db-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c34db-131">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="c34db-131">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




