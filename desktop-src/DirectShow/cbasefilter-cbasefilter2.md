---
description: Costruttore CBaseFilter.CBaseFilter(const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID) - Metodo costruttore.
ms.assetid: b6433ec9-6710-4c2f-968f-00e0d9f8c7a5
title: Costruttore CBaseFilter.CBaseFilter(const *TCHAR, LPUNKNOWN, CCritSec*, REFCLSID) (Amfilter.h)
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
ms.openlocfilehash: b621bdb3f6a15ae950959a65eba8841bde399b81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099829"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-constructor"></a><span data-ttu-id="c4dd3-103">Costruttore CBaseFilter.CBaseFilter(const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID)</span><span class="sxs-lookup"><span data-stu-id="c4dd3-103">CBaseFilter.CBaseFilter(const TCHAR\*, LPUNKNOWN, CCritSec\*, REFCLSID) constructor</span></span>

<span data-ttu-id="c4dd3-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="c4dd3-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4dd3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4dd3-105">Syntax</span></span>


```C++
CBaseFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="c4dd3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4dd3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4dd3-107">*Pname*</span><span class="sxs-lookup"><span data-stu-id="c4dd3-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="c4dd3-108">Puntatore a una stringa contenente il nome del filtro, a scopo di debug.</span><span class="sxs-lookup"><span data-stu-id="c4dd3-108">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="c4dd3-109">*Punk*</span><span class="sxs-lookup"><span data-stu-id="c4dd3-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="c4dd3-110">Puntatore al proprietario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="c4dd3-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="c4dd3-111">Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown dell'oggetto** aggregatore.</span><span class="sxs-lookup"><span data-stu-id="c4dd3-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="c4dd3-112">In caso contrario, impostare questo parametro su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="c4dd3-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c4dd3-113">*Plock*</span><span class="sxs-lookup"><span data-stu-id="c4dd3-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="c4dd3-114">Puntatore a un [**blocco CCritSec,**](ccritsec.md) utilizzato per serializzare le modifiche dello stato.</span><span class="sxs-lookup"><span data-stu-id="c4dd3-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="c4dd3-115">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="c4dd3-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="c4dd3-116">Identificatore di classe (CLSID) del filtro.</span><span class="sxs-lookup"><span data-stu-id="c4dd3-116">Class identifier (CLSID) of the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4dd3-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4dd3-117">Remarks</span></span>

<span data-ttu-id="c4dd3-118">Per l'oggetto sezione critica, è in genere necessario eseguire una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c4dd3-118">For the critical section object, you would typically do one of the following:</span></span>

-   <span data-ttu-id="c4dd3-119">Derivare una classe che eredita **sia CBaseFilter** che **CCritSec.**</span><span class="sxs-lookup"><span data-stu-id="c4dd3-119">Derive a class that inherits both **CBaseFilter** and **CCritSec**.</span></span> <span data-ttu-id="c4dd3-120">Per *pLock*, passare il `this` puntatore .</span><span class="sxs-lookup"><span data-stu-id="c4dd3-120">For *pLock*, pass the `this` pointer.</span></span>
-   <span data-ttu-id="c4dd3-121">Derivare una classe che eredita **CBaseFilter** e contiene una **variabile membro CCritSec.**</span><span class="sxs-lookup"><span data-stu-id="c4dd3-121">Derive a class that inherits **CBaseFilter** and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="c4dd3-122">Per *pLock*, passare l'indirizzo di tale variabile.</span><span class="sxs-lookup"><span data-stu-id="c4dd3-122">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4dd3-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4dd3-123">Requirements</span></span>



| <span data-ttu-id="c4dd3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4dd3-124">Requirement</span></span> | <span data-ttu-id="c4dd3-125">Valore</span><span class="sxs-lookup"><span data-stu-id="c4dd3-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4dd3-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4dd3-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c4dd3-127"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4dd3-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c4dd3-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="c4dd3-128">Library</span></span><br/> | <dl> <span data-ttu-id="c4dd3-129"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c4dd3-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4dd3-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4dd3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4dd3-131">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="c4dd3-131">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




