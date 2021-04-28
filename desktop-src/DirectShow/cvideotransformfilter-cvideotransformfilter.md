---
description: Costruttore CVideoTransformFilter.CVideoTransformFilter - Metodo costruttore.
ms.assetid: 4dad635f-4637-4f40-9f02-a91b59d05278
title: Costruttore CVideoTransformFilter.CVideoTransformFilter (Vtrans.h)
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
ms.openlocfilehash: 59609e09b252e56aded1669264bb98cdbe823e89
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084589"
---
# <a name="cvideotransformfiltercvideotransformfilter-constructor"></a><span data-ttu-id="3f741-103">Costruttore CVideoTransformFilter.CVideoTransformFilter</span><span class="sxs-lookup"><span data-stu-id="3f741-103">CVideoTransformFilter.CVideoTransformFilter constructor</span></span>

<span data-ttu-id="3f741-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="3f741-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f741-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f741-105">Syntax</span></span>


```C++
CVideoTransformFilter(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="3f741-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3f741-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f741-107">*Pname*</span><span class="sxs-lookup"><span data-stu-id="3f741-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="3f741-108">Stringa contenente il nome di debug del filtro.</span><span class="sxs-lookup"><span data-stu-id="3f741-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="3f741-109">Per altre informazioni, vedere [**CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="3f741-109">For more information, see [**CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="3f741-110">*Punk*</span><span class="sxs-lookup"><span data-stu-id="3f741-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="3f741-111">Puntatore al proprietario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="3f741-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="3f741-112">Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown dell'oggetto** di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="3f741-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="3f741-113">In caso contrario, impostare questo parametro su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="3f741-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3f741-114">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="3f741-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="3f741-115">Identificatore di classe del filtro.</span><span class="sxs-lookup"><span data-stu-id="3f741-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3f741-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f741-116">Requirements</span></span>



| <span data-ttu-id="3f741-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f741-117">Requirement</span></span> | <span data-ttu-id="3f741-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3f741-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f741-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3f741-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3f741-120"><dt>Vtrans.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f741-120"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3f741-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="3f741-121">Library</span></span><br/> | <dl> <span data-ttu-id="3f741-122"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3f741-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f741-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f741-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f741-124">**Classe CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="3f741-124">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




