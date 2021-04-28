---
description: Costruttore CMemAllocator.CMemAllocator - Metodo costruttore.
ms.assetid: 2340b39a-cab6-4524-b8cd-b22d4bdd24d0
title: Costruttore CMemAllocator.CMemAllocator (Amfilter.h)
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
ms.openlocfilehash: 1151572c32efe69cceb89e7a5ea5a045955b5f43
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095399"
---
# <a name="cmemallocatorcmemallocator-constructor"></a><span data-ttu-id="cc4c4-103">Costruttore CMemAllocator.CMemAllocator</span><span class="sxs-lookup"><span data-stu-id="cc4c4-103">CMemAllocator.CMemAllocator constructor</span></span>

<span data-ttu-id="cc4c4-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="cc4c4-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc4c4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cc4c4-105">Syntax</span></span>


```C++
CMemAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="cc4c4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cc4c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc4c4-107">*Pname*</span><span class="sxs-lookup"><span data-stu-id="cc4c4-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="cc4c4-108">Puntatore a una stringa contenente il nome dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="cc4c4-108">Pointer to a string containing the name of the allocator.</span></span>

</dd> <dt>

<span data-ttu-id="cc4c4-109">*Punk*</span><span class="sxs-lookup"><span data-stu-id="cc4c4-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="cc4c4-110">Puntatore al proprietario dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cc4c4-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="cc4c4-111">Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown dell'oggetto** di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="cc4c4-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="cc4c4-112">In caso contrario, impostare questo parametro su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="cc4c4-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cc4c4-113">*Phr*</span><span class="sxs-lookup"><span data-stu-id="cc4c4-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="cc4c4-114">Puntatore a una variabile che riceve un **valore HRESULT** che indica l'esito positivo o negativo del metodo.</span><span class="sxs-lookup"><span data-stu-id="cc4c4-114">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cc4c4-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc4c4-115">Requirements</span></span>



| <span data-ttu-id="cc4c4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc4c4-116">Requirement</span></span> | <span data-ttu-id="cc4c4-117">Valore</span><span class="sxs-lookup"><span data-stu-id="cc4c4-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc4c4-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cc4c4-118">Header</span></span><br/>  | <dl> <span data-ttu-id="cc4c4-119"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc4c4-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cc4c4-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="cc4c4-120">Library</span></span><br/> | <dl> <span data-ttu-id="cc4c4-121"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cc4c4-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc4c4-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc4c4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc4c4-123">**Classe CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="cc4c4-123">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




