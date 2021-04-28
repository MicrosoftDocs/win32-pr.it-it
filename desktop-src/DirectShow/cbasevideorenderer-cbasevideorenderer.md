---
description: Costruttore CBaseVideoRenderer.CBaseVideoRenderer - Metodo costruttore.
ms.assetid: 9b69632b-7932-4a9b-bd68-69b06dd8a5ec
title: Costruttore CBaseVideoRenderer.CBaseVideoRenderer (Renbase.h)
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
ms.openlocfilehash: c0ae558238b94402150e5cb15373d202065e485e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095839"
---
# <a name="cbasevideorenderercbasevideorenderer-constructor"></a><span data-ttu-id="62d8c-103">Costruttore CBaseVideoRenderer.CBaseVideoRenderer</span><span class="sxs-lookup"><span data-stu-id="62d8c-103">CBaseVideoRenderer.CBaseVideoRenderer constructor</span></span>

<span data-ttu-id="62d8c-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="62d8c-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="62d8c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62d8c-105">Syntax</span></span>


```C++
CBaseVideoRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="62d8c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="62d8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62d8c-107">*Classe RenderClass*</span><span class="sxs-lookup"><span data-stu-id="62d8c-107">*RenderClass*</span></span> 
</dt> <dd>

<span data-ttu-id="62d8c-108">Identificatore di classe per questo renderer.</span><span class="sxs-lookup"><span data-stu-id="62d8c-108">Class identifier for this renderer.</span></span>

</dd> <dt>

<span data-ttu-id="62d8c-109">*Pname*</span><span class="sxs-lookup"><span data-stu-id="62d8c-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="62d8c-110">Puntatore a una descrizione utilizzata a scopo di debug.</span><span class="sxs-lookup"><span data-stu-id="62d8c-110">Pointer to a description used for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="62d8c-111">*Punk*</span><span class="sxs-lookup"><span data-stu-id="62d8c-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="62d8c-112">Puntatore all'oggetto proprietario aggregato.</span><span class="sxs-lookup"><span data-stu-id="62d8c-112">Pointer to the aggregated owner object.</span></span>

</dd> <dt>

<span data-ttu-id="62d8c-113">*Phr*</span><span class="sxs-lookup"><span data-stu-id="62d8c-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="62d8c-114">Puntatore a un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="62d8c-114">Pointer to an **HRESULT** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="62d8c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62d8c-115">Requirements</span></span>



| <span data-ttu-id="62d8c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="62d8c-116">Requirement</span></span> | <span data-ttu-id="62d8c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="62d8c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62d8c-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62d8c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="62d8c-119"><dt>Renbase.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="62d8c-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="62d8c-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="62d8c-120">Library</span></span><br/> | <dl> <span data-ttu-id="62d8c-121"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="62d8c-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62d8c-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62d8c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62d8c-123">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="62d8c-123">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




