---
description: Il metodo InitAllocator crea un allocatore di memoria.
ms.assetid: a1fa0ffb-ed43-446d-811e-6c3594743592
title: Metodo CBaseOutputPin.InitAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.InitAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7e5385671ba4c7fdf1b719f83aafba7d84421bce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332059"
---
# <a name="cbaseoutputpininitallocator-method"></a><span data-ttu-id="473c6-103">Metodo tAllocator CBaseOutputPin.Ini</span><span class="sxs-lookup"><span data-stu-id="473c6-103">CBaseOutputPin.InitAllocator method</span></span>

<span data-ttu-id="473c6-104">Il `InitAllocator` metodo crea un allocatore di memoria.</span><span class="sxs-lookup"><span data-stu-id="473c6-104">The `InitAllocator` method creates a memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="473c6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="473c6-105">Syntax</span></span>


```C++
virtual HRESULT InitAllocator(
   IMemAllocator **ppAlloc
);
```



## <a name="parameters"></a><span data-ttu-id="473c6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="473c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="473c6-107">*ppAlloc*</span><span class="sxs-lookup"><span data-stu-id="473c6-107">*ppAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="473c6-108">Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="473c6-108">Address of a variable that receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="473c6-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="473c6-109">Return value</span></span>

<span data-ttu-id="473c6-110">Restituisce \_ OK se ha esito positivo o un codice di errore della funzione **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="473c6-110">Returns S\_OK if successful, or an error code from the **CoCreateInstance** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="473c6-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="473c6-111">Remarks</span></span>

<span data-ttu-id="473c6-112">Se il pin di input non fornisce un allocatore di memoria, il metodo [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md) chiama questo metodo per creare un allocatore.</span><span class="sxs-lookup"><span data-stu-id="473c6-112">If the input pin does not provide a memory allocator, the [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md) method calls this method to create an allocator.</span></span>

## <a name="requirements"></a><span data-ttu-id="473c6-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="473c6-113">Requirements</span></span>



| <span data-ttu-id="473c6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="473c6-114">Requirement</span></span> | <span data-ttu-id="473c6-115">Valore</span><span class="sxs-lookup"><span data-stu-id="473c6-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="473c6-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="473c6-116">Header</span></span><br/>  | <dl> <span data-ttu-id="473c6-117"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="473c6-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="473c6-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="473c6-118">Library</span></span><br/> | <dl> <span data-ttu-id="473c6-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="473c6-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="473c6-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="473c6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="473c6-121">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="473c6-121">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




