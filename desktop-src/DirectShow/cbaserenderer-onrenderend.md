---
description: Il metodo OnRenderEnd viene chiamato dopo il rendering di un campione.
ms.assetid: c9b3a3b2-a5c0-4a08-9e55-53c27a4d1032
title: Metodo CBaseRenderer. OnRenderEnd (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnRenderEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5859cf81a5fd0306f3470ee0fc6d54476e99833d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333350"
---
# <a name="cbaserendereronrenderend-method"></a><span data-ttu-id="300da-103">CBaseRenderer. OnRenderEnd, metodo</span><span class="sxs-lookup"><span data-stu-id="300da-103">CBaseRenderer.OnRenderEnd method</span></span>

<span data-ttu-id="300da-104">Il `OnRenderEnd` metodo viene chiamato dopo il rendering di un campione.</span><span class="sxs-lookup"><span data-stu-id="300da-104">The `OnRenderEnd` method is called after a sample is rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="300da-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="300da-105">Syntax</span></span>


```C++
virtual void OnRenderEnd(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="300da-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="300da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="300da-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="300da-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="300da-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="300da-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="300da-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="300da-109">Return value</span></span>

<span data-ttu-id="300da-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="300da-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="300da-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="300da-111">Remarks</span></span>

<span data-ttu-id="300da-112">Il metodo [**CBaseRenderer:: Render**](cbaserenderer-render.md) chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="300da-112">The [**CBaseRenderer::Render**](cbaserenderer-render.md) method calls this method.</span></span> <span data-ttu-id="300da-113">Non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override. ad esempio, per raccogliere dati di controllo della qualità.</span><span class="sxs-lookup"><span data-stu-id="300da-113">It does nothing in the base class, but the derived class can override it; for example, to collect quality-control data.</span></span>

## <a name="requirements"></a><span data-ttu-id="300da-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="300da-114">Requirements</span></span>



| <span data-ttu-id="300da-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="300da-115">Requirement</span></span> | <span data-ttu-id="300da-116">Valore</span><span class="sxs-lookup"><span data-stu-id="300da-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="300da-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="300da-117">Header</span></span><br/>  | <dl> <span data-ttu-id="300da-118"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="300da-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="300da-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="300da-119">Library</span></span><br/> | <dl> <span data-ttu-id="300da-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="300da-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="300da-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="300da-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="300da-122">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="300da-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




