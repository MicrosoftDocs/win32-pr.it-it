---
description: Costruttore CBaseRenderer.CBaseRenderer - Metodo costruttore.
ms.assetid: df5efbb3-6bce-4e30-b1b1-d69bf64fa87d
title: Costruttore CBaseRenderer.CBaseRenderer (Renbase.h)
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
ms.openlocfilehash: 68ebc6255456f0fcbb4bf732a91dce981d0f78ce
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119909"
---
# <a name="cbaserenderercbaserenderer-constructor"></a><span data-ttu-id="443c8-103">Costruttore CBaseRenderer.CBaseRenderer</span><span class="sxs-lookup"><span data-stu-id="443c8-103">CBaseRenderer.CBaseRenderer constructor</span></span>

<span data-ttu-id="443c8-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="443c8-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="443c8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="443c8-105">Syntax</span></span>


```C++
CBaseRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   UINT      TimerResolution = 1
);
```



## <a name="parameters"></a><span data-ttu-id="443c8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="443c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="443c8-107">*Classe RenderClass*</span><span class="sxs-lookup"><span data-stu-id="443c8-107">*RenderClass*</span></span> 
</dt> <dd>

<span data-ttu-id="443c8-108">Identificatore di classe del renderer.</span><span class="sxs-lookup"><span data-stu-id="443c8-108">Class identifier of the renderer.</span></span>

</dd> <dt>

<span data-ttu-id="443c8-109">*Pname*</span><span class="sxs-lookup"><span data-stu-id="443c8-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="443c8-110">Puntatore a una stringa contenente il nome del filtro, a scopo di debug.</span><span class="sxs-lookup"><span data-stu-id="443c8-110">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="443c8-111">*Punk*</span><span class="sxs-lookup"><span data-stu-id="443c8-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="443c8-112">Puntatore al proprietario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="443c8-112">Pointer to the owner of this object.</span></span> <span data-ttu-id="443c8-113">Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown dell'oggetto** di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="443c8-113">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="443c8-114">In caso contrario, impostare questo parametro su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="443c8-114">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="443c8-115">*Phr*</span><span class="sxs-lookup"><span data-stu-id="443c8-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="443c8-116">Riceve un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="443c8-116">Receives an **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="443c8-117">*TimerResolution*</span><span class="sxs-lookup"><span data-stu-id="443c8-117">*TimerResolution*</span></span> 
</dt> <dd>

<span data-ttu-id="443c8-118">Risoluzione del timer.</span><span class="sxs-lookup"><span data-stu-id="443c8-118">Timer resolution.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="443c8-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="443c8-119">Requirements</span></span>



| <span data-ttu-id="443c8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="443c8-120">Requirement</span></span> | <span data-ttu-id="443c8-121">Valore</span><span class="sxs-lookup"><span data-stu-id="443c8-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="443c8-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="443c8-122">Header</span></span><br/>  | <dl> <span data-ttu-id="443c8-123"><dt>Renbase.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="443c8-123"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="443c8-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="443c8-124">Library</span></span><br/> | <dl> <span data-ttu-id="443c8-125"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="443c8-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="443c8-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="443c8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="443c8-127">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="443c8-127">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




