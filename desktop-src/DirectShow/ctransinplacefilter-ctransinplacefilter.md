---
description: Metodo del costruttore.
ms.assetid: f0d30125-5d16-470c-a5fb-a7df96814dad
title: Costruttore CTransInPlaceFilter. CTransInPlaceFilter (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CTransInPlaceFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 091ea6e6a52d4cc9221ddb29db34b4823111a395
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332974"
---
# <a name="ctransinplacefilterctransinplacefilter-constructor"></a><span data-ttu-id="6c945-103">Costruttore CTransInPlaceFilter. CTransInPlaceFilter</span><span class="sxs-lookup"><span data-stu-id="6c945-103">CTransInPlaceFilter.CTransInPlaceFilter constructor</span></span>

<span data-ttu-id="6c945-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="6c945-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c945-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c945-105">Syntax</span></span>


```C++
CTransInPlaceFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   REFCLSID  clsid,
   HRESULT   *phr,
   bool      bModifiesData = TRUE
);
```



## <a name="parameters"></a><span data-ttu-id="6c945-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c945-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c945-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="6c945-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="6c945-108">Stringa contenente il nome di debug del filtro.</span><span class="sxs-lookup"><span data-stu-id="6c945-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="6c945-109">Per ulteriori informazioni, vedere [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="6c945-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c945-110">*lpUnk*</span><span class="sxs-lookup"><span data-stu-id="6c945-110">*lpUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="6c945-111">Puntatore al proprietario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="6c945-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="6c945-112">Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown** dell'oggetto di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="6c945-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="6c945-113">In caso contrario, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="6c945-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6c945-114">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="6c945-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="6c945-115">Identificatore di classe del filtro.</span><span class="sxs-lookup"><span data-stu-id="6c945-115">Class identifier of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="6c945-116">*PHR*</span><span class="sxs-lookup"><span data-stu-id="6c945-116">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="6c945-117">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="6c945-117">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="6c945-118">*bModifiesData*</span><span class="sxs-lookup"><span data-stu-id="6c945-118">*bModifiesData*</span></span> 
</dt> <dd>

<span data-ttu-id="6c945-119">Valore booleano che specifica se il filtro modifica i dati di input.</span><span class="sxs-lookup"><span data-stu-id="6c945-119">Boolean value that specifies whether the filter modifies the input data.</span></span> <span data-ttu-id="6c945-120">Se **true**, il filtro modifica i dati.</span><span class="sxs-lookup"><span data-stu-id="6c945-120">If **TRUE**, the filter modifies the data.</span></span> <span data-ttu-id="6c945-121">In caso contrario, il filtro passa i dati a valle invariati.</span><span class="sxs-lookup"><span data-stu-id="6c945-121">Otherwise, the filter passes the data downstream unchanged.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c945-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c945-122">Requirements</span></span>



| <span data-ttu-id="6c945-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c945-123">Requirement</span></span> | <span data-ttu-id="6c945-124">Valore</span><span class="sxs-lookup"><span data-stu-id="6c945-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c945-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6c945-125">Header</span></span><br/>  | <dl> <span data-ttu-id="6c945-126"><dt>Transip. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c945-126"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6c945-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="6c945-127">Library</span></span><br/> | <dl> <span data-ttu-id="6c945-128"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6c945-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c945-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c945-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c945-130">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="6c945-130">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




