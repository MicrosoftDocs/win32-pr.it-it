---
description: Il metodo TimerCallback è un metodo di callback per l'evento timer di fine flusso.
ms.assetid: ed43d07a-1ece-43ab-8753-ab14fa388946
title: Metodo CBaseRenderer. TimerCallback (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.TimerCallback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cfa59ca6bed0539caa7eb650458c168999b0de5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332989"
---
# <a name="cbaserenderertimercallback-method"></a><span data-ttu-id="2e065-103">CBaseRenderer. TimerCallback, metodo</span><span class="sxs-lookup"><span data-stu-id="2e065-103">CBaseRenderer.TimerCallback method</span></span>

<span data-ttu-id="2e065-104">Il `TimerCallback` metodo è un metodo di callback per l'evento timer di fine flusso.</span><span class="sxs-lookup"><span data-stu-id="2e065-104">The `TimerCallback` method is a callback method for the end-of-stream timer event.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e065-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e065-105">Syntax</span></span>


```C++
void TimerCallback();
```



## <a name="parameters"></a><span data-ttu-id="2e065-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e065-106">Parameters</span></span>

<span data-ttu-id="2e065-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="2e065-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2e065-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e065-108">Return value</span></span>

<span data-ttu-id="2e065-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="2e065-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e065-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e065-110">Remarks</span></span>

<span data-ttu-id="2e065-111">Il metodo [**CBaseRenderer:: SendEndOfStream**](cbaserenderer-sendendofstream.md) usa un evento timer per pianificare le \_ notifiche complete di EC.</span><span class="sxs-lookup"><span data-stu-id="2e065-111">The [**CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md) method uses a timer event to schedule EC\_COMPLETE notifications.</span></span> <span data-ttu-id="2e065-112">Il metodo **CBaseRenderer:: TimerCallback** è la funzione di callback per l'evento del timer.</span><span class="sxs-lookup"><span data-stu-id="2e065-112">The **CBaseRenderer::TimerCallback** method is the callback function for the timer event.</span></span> <span data-ttu-id="2e065-113">Il `TimerCallback` metodo chiama di nuovo **SendEndOfStream** e **SendEndOfStream** determina se inviare la notifica di \_ completamento EC o impostare un altro timer.</span><span class="sxs-lookup"><span data-stu-id="2e065-113">The `TimerCallback` method calls **SendEndOfStream** again, and **SendEndOfStream** determines whether to send the EC\_COMPLETE notification or set another timer.</span></span>

<span data-ttu-id="2e065-114">Il metodo [**CBaseRenderer:: ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md) Annulla l'evento del timer.</span><span class="sxs-lookup"><span data-stu-id="2e065-114">The [**CBaseRenderer::ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md) method cancels the timer event.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e065-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e065-115">Requirements</span></span>



| <span data-ttu-id="2e065-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e065-116">Requirement</span></span> | <span data-ttu-id="2e065-117">Valore</span><span class="sxs-lookup"><span data-stu-id="2e065-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e065-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2e065-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2e065-119"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2e065-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2e065-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="2e065-120">Library</span></span><br/> | <dl> <span data-ttu-id="2e065-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2e065-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e065-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e065-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e065-123">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="2e065-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




