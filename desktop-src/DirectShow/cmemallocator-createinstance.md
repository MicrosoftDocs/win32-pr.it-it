---
description: Il metodo CreateInstance crea una nuova istanza della classe CMemAllocator.
ms.assetid: 87a831a4-2414-4240-8448-c5d90f130470
title: Metodo CMemAllocator. CreateInstance (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ef85de95db74e8a9d7aa6a7b1ba977620a29826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327443"
---
# <a name="cmemallocatorcreateinstance-method"></a><span data-ttu-id="f7b28-103">Metodo CMemAllocator. CreateInstance</span><span class="sxs-lookup"><span data-stu-id="f7b28-103">CMemAllocator.CreateInstance method</span></span>

<span data-ttu-id="f7b28-104">Il `CreateInstance` metodo crea una nuova istanza della classe **CMemAllocator** .</span><span class="sxs-lookup"><span data-stu-id="f7b28-104">The `CreateInstance` method creates a new instance of the **CMemAllocator** class.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7b28-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f7b28-105">Syntax</span></span>


```C++
static CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="f7b28-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7b28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7b28-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="f7b28-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="f7b28-108">Puntatore al proprietario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="f7b28-108">Pointer to the owner of this object.</span></span> <span data-ttu-id="f7b28-109">Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown** dell'oggetto di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="f7b28-109">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="f7b28-110">In caso contrario, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="f7b28-110">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f7b28-111">*PHR*</span><span class="sxs-lookup"><span data-stu-id="f7b28-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="f7b28-112">Puntatore a una variabile che riceve un valore **HRESULT** che indica l'esito positivo o negativo del metodo.</span><span class="sxs-lookup"><span data-stu-id="f7b28-112">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7b28-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f7b28-113">Return value</span></span>

<span data-ttu-id="f7b28-114">Restituisce un puntatore a un nuovo oggetto **CMemAllocator** , tipizzato come oggetto **CUnknown** .</span><span class="sxs-lookup"><span data-stu-id="f7b28-114">Returns a pointer to a new **CMemAllocator** object, typed as a **CUnknown** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7b28-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7b28-115">Requirements</span></span>



| <span data-ttu-id="f7b28-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7b28-116">Requirement</span></span> | <span data-ttu-id="f7b28-117">Valore</span><span class="sxs-lookup"><span data-stu-id="f7b28-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b28-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f7b28-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f7b28-119"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f7b28-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f7b28-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="f7b28-120">Library</span></span><br/> | <dl> <span data-ttu-id="f7b28-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f7b28-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7b28-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7b28-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7b28-123">**Classe CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="f7b28-123">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




