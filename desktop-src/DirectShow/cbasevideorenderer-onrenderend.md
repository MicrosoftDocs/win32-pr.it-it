---
description: Il metodo OnRenderEnd esegue una smussatura per i casi in cui il tempo di rendering varia a causa di interruzioni.
ms.assetid: 561b3306-0c41-4f04-b73a-78e7b4038e86
title: Metodo CBaseVideoRenderer. OnRenderEnd (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8f37b4d03f77090f4cac40a218fd3ac27c0c349d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324489"
---
# <a name="cbasevideorendereronrenderend-method"></a><span data-ttu-id="3c420-103">CBaseVideoRenderer. OnRenderEnd, metodo</span><span class="sxs-lookup"><span data-stu-id="3c420-103">CBaseVideoRenderer.OnRenderEnd method</span></span>

<span data-ttu-id="3c420-104">Il `OnRenderEnd` metodo esegue la smussatura per i casi in cui il tempo di rendering varia a causa di interruzioni.</span><span class="sxs-lookup"><span data-stu-id="3c420-104">The `OnRenderEnd` method performs smoothing for cases where the rendering time varies due to interruptions.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c420-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c420-105">Syntax</span></span>


```C++
void OnRenderEnd(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="3c420-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c420-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c420-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="3c420-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="3c420-108">Puntatore all'esempio di supporto.</span><span class="sxs-lookup"><span data-stu-id="3c420-108">Pointer to the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c420-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c420-109">Return value</span></span>

<span data-ttu-id="3c420-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="3c420-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c420-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c420-111">Remarks</span></span>

<span data-ttu-id="3c420-112">Questa funzione membro deve essere chiamata subito dopo il disegno di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="3c420-112">This member function should be called just after drawing an image.</span></span>

<span data-ttu-id="3c420-113">Questa funzione membro esegue l'override di [**CBaseRenderer:: OnRenderEnd**](cbaserenderer-onrenderend.md).</span><span class="sxs-lookup"><span data-stu-id="3c420-113">This member function overrides [**CBaseRenderer::OnRenderEnd**](cbaserenderer-onrenderend.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c420-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c420-114">Requirements</span></span>



| <span data-ttu-id="3c420-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c420-115">Requirement</span></span> | <span data-ttu-id="3c420-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3c420-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c420-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c420-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3c420-118"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c420-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3c420-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="3c420-119">Library</span></span><br/> | <dl> <span data-ttu-id="3c420-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3c420-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c420-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c420-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c420-122">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="3c420-122">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




