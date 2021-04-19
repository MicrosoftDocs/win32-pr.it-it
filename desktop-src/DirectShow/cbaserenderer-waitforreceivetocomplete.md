---
description: 'Il metodo WaitForReceiveToComplete attende il completamento del metodo CBaseRenderer:: Receive.'
ms.assetid: 3c722680-e54b-4ba1-8e98-36647cd027bc
title: Metodo CBaseRenderer. WaitForReceiveToComplete (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForReceiveToComplete
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9033474c71d23fed106205839071bad200df6a23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324197"
---
# <a name="cbaserendererwaitforreceivetocomplete-method"></a><span data-ttu-id="4132c-103">CBaseRenderer. WaitForReceiveToComplete, metodo</span><span class="sxs-lookup"><span data-stu-id="4132c-103">CBaseRenderer.WaitForReceiveToComplete method</span></span>

<span data-ttu-id="4132c-104">Il `WaitForReceiveToComplete` metodo attende il completamento del metodo [**CBaseRenderer:: Receive**](cbaserenderer-receive.md) .</span><span class="sxs-lookup"><span data-stu-id="4132c-104">The `WaitForReceiveToComplete` method waits for the [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method to complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="4132c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4132c-105">Syntax</span></span>


```C++
void WaitForReceiveToComplete();
```



## <a name="parameters"></a><span data-ttu-id="4132c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4132c-106">Parameters</span></span>

<span data-ttu-id="4132c-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="4132c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4132c-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4132c-108">Return value</span></span>

<span data-ttu-id="4132c-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="4132c-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4132c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="4132c-110">Remarks</span></span>

<span data-ttu-id="4132c-111">I metodi [**CBaseRenderer:: Stop**](cbaserenderer-stop.md) e [**CBaseRenderer:: BeginFlush**](cbaserenderer-beginflush.md) chiamano questo metodo per sincronizzare la modifica dello stato con il metodo **Receive** .</span><span class="sxs-lookup"><span data-stu-id="4132c-111">The [**CBaseRenderer::Stop**](cbaserenderer-stop.md) and [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) methods call this method to synchronize the state change with the **Receive** method.</span></span>

<span data-ttu-id="4132c-112">In particolare, questo metodo invia i messaggi mentre è in attesa che il flag [**\_ BInReceive di CBaseRenderer:: m**](cbaserenderer-m-binreceive.md) diventi **false**.</span><span class="sxs-lookup"><span data-stu-id="4132c-112">Specifically, this method dispatches messages while it waits for the [**CBaseRenderer::m\_bInReceive**](cbaserenderer-m-binreceive.md) flag to become **FALSE**.</span></span> <span data-ttu-id="4132c-113">Il flag diventa **true** nel metodo [**CBaseRenderer::P reparereceive**](cbaserenderer-preparereceive.md) e ritorna a **false** dopo che il metodo **Receive** chiama il metodo [**CBaseRenderer::P reparerender**](cbaserenderer-preparerender.md) .</span><span class="sxs-lookup"><span data-stu-id="4132c-113">The flag becomes **TRUE** in the [**CBaseRenderer::PrepareReceive**](cbaserenderer-preparereceive.md) method and switches back to **FALSE** after the **Receive** method calls the [**CBaseRenderer::PrepareRender**](cbaserenderer-preparerender.md) method.</span></span> <span data-ttu-id="4132c-114">La classe derivata può utilizzare **PrepareRender** per impostare la tavolozza.</span><span class="sxs-lookup"><span data-stu-id="4132c-114">The derived class can use **PrepareRender** to set the palette.</span></span> <span data-ttu-id="4132c-115">In attesa del completamento di **PrepareRender** si garantisce che i messaggi di modifica della tavolozza vengano inviati prima che si verifichi la modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="4132c-115">Waiting for **PrepareRender** to complete ensures that palette-change messages are dispatched before the state change occurs.</span></span> <span data-ttu-id="4132c-116">In questo modo si evita un potenziale deadlock.</span><span class="sxs-lookup"><span data-stu-id="4132c-116">This avoids a potential deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="4132c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4132c-117">Requirements</span></span>



| <span data-ttu-id="4132c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4132c-118">Requirement</span></span> | <span data-ttu-id="4132c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="4132c-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4132c-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4132c-120">Header</span></span><br/>  | <dl> <span data-ttu-id="4132c-121"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4132c-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4132c-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="4132c-122">Library</span></span><br/> | <dl> <span data-ttu-id="4132c-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4132c-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4132c-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4132c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4132c-125">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="4132c-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




