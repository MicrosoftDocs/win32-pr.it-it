---
description: Metodo del costruttore.
ms.assetid: 94a92c1e-9768-4293-8290-a2b1938cd196
title: Costruttore CSource. CSource (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.CSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 992775659d5f9838ef63b15c5395998f1faf6200
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324655"
---
# <a name="csourcecsource-constructor"></a><span data-ttu-id="09b67-103">Costruttore CSource. CSource</span><span class="sxs-lookup"><span data-stu-id="09b67-103">CSource.CSource constructor</span></span>

<span data-ttu-id="09b67-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="09b67-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="09b67-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09b67-105">Syntax</span></span>


```C++
CSource(
   TCHAR     *pName,
   LPUNKNOWN lpunk,
   CLSID     clsid
);
```



## <a name="parameters"></a><span data-ttu-id="09b67-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="09b67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09b67-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="09b67-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="09b67-108">Puntatore a una stringa che contiene il nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="09b67-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="09b67-109">Per ulteriori informazioni, vedere [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="09b67-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="09b67-110">*lpunk*</span><span class="sxs-lookup"><span data-stu-id="09b67-110">*lpunk*</span></span> 
</dt> <dd>

<span data-ttu-id="09b67-111">Puntatore al proprietario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="09b67-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="09b67-112">Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown** dell'oggetto di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="09b67-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="09b67-113">In caso contrario, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="09b67-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="09b67-114">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="09b67-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="09b67-115">Identificatore di classe del filtro.</span><span class="sxs-lookup"><span data-stu-id="09b67-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="09b67-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09b67-116">Requirements</span></span>



| <span data-ttu-id="09b67-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="09b67-117">Requirement</span></span> | <span data-ttu-id="09b67-118">Valore</span><span class="sxs-lookup"><span data-stu-id="09b67-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09b67-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="09b67-119">Header</span></span><br/>  | <dl> <span data-ttu-id="09b67-120"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09b67-120"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="09b67-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="09b67-121">Library</span></span><br/> | <dl> <span data-ttu-id="09b67-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="09b67-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09b67-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09b67-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09b67-124">**Classe CSource**</span><span class="sxs-lookup"><span data-stu-id="09b67-124">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




