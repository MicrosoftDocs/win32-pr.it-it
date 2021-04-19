---
description: Il metodo PrepareRender viene chiamato prima che il filtro esegua il rendering di un campione.
ms.assetid: 0b137da9-eac0-469f-b457-719a36569c82
title: Metodo CBaseRenderer. PrepareRender (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.PrepareRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee5739a839222900458ae334de6f97fb6d18876b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333340"
---
# <a name="cbaserendererpreparerender-method"></a><span data-ttu-id="5d829-103">CBaseRenderer. PrepareRender, metodo</span><span class="sxs-lookup"><span data-stu-id="5d829-103">CBaseRenderer.PrepareRender method</span></span>

<span data-ttu-id="5d829-104">Il `PrepareRender` metodo viene chiamato prima che il filtro esegua il rendering di un campione.</span><span class="sxs-lookup"><span data-stu-id="5d829-104">The `PrepareRender` method is called before the filter renders a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d829-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5d829-105">Syntax</span></span>


```C++
virtual void PrepareRender();
```



## <a name="parameters"></a><span data-ttu-id="5d829-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5d829-106">Parameters</span></span>

<span data-ttu-id="5d829-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="5d829-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5d829-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5d829-108">Return value</span></span>

<span data-ttu-id="5d829-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="5d829-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d829-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="5d829-110">Remarks</span></span>

<span data-ttu-id="5d829-111">Il filtro chiama questo metodo prima di chiamare il metodo [**CBaseRenderer:: OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md) o il metodo [**CBaseRenderer:: Render**](cbaserenderer-render.md) .</span><span class="sxs-lookup"><span data-stu-id="5d829-111">The filter calls this method before it calls the [**CBaseRenderer::OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md) method or the [**CBaseRenderer::Render**](cbaserenderer-render.md) method.</span></span> <span data-ttu-id="5d829-112">`PrepareRender` non esegue alcuna operazione nella classe di base.</span><span class="sxs-lookup"><span data-stu-id="5d829-112">`PrepareRender` does not do anything in the base class.</span></span> <span data-ttu-id="5d829-113">La classe derivata può eseguire l'override di questa classe per eseguire le azioni necessarie prima del rendering.</span><span class="sxs-lookup"><span data-stu-id="5d829-113">The derived class can override it to perform any actions required before rendering.</span></span> <span data-ttu-id="5d829-114">Un renderer video, ad esempio, può eseguire l'override di questo metodo per realizzare la relativa tavolozza.</span><span class="sxs-lookup"><span data-stu-id="5d829-114">For example, a video renderer can override this method to realize its palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d829-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d829-115">Requirements</span></span>



| <span data-ttu-id="5d829-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d829-116">Requirement</span></span> | <span data-ttu-id="5d829-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5d829-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d829-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5d829-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5d829-119"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d829-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5d829-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="5d829-120">Library</span></span><br/> | <dl> <span data-ttu-id="5d829-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5d829-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d829-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5d829-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d829-123">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="5d829-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




