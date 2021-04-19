---
description: Informazioni sul metodo del costruttore CMediaPosition. CMediaPosition (Ctlutil. h). Questo metodo usa i parametri "pName" e "pUnk".
ms.assetid: 18a7785c-30c6-43b8-9a41-542a8424522c
title: Costruttore CMediaPosition. CMediaPosition (Ctlutil. h)-pName, parametri pUnk
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
ms.openlocfilehash: e65f034e5f8857b21bc706bce45aa74c3c3cf966
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323785"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-parameters"></a><span data-ttu-id="7a45e-104">Costruttore CMediaPosition. CMediaPosition (Ctlutil. h)-pName, parametri pUnk</span><span class="sxs-lookup"><span data-stu-id="7a45e-104">CMediaPosition.CMediaPosition constructor (Ctlutil.h) - pName, pUnk parameters</span></span>

<span data-ttu-id="7a45e-105">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="7a45e-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a45e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a45e-106">Syntax</span></span>


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="7a45e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="7a45e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a45e-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="7a45e-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="7a45e-109">Puntatore al nome dell'oggetto, a scopo di debug.</span><span class="sxs-lookup"><span data-stu-id="7a45e-109">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="7a45e-110">Allocare questo parametro nella memoria statica.</span><span class="sxs-lookup"><span data-stu-id="7a45e-110">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="7a45e-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="7a45e-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="7a45e-112">Puntatore al proprietario di questo oggetto o **null** se l'oggetto non è aggregato.</span><span class="sxs-lookup"><span data-stu-id="7a45e-112">Pointer to the owner of this object, or **NULL** if the object is not aggregated.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a45e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a45e-113">Requirements</span></span>

| <span data-ttu-id="7a45e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a45e-114">Requirement</span></span> | <span data-ttu-id="7a45e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7a45e-115">Value</span></span> |
|-|-|
| <span data-ttu-id="7a45e-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a45e-116">Header</span></span> | <span data-ttu-id="7a45e-117">Ctlutil. h (include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="7a45e-117">Ctlutil.h (include Streams.h)</span></span> |
| <span data-ttu-id="7a45e-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="7a45e-118">Library</span></span>| <span data-ttu-id="7a45e-119">Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug)</span><span class="sxs-lookup"><span data-stu-id="7a45e-119">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="7a45e-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a45e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a45e-121">**Classe CMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="7a45e-121">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




