---
description: Metodo del costruttore.
ms.assetid: df5efbb3-6bce-4e30-b1b1-d69bf64fa87d
title: Costruttore CBaseRenderer. CBaseRenderer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CBaseRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b41f8d7f9681a64f58413aea2fd8717320278f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329402"
---
# <a name="cbaserenderercbaserenderer-constructor"></a><span data-ttu-id="0416e-103">Costruttore CBaseRenderer. CBaseRenderer</span><span class="sxs-lookup"><span data-stu-id="0416e-103">CBaseRenderer.CBaseRenderer constructor</span></span>

<span data-ttu-id="0416e-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="0416e-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0416e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0416e-105">Syntax</span></span>


```C++
CBaseRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   UINT      TimerResolution = 1
);
```



## <a name="parameters"></a><span data-ttu-id="0416e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0416e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0416e-107">*RenderClass*</span><span class="sxs-lookup"><span data-stu-id="0416e-107">*RenderClass*</span></span> 
</dt> <dd>

<span data-ttu-id="0416e-108">Identificatore di classe del renderer.</span><span class="sxs-lookup"><span data-stu-id="0416e-108">Class identifier of the renderer.</span></span>

</dd> <dt>

<span data-ttu-id="0416e-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="0416e-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="0416e-110">Puntatore a una stringa che contiene il nome del filtro, a scopo di debug.</span><span class="sxs-lookup"><span data-stu-id="0416e-110">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="0416e-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="0416e-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="0416e-112">Puntatore al proprietario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="0416e-112">Pointer to the owner of this object.</span></span> <span data-ttu-id="0416e-113">Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown** dell'oggetto di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="0416e-113">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="0416e-114">In caso contrario, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="0416e-114">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0416e-115">*PHR*</span><span class="sxs-lookup"><span data-stu-id="0416e-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="0416e-116">Riceve un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0416e-116">Receives an **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="0416e-117">*TimerResolution*</span><span class="sxs-lookup"><span data-stu-id="0416e-117">*TimerResolution*</span></span> 
</dt> <dd>

<span data-ttu-id="0416e-118">Risoluzione del timer.</span><span class="sxs-lookup"><span data-stu-id="0416e-118">Timer resolution.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0416e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0416e-119">Requirements</span></span>



| <span data-ttu-id="0416e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0416e-120">Requirement</span></span> | <span data-ttu-id="0416e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="0416e-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0416e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0416e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="0416e-123"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0416e-123"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0416e-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="0416e-124">Library</span></span><br/> | <dl> <span data-ttu-id="0416e-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0416e-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0416e-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0416e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0416e-127">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="0416e-127">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




