---
description: Il metodo OnRenderStart imposta le informazioni per il rendering.
ms.assetid: 698fe778-e2cb-4b87-a668-084b6c12c71f
title: Metodo CBaseVideoRenderer. OnRenderStart (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7327d25aafa6f6673b7ed70b658f675a9dab8f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325368"
---
# <a name="cbasevideorendereronrenderstart-method"></a><span data-ttu-id="2f9a9-103">CBaseVideoRenderer. OnRenderStart, metodo</span><span class="sxs-lookup"><span data-stu-id="2f9a9-103">CBaseVideoRenderer.OnRenderStart method</span></span>

<span data-ttu-id="2f9a9-104">Il `OnRenderStart` metodo imposta le informazioni per il rendering.</span><span class="sxs-lookup"><span data-stu-id="2f9a9-104">The `OnRenderStart` method sets information for rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f9a9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f9a9-105">Syntax</span></span>


```C++
void OnRenderStart(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="2f9a9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f9a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f9a9-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="2f9a9-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="2f9a9-108">Puntatore all'esempio di supporto.</span><span class="sxs-lookup"><span data-stu-id="2f9a9-108">Pointer to the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f9a9-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f9a9-109">Return value</span></span>

<span data-ttu-id="2f9a9-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="2f9a9-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f9a9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f9a9-111">Remarks</span></span>

<span data-ttu-id="2f9a9-112">Questa funzione membro recupera l'ora dell'orologio corrente dal sistema e la archivia in una variabile membro da utilizzare al termine del disegno.</span><span class="sxs-lookup"><span data-stu-id="2f9a9-112">This member function retrieves the current clock time from the system and stores it in a member variable to be used when the drawing is complete.</span></span> <span data-ttu-id="2f9a9-113">La funzione esegue anche la registrazione delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="2f9a9-113">The function also performs performance logging.</span></span> <span data-ttu-id="2f9a9-114">Questa funzione membro deve essere chiamata immediatamente prima dell'inizio del disegno.</span><span class="sxs-lookup"><span data-stu-id="2f9a9-114">This member function should be called just before drawing starts.</span></span>

<span data-ttu-id="2f9a9-115">Questa funzione membro esegue l'override di [**CBaseRenderer:: OnRenderStart**](cbaserenderer-onrenderstart.md).</span><span class="sxs-lookup"><span data-stu-id="2f9a9-115">This member function overrides [**CBaseRenderer::OnRenderStart**](cbaserenderer-onrenderstart.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f9a9-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f9a9-116">Requirements</span></span>



| <span data-ttu-id="2f9a9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f9a9-117">Requirement</span></span> | <span data-ttu-id="2f9a9-118">Valore</span><span class="sxs-lookup"><span data-stu-id="2f9a9-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f9a9-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2f9a9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="2f9a9-120"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f9a9-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2f9a9-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="2f9a9-121">Library</span></span><br/> | <dl> <span data-ttu-id="2f9a9-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2f9a9-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f9a9-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f9a9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f9a9-124">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="2f9a9-124">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




