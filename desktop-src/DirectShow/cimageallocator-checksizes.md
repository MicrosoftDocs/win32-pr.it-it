---
description: Il metodo CheckSizes controlla le proprietà dell'allocatore rispetto al tipo di supporto corrente.
ms.assetid: 040b4ed0-c1cc-4995-a0f8-86efa493f84b
title: Metodo CImageAllocator. CheckSizes (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CheckSizes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71184d4915911c29bff9d3a6fa9985942a4aaa44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329774"
---
# <a name="cimageallocatorchecksizes-method"></a><span data-ttu-id="613c6-103">CImageAllocator. CheckSizes, metodo</span><span class="sxs-lookup"><span data-stu-id="613c6-103">CImageAllocator.CheckSizes method</span></span>

<span data-ttu-id="613c6-104">Il `CheckSizes` metodo controlla le proprietà dell'allocatore rispetto al tipo di supporto corrente.</span><span class="sxs-lookup"><span data-stu-id="613c6-104">The `CheckSizes` method checks allocator properties against the current media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="613c6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="613c6-105">Syntax</span></span>


```C++
HRESULT CheckSizes(
   ALLOCATOR_PROPERTIES *pRequest
);
```



## <a name="parameters"></a><span data-ttu-id="613c6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="613c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="613c6-107">*pRequest*</span><span class="sxs-lookup"><span data-stu-id="613c6-107">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="613c6-108">Puntatore a una struttura di [**\_ proprietà dell'allocatore**](/windows/win32/api/strmif/ns-strmif-allocator_properties) che descrive le proprietà dell'allocatore richieste.</span><span class="sxs-lookup"><span data-stu-id="613c6-108">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that describes the requested allocator properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="613c6-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="613c6-109">Return value</span></span>

<span data-ttu-id="613c6-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="613c6-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="613c6-111">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="613c6-111">Possible values include the following.</span></span>



| <span data-ttu-id="613c6-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="613c6-112">Return code</span></span>                                                                                           | <span data-ttu-id="613c6-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="613c6-113">Description</span></span>                                                                 |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="613c6-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="613c6-114"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="613c6-115">Le proprietà richieste sono compatibili con il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="613c6-115">The requested properties are compatible with the media type.</span></span><br/>     |
| <dl> <span data-ttu-id="613c6-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="613c6-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="613c6-117">Le proprietà richieste non sono compatibili con il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="613c6-117">The requested properties are not compatible with the media type.</span></span><br/> |
| <dl> <span data-ttu-id="613c6-118"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="613c6-118"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="613c6-119">Il pin proprietario non è connesso.</span><span class="sxs-lookup"><span data-stu-id="613c6-119">The owning pin is not connected.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="613c6-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="613c6-120">Remarks</span></span>

<span data-ttu-id="613c6-121">Quando il metodo restituisce, se il valore restituito è \_ OK, il membro **cbBuffer** di *pRequest* contiene le dimensioni effettive del buffer.</span><span class="sxs-lookup"><span data-stu-id="613c6-121">When the method returns, if the return value is S\_OK, the **cbBuffer** member of *pRequest* contains the actual buffer size.</span></span> <span data-ttu-id="613c6-122">Questo potrebbe essere maggiore della dimensione richiesta, ma non sarà mai minore.</span><span class="sxs-lookup"><span data-stu-id="613c6-122">This might be larger than the requested size, but will never be smaller.</span></span>

## <a name="requirements"></a><span data-ttu-id="613c6-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="613c6-123">Requirements</span></span>



| <span data-ttu-id="613c6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="613c6-124">Requirement</span></span> | <span data-ttu-id="613c6-125">Valore</span><span class="sxs-lookup"><span data-stu-id="613c6-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="613c6-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="613c6-126">Header</span></span><br/>  | <dl> <span data-ttu-id="613c6-127"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="613c6-127"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="613c6-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="613c6-128">Library</span></span><br/> | <dl> <span data-ttu-id="613c6-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="613c6-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="613c6-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="613c6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="613c6-131">**Classe CImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="613c6-131">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




