---
description: Il metodo CreateInstance crea un'istanza dell'oggetto. Questo metodo supporta la creazione dell'oggetto tramite un class factory. Per ulteriori informazioni, vedere CFactoryTemplate.
ms.assetid: 88dfa933-6fa1-4b57-8b0d-579233fa960c
title: Metodo CSeekingPassThru. CreateInstance (Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3640cbd6a0a3e582899e7f5cd349ca48498f3532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327839"
---
# <a name="cseekingpassthrucreateinstance-method"></a><span data-ttu-id="b8e0f-105">Metodo CSeekingPassThru. CreateInstance</span><span class="sxs-lookup"><span data-stu-id="b8e0f-105">CSeekingPassThru.CreateInstance method</span></span>

<span data-ttu-id="b8e0f-106">Il `CreateInstance` metodo crea un'istanza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b8e0f-106">The `CreateInstance` method creates an instance of the object.</span></span> <span data-ttu-id="b8e0f-107">Questo metodo supporta la creazione dell'oggetto tramite un class factory.</span><span class="sxs-lookup"><span data-stu-id="b8e0f-107">This method supports creation of the object through a class factory.</span></span> <span data-ttu-id="b8e0f-108">Per ulteriori informazioni, vedere [**CFactoryTemplate**](cfactorytemplate.md).</span><span class="sxs-lookup"><span data-stu-id="b8e0f-108">For more information, see [**CFactoryTemplate**](cfactorytemplate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b8e0f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8e0f-109">Syntax</span></span>


```C++
static CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="b8e0f-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b8e0f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8e0f-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="b8e0f-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="b8e0f-112">Puntatore al proprietario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="b8e0f-112">Pointer to the owner of this object.</span></span> <span data-ttu-id="b8e0f-113">Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown** dell'oggetto di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="b8e0f-113">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="b8e0f-114">In caso contrario, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="b8e0f-114">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b8e0f-115">*PHR*</span><span class="sxs-lookup"><span data-stu-id="b8e0f-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="b8e0f-116">Puntatore a un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b8e0f-116">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="b8e0f-117">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="b8e0f-117">Ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8e0f-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b8e0f-118">Return value</span></span>

<span data-ttu-id="b8e0f-119">Restituisce un puntatore a un nuovo oggetto **CSeekingPassThru** .</span><span class="sxs-lookup"><span data-stu-id="b8e0f-119">Returns a pointer to a new **CSeekingPassThru** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8e0f-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8e0f-120">Requirements</span></span>



| <span data-ttu-id="b8e0f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8e0f-121">Requirement</span></span> | <span data-ttu-id="b8e0f-122">Valore</span><span class="sxs-lookup"><span data-stu-id="b8e0f-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8e0f-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b8e0f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b8e0f-124"><dt>Seekpt. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8e0f-124"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b8e0f-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="b8e0f-125">Library</span></span><br/> | <dl> <span data-ttu-id="b8e0f-126"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b8e0f-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8e0f-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8e0f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8e0f-128">**Classe CSeekingPassThru**</span><span class="sxs-lookup"><span data-stu-id="b8e0f-128">**CSeekingPassThru Class**</span></span>](cseekingpassthru.md)
</dt> </dl>

 

 




