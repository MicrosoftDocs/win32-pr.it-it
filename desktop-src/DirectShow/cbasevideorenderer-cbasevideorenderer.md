---
description: Metodo del costruttore.
ms.assetid: 9b69632b-7932-4a9b-bd68-69b06dd8a5ec
title: Costruttore CBaseVideoRenderer. CBaseVideoRenderer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.CBaseVideoRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27ed49be63d9c2c05e12a2ac92ae33f64705460b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328509"
---
# <a name="cbasevideorenderercbasevideorenderer-constructor"></a><span data-ttu-id="8e0b3-103">Costruttore CBaseVideoRenderer. CBaseVideoRenderer</span><span class="sxs-lookup"><span data-stu-id="8e0b3-103">CBaseVideoRenderer.CBaseVideoRenderer constructor</span></span>

<span data-ttu-id="8e0b3-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="8e0b3-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e0b3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e0b3-105">Syntax</span></span>


```C++
CBaseVideoRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="8e0b3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e0b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e0b3-107">*RenderClass*</span><span class="sxs-lookup"><span data-stu-id="8e0b3-107">*RenderClass*</span></span> 
</dt> <dd>

<span data-ttu-id="8e0b3-108">Identificatore di classe per questo renderer.</span><span class="sxs-lookup"><span data-stu-id="8e0b3-108">Class identifier for this renderer.</span></span>

</dd> <dt>

<span data-ttu-id="8e0b3-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="8e0b3-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="8e0b3-110">Puntatore a una descrizione utilizzata a scopo di debug.</span><span class="sxs-lookup"><span data-stu-id="8e0b3-110">Pointer to a description used for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="8e0b3-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="8e0b3-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="8e0b3-112">Puntatore all'oggetto proprietario aggregato.</span><span class="sxs-lookup"><span data-stu-id="8e0b3-112">Pointer to the aggregated owner object.</span></span>

</dd> <dt>

<span data-ttu-id="8e0b3-113">*PHR*</span><span class="sxs-lookup"><span data-stu-id="8e0b3-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="8e0b3-114">Puntatore a un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8e0b3-114">Pointer to an **HRESULT** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8e0b3-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e0b3-115">Requirements</span></span>



| <span data-ttu-id="8e0b3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e0b3-116">Requirement</span></span> | <span data-ttu-id="8e0b3-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8e0b3-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e0b3-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e0b3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8e0b3-119"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8e0b3-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8e0b3-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="8e0b3-120">Library</span></span><br/> | <dl> <span data-ttu-id="8e0b3-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8e0b3-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e0b3-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e0b3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e0b3-123">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="8e0b3-123">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




