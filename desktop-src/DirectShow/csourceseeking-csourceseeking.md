---
description: 'Costruttore CSourceSeeking.CSourceSeeking : metodo del costruttore.'
ms.assetid: a51d90c9-4046-42dc-b7cf-51b904c5f57a
title: Costruttore CSourceSeeking.CSourceSeeking (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.CSourceSeeking
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7fcca70408e76466a88c620e3907271d49930973
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098819"
---
# <a name="csourceseekingcsourceseeking-constructor"></a><span data-ttu-id="326a3-103">Costruttore CSourceSeeking.CSourceSeeking</span><span class="sxs-lookup"><span data-stu-id="326a3-103">CSourceSeeking.CSourceSeeking constructor</span></span>

<span data-ttu-id="326a3-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="326a3-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="326a3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="326a3-105">Syntax</span></span>


```C++
CSourceSeeking(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         CCritSec  *pLock
);
```



## <a name="parameters"></a><span data-ttu-id="326a3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="326a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="326a3-107">*Pname*</span><span class="sxs-lookup"><span data-stu-id="326a3-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="326a3-108">Puntatore a una stringa contenente il nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="326a3-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="326a3-109">Per altre informazioni, vedere [**CBaseObject.**](cbaseobject.md)</span><span class="sxs-lookup"><span data-stu-id="326a3-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="326a3-110">*Punk*</span><span class="sxs-lookup"><span data-stu-id="326a3-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="326a3-111">Puntatore al proprietario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="326a3-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="326a3-112">Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown dell'oggetto** aggregatore.</span><span class="sxs-lookup"><span data-stu-id="326a3-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="326a3-113">In caso contrario, impostare questo parametro su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="326a3-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="326a3-114">*Phr*</span><span class="sxs-lookup"><span data-stu-id="326a3-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="326a3-115">Puntatore a un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="326a3-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="326a3-116">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="326a3-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="326a3-117">*Plock*</span><span class="sxs-lookup"><span data-stu-id="326a3-117">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="326a3-118">Puntatore a [**un oggetto CCritSec.**](ccritsec.md)</span><span class="sxs-lookup"><span data-stu-id="326a3-118">Pointer to a [**CCritSec**](ccritsec.md) object.</span></span> <span data-ttu-id="326a3-119">Nella classe derivata dichiarare una **variabile membro CCritSec** e usare l'indirizzo per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="326a3-119">In your derived class, declare a **CCritSec** member variable and use the address of it for this parameter.</span></span> <span data-ttu-id="326a3-120">La classe usa questa sezione critica per sincronizzare l'accesso a ora di inizio e `CSourceSeeking` arresto, durata e velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="326a3-120">The `CSourceSeeking` class uses this critical section to synchronize access to the start and stop times, duration, and playback rate.</span></span> <span data-ttu-id="326a3-121">Ogni volta che si accede a tali variabili nella classe derivata, mantenere questo blocco.</span><span class="sxs-lookup"><span data-stu-id="326a3-121">Whenever you access those variables in your derived class, hold this lock.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="326a3-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="326a3-122">Requirements</span></span>



| <span data-ttu-id="326a3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="326a3-123">Requirement</span></span> | <span data-ttu-id="326a3-124">Valore</span><span class="sxs-lookup"><span data-stu-id="326a3-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="326a3-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="326a3-125">Header</span></span><br/>  | <dl> <span data-ttu-id="326a3-126"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="326a3-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="326a3-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="326a3-127">Library</span></span><br/> | <dl> <span data-ttu-id="326a3-128"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="326a3-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="326a3-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="326a3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="326a3-130">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="326a3-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




