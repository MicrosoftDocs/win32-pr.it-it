---
description: Metodo del costruttore.
ms.assetid: 8c215b16-98e5-42fb-a95b-b6df1ade180e
title: Costruttore CImageAllocator. CImageAllocator (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5f6873e8cc073e0b716f94c980ecceba8f4512f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329773"
---
# <a name="cimageallocatorcimageallocator-constructor"></a><span data-ttu-id="38197-103">Costruttore CImageAllocator. CImageAllocator</span><span class="sxs-lookup"><span data-stu-id="38197-103">CImageAllocator.CImageAllocator constructor</span></span>

<span data-ttu-id="38197-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="38197-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="38197-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="38197-105">Syntax</span></span>


```C++
CImageAllocator(
   CBaseFilter *pFilter,
   TCHAR       *pName,
   HRESULT     *phr
);
```



## <a name="parameters"></a><span data-ttu-id="38197-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="38197-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38197-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="38197-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="38197-108">Puntatore al filtro proprietario.</span><span class="sxs-lookup"><span data-stu-id="38197-108">Pointer to the owning filter.</span></span>

</dd> <dt>

<span data-ttu-id="38197-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="38197-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="38197-110">Puntatore a una stringa contenente il nome di debug dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="38197-110">Pointer to a string containing the debug name of the allocator.</span></span> <span data-ttu-id="38197-111">Per ulteriori informazioni, vedere [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="38197-111">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="38197-112">*PHR*</span><span class="sxs-lookup"><span data-stu-id="38197-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="38197-113">Puntatore a un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="38197-113">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="38197-114">Impostare il valore su S \_ OK prima di creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="38197-114">Set the value to S\_OK before creating the object.</span></span> <span data-ttu-id="38197-115">Se il costruttore ha esito negativo, il valore viene impostato su un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="38197-115">If the constructor fails, the value is set to an error code.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="38197-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38197-116">Requirements</span></span>



| <span data-ttu-id="38197-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="38197-117">Requirement</span></span> | <span data-ttu-id="38197-118">Valore</span><span class="sxs-lookup"><span data-stu-id="38197-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38197-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="38197-119">Header</span></span><br/>  | <dl> <span data-ttu-id="38197-120"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="38197-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="38197-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="38197-121">Library</span></span><br/> | <dl> <span data-ttu-id="38197-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="38197-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38197-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38197-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38197-124">**Classe CImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="38197-124">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




