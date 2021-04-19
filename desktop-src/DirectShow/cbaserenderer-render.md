---
description: Il metodo Render esegue il rendering di un campione.
ms.assetid: 82b47777-2900-4821-ab79-1856da432832
title: Metodo CBaseRenderer. Render (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Render
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fefd44fe1b913fbba0e3ebfaa6f750b88d40813
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333332"
---
# <a name="cbaserendererrender-method"></a><span data-ttu-id="777e2-103">Metodo CBaseRenderer. Render</span><span class="sxs-lookup"><span data-stu-id="777e2-103">CBaseRenderer.Render method</span></span>

<span data-ttu-id="777e2-104">Il `Render` metodo esegue il rendering di un campione.</span><span class="sxs-lookup"><span data-stu-id="777e2-104">The `Render` method renders a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="777e2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="777e2-105">Syntax</span></span>


```C++
virtual Render(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="777e2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="777e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="777e2-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="777e2-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="777e2-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="777e2-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="777e2-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="777e2-109">Return value</span></span>

<span data-ttu-id="777e2-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="777e2-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="777e2-111">I valori possibili includono quelli nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="777e2-111">Possible values include those in the following table.</span></span>



| <span data-ttu-id="777e2-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="777e2-112">Return code</span></span>                                                                             | <span data-ttu-id="777e2-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="777e2-113">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="777e2-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="777e2-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="777e2-115">Il filtro è stato interrotto oppure *pMediaSample* è **null**.</span><span class="sxs-lookup"><span data-stu-id="777e2-115">The filter is stopped, or *pMediaSample* is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="777e2-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="777e2-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="777e2-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="777e2-117">Success.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="777e2-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="777e2-118">Remarks</span></span>

<span data-ttu-id="777e2-119">Questo metodo chiama il metodo virtuale pure [**CBaseRenderer::D orendersample**](cbaserenderer-dorendersample.md), che esegue le operazioni effettive.</span><span class="sxs-lookup"><span data-stu-id="777e2-119">This method calls the pure virtual method [**CBaseRenderer::DoRenderSample**](cbaserenderer-dorendersample.md), which does the real work.</span></span> <span data-ttu-id="777e2-120">La classe derivata deve implementare **DoRenderSample**.</span><span class="sxs-lookup"><span data-stu-id="777e2-120">The derived class must implement **DoRenderSample**.</span></span>

<span data-ttu-id="777e2-121">Immediatamente prima di chiamare **DoRenderSample**, questo metodo chiama il metodo [**CBaseRenderer:: OnRenderStart**](cbaserenderer-onrenderstart.md) .</span><span class="sxs-lookup"><span data-stu-id="777e2-121">Immediately before calling **DoRenderSample**, this method calls the [**CBaseRenderer::OnRenderStart**](cbaserenderer-onrenderstart.md) method.</span></span> <span data-ttu-id="777e2-122">Immediatamente dopo, viene chiamato il metodo [**CBaseRenderer:: OnRenderEnd**](cbaserenderer-onrenderend.md) .</span><span class="sxs-lookup"><span data-stu-id="777e2-122">Immediately after, it calls the [**CBaseRenderer::OnRenderEnd**](cbaserenderer-onrenderend.md) method.</span></span> <span data-ttu-id="777e2-123">La classe derivata può eseguire l'override di questi due metodi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="777e2-123">The derived class can override those two methods as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="777e2-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="777e2-124">Requirements</span></span>



| <span data-ttu-id="777e2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="777e2-125">Requirement</span></span> | <span data-ttu-id="777e2-126">Valore</span><span class="sxs-lookup"><span data-stu-id="777e2-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="777e2-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="777e2-127">Header</span></span><br/>  | <dl> <span data-ttu-id="777e2-128"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="777e2-128"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="777e2-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="777e2-129">Library</span></span><br/> | <dl> <span data-ttu-id="777e2-130"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="777e2-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="777e2-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="777e2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="777e2-132">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="777e2-132">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




