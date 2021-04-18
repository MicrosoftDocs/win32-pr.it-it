---
description: Metodo del costruttore.
ms.assetid: 4dad635f-4637-4f40-9f02-a91b59d05278
title: Costruttore CVideoTransformFilter. CVideoTransformFilter (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.CVideoTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63e642182a0f968db5bda06e0af410d02455eb19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331442"
---
# <a name="cvideotransformfiltercvideotransformfilter-constructor"></a><span data-ttu-id="bb29a-103">Costruttore CVideoTransformFilter. CVideoTransformFilter</span><span class="sxs-lookup"><span data-stu-id="bb29a-103">CVideoTransformFilter.CVideoTransformFilter constructor</span></span>

<span data-ttu-id="bb29a-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="bb29a-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb29a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb29a-105">Syntax</span></span>


```C++
CVideoTransformFilter(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="bb29a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb29a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb29a-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="bb29a-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="bb29a-108">Stringa contenente il nome di debug del filtro.</span><span class="sxs-lookup"><span data-stu-id="bb29a-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="bb29a-109">Per ulteriori informazioni, vedere [**CBaseObject:: CBaseObject**](cbaseobject-cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="bb29a-109">For more information, see [**CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb29a-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="bb29a-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="bb29a-111">Puntatore al proprietario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="bb29a-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="bb29a-112">Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown** dell'oggetto di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="bb29a-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="bb29a-113">In caso contrario, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="bb29a-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bb29a-114">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="bb29a-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="bb29a-115">Identificatore di classe del filtro.</span><span class="sxs-lookup"><span data-stu-id="bb29a-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bb29a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb29a-116">Requirements</span></span>



| <span data-ttu-id="bb29a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb29a-117">Requirement</span></span> | <span data-ttu-id="bb29a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="bb29a-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb29a-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb29a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="bb29a-120"><dt>Vtrans. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb29a-120"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="bb29a-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="bb29a-121">Library</span></span><br/> | <dl> <span data-ttu-id="bb29a-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bb29a-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb29a-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb29a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb29a-124">**Classe CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="bb29a-124">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




