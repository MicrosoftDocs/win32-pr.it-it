---
description: Metodo del costruttore.
ms.assetid: 0fbfdc68-e1df-449f-a7d1-739504db8a2f
title: Costruttore CBaseReferenceClock. CBaseReferenceClock (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.CBaseReferenceClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5ad593d488e367ad6e902b0c931ffbfc3f741a53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330304"
---
# <a name="cbasereferenceclockcbasereferenceclock-constructor"></a><span data-ttu-id="bdd33-103">Costruttore CBaseReferenceClock. CBaseReferenceClock</span><span class="sxs-lookup"><span data-stu-id="bdd33-103">CBaseReferenceClock.CBaseReferenceClock constructor</span></span>

<span data-ttu-id="bdd33-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="bdd33-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdd33-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bdd33-105">Syntax</span></span>


```C++
CBaseReferenceClock(
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr,
   CAMSchedule *pSched = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="bdd33-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bdd33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdd33-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="bdd33-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="bdd33-108">Puntatore a una stringa che contiene il nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bdd33-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="bdd33-109">Per ulteriori informazioni, vedere [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="bdd33-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="bdd33-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="bdd33-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="bdd33-111">Puntatore al proprietario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="bdd33-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="bdd33-112">Se l'oggetto è aggregato, passare un puntatore all'interfaccia IUnknown dell'oggetto di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="bdd33-112">If the object is aggregated, pass a pointer to the aggregating object's IUnknown interface.</span></span> <span data-ttu-id="bdd33-113">In caso contrario, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="bdd33-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bdd33-114">*PHR*</span><span class="sxs-lookup"><span data-stu-id="bdd33-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="bdd33-115">Puntatore a un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bdd33-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="bdd33-116">Se si verifica un errore, il metodo restituisce un codice di errore in questo parametro.</span><span class="sxs-lookup"><span data-stu-id="bdd33-116">If an error occurs, the method returns an error code in this parameter.</span></span> <span data-ttu-id="bdd33-117">Non impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="bdd33-117">Do not set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bdd33-118">*pSched*</span><span class="sxs-lookup"><span data-stu-id="bdd33-118">*pSched*</span></span> 
</dt> <dd>

<span data-ttu-id="bdd33-119">Puntatore a un oggetto [**CAMSchedule**](camschedule.md) .</span><span class="sxs-lookup"><span data-stu-id="bdd33-119">Pointer to a [**CAMSchedule**](camschedule.md) object.</span></span> <span data-ttu-id="bdd33-120">Se **null**, questo metodo crea un nuovo oggetto **CAMSchedule** .</span><span class="sxs-lookup"><span data-stu-id="bdd33-120">If **NULL**, this method creates a new **CAMSchedule** object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bdd33-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bdd33-121">Requirements</span></span>



| <span data-ttu-id="bdd33-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdd33-122">Requirement</span></span> | <span data-ttu-id="bdd33-123">Valore</span><span class="sxs-lookup"><span data-stu-id="bdd33-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdd33-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bdd33-124">Header</span></span><br/>  | <dl> <span data-ttu-id="bdd33-125"><dt>Refclock. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bdd33-125"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bdd33-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="bdd33-126">Library</span></span><br/> | <dl> <span data-ttu-id="bdd33-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bdd33-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdd33-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bdd33-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdd33-129">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="bdd33-129">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




