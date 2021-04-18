---
description: Il metodo OnRenderStart viene chiamato quando il rendering sta per iniziare.
ms.assetid: 46af24cf-9075-4ebc-a49b-85f8f0c3da6f
title: Metodo CBaseRenderer. OnRenderStart (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7838b0ba43c1e570b745541882a2f2f815dd948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327957"
---
# <a name="cbaserendereronrenderstart-method"></a><span data-ttu-id="4696b-103">CBaseRenderer. OnRenderStart, metodo</span><span class="sxs-lookup"><span data-stu-id="4696b-103">CBaseRenderer.OnRenderStart method</span></span>

<span data-ttu-id="4696b-104">Il `OnRenderStart` metodo viene chiamato quando il rendering sta per iniziare.</span><span class="sxs-lookup"><span data-stu-id="4696b-104">The `OnRenderStart` method is called when rendering is about to start.</span></span>

## <a name="syntax"></a><span data-ttu-id="4696b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4696b-105">Syntax</span></span>


```C++
virtual void OnRenderStart(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="4696b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4696b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4696b-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="4696b-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="4696b-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="4696b-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4696b-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4696b-109">Return value</span></span>

<span data-ttu-id="4696b-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="4696b-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4696b-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="4696b-111">Remarks</span></span>

<span data-ttu-id="4696b-112">Il metodo [**CBaseRenderer:: Render**](cbaserenderer-render.md) chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="4696b-112">The [**CBaseRenderer::Render**](cbaserenderer-render.md) method calls this method.</span></span> <span data-ttu-id="4696b-113">Non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override. ad esempio, per raccogliere dati di controllo della qualità.</span><span class="sxs-lookup"><span data-stu-id="4696b-113">It does nothing in the base class, but the derived class can override it; for example, to collect quality-control data.</span></span>

## <a name="requirements"></a><span data-ttu-id="4696b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4696b-114">Requirements</span></span>



| <span data-ttu-id="4696b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4696b-115">Requirement</span></span> | <span data-ttu-id="4696b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4696b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4696b-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4696b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4696b-118"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4696b-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4696b-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="4696b-119">Library</span></span><br/> | <dl> <span data-ttu-id="4696b-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4696b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4696b-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4696b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4696b-122">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="4696b-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




