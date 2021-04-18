---
description: Metodo del costruttore.
ms.assetid: 2340b39a-cab6-4524-b8cd-b22d4bdd24d0
title: Costruttore CMemAllocator. CMemAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b650e23761c3fe5b3f5014666f90c679f088c4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327444"
---
# <a name="cmemallocatorcmemallocator-constructor"></a><span data-ttu-id="74107-103">Costruttore CMemAllocator. CMemAllocator</span><span class="sxs-lookup"><span data-stu-id="74107-103">CMemAllocator.CMemAllocator constructor</span></span>

<span data-ttu-id="74107-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="74107-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="74107-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74107-105">Syntax</span></span>


```C++
CMemAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="74107-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="74107-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74107-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="74107-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="74107-108">Puntatore a una stringa che contiene il nome dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="74107-108">Pointer to a string containing the name of the allocator.</span></span>

</dd> <dt>

<span data-ttu-id="74107-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="74107-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="74107-110">Puntatore al proprietario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="74107-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="74107-111">Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown** dell'oggetto di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="74107-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="74107-112">In caso contrario, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="74107-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="74107-113">*PHR*</span><span class="sxs-lookup"><span data-stu-id="74107-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="74107-114">Puntatore a una variabile che riceve un valore **HRESULT** che indica l'esito positivo o negativo del metodo.</span><span class="sxs-lookup"><span data-stu-id="74107-114">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="74107-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74107-115">Requirements</span></span>



| <span data-ttu-id="74107-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="74107-116">Requirement</span></span> | <span data-ttu-id="74107-117">Valore</span><span class="sxs-lookup"><span data-stu-id="74107-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74107-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="74107-118">Header</span></span><br/>  | <dl> <span data-ttu-id="74107-119"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74107-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="74107-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="74107-120">Library</span></span><br/> | <dl> <span data-ttu-id="74107-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="74107-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74107-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74107-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74107-123">**Classe CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="74107-123">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




