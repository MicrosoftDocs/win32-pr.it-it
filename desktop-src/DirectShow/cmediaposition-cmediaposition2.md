---
description: Informazioni sul metodo del costruttore CMediaPosition. CMediaPosition (Ctlutil. h). Questo metodo usa i parametri ' pName ',' pUnk ' è PHR '.
ms.assetid: 4074f513-d1e7-4311-8732-4d755e621e55
title: Costruttore CMediaPosition. CMediaPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb9d86a2403cd0e2e71130b51cdb87bad15c4e95
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323772"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-phr-parameters"></a><span data-ttu-id="5e85e-104">Costruttore CMediaPosition. CMediaPosition (Ctlutil. h)-pName, pUnk, PHR parametri</span><span class="sxs-lookup"><span data-stu-id="5e85e-104">CMediaPosition.CMediaPosition constructor (Ctlutil.h) - pName, pUnk, phr parameters</span></span>

<span data-ttu-id="5e85e-105">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="5e85e-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e85e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e85e-106">Syntax</span></span>


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="5e85e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5e85e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e85e-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="5e85e-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="5e85e-109">Puntatore al nome dell'oggetto, a scopo di debug.</span><span class="sxs-lookup"><span data-stu-id="5e85e-109">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="5e85e-110">Allocare questo parametro nella memoria statica.</span><span class="sxs-lookup"><span data-stu-id="5e85e-110">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="5e85e-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="5e85e-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="5e85e-112">Puntatore al proprietario di questo oggetto o **null** se l'oggetto non è aggregato.</span><span class="sxs-lookup"><span data-stu-id="5e85e-112">Pointer to the owner of this object, or **NULL** if the object is not aggregated.</span></span>

</dd> <dt>

<span data-ttu-id="5e85e-113">*PHR*</span><span class="sxs-lookup"><span data-stu-id="5e85e-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="5e85e-114">Puntatore a un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5e85e-114">Pointer to an **HRESULT** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5e85e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e85e-115">Requirements</span></span>

| <span data-ttu-id="5e85e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e85e-116">Requirement</span></span> | <span data-ttu-id="5e85e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5e85e-117">Value</span></span> |
|-|-|
| <span data-ttu-id="5e85e-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5e85e-118">Header</span></span> | <span data-ttu-id="5e85e-119">Ctlutil. h (include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="5e85e-119">Ctlutil.h (include Streams.h)</span></span> |
| <span data-ttu-id="5e85e-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="5e85e-120">Library</span></span>| <span data-ttu-id="5e85e-121">Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug)</span><span class="sxs-lookup"><span data-stu-id="5e85e-121">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="5e85e-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e85e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e85e-123">**Classe CMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="5e85e-123">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




