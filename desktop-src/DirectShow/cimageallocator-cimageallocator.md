---
description: Costruttore CImageAllocator.CImageAllocator - Metodo costruttore.
ms.assetid: 8c215b16-98e5-42fb-a95b-b6df1ade180e
title: Costruttore CImageAllocator.CImageAllocator (Winutil.h)
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
ms.openlocfilehash: f17ae78b668f6cc35e454c5e4e83d38727077ef7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085759"
---
# <a name="cimageallocatorcimageallocator-constructor"></a><span data-ttu-id="382b2-103">Costruttore CImageAllocator.CImageAllocator</span><span class="sxs-lookup"><span data-stu-id="382b2-103">CImageAllocator.CImageAllocator constructor</span></span>

<span data-ttu-id="382b2-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="382b2-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="382b2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="382b2-105">Syntax</span></span>


```C++
CImageAllocator(
   CBaseFilter *pFilter,
   TCHAR       *pName,
   HRESULT     *phr
);
```



## <a name="parameters"></a><span data-ttu-id="382b2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="382b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="382b2-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="382b2-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="382b2-108">Puntatore al filtro proprietario.</span><span class="sxs-lookup"><span data-stu-id="382b2-108">Pointer to the owning filter.</span></span>

</dd> <dt>

<span data-ttu-id="382b2-109">*Pname*</span><span class="sxs-lookup"><span data-stu-id="382b2-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="382b2-110">Puntatore a una stringa contenente il nome di debug dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="382b2-110">Pointer to a string containing the debug name of the allocator.</span></span> <span data-ttu-id="382b2-111">Per altre informazioni, vedere [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="382b2-111">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="382b2-112">*Phr*</span><span class="sxs-lookup"><span data-stu-id="382b2-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="382b2-113">Puntatore a un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="382b2-113">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="382b2-114">Impostare il valore su S \_ OK prima di creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="382b2-114">Set the value to S\_OK before creating the object.</span></span> <span data-ttu-id="382b2-115">Se il costruttore ha esito negativo, il valore viene impostato su un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="382b2-115">If the constructor fails, the value is set to an error code.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="382b2-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="382b2-116">Requirements</span></span>



| <span data-ttu-id="382b2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="382b2-117">Requirement</span></span> | <span data-ttu-id="382b2-118">Valore</span><span class="sxs-lookup"><span data-stu-id="382b2-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="382b2-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="382b2-119">Header</span></span><br/>  | <dl> <span data-ttu-id="382b2-120"><dt>Winutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="382b2-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="382b2-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="382b2-121">Library</span></span><br/> | <dl> <span data-ttu-id="382b2-122"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="382b2-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="382b2-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="382b2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="382b2-124">**Classe CImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="382b2-124">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




