---
description: "Il metodo CompleteConnect completa una connessione a un pin di output. Questo metodo esegue l'override del Metodo CBasePin:: CompleteConnect."
ms.assetid: 32d95815-e018-4724-8cf3-8cd093ede517
title: Metodo CRendererInputPin. CompleteConnect (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e868693308d40fb786f201a9d7f056dd88326ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333191"
---
# <a name="crendererinputpincompleteconnect-method"></a><span data-ttu-id="a879f-104">CRendererInputPin. CompleteConnect, metodo</span><span class="sxs-lookup"><span data-stu-id="a879f-104">CRendererInputPin.CompleteConnect method</span></span>

<span data-ttu-id="a879f-105">Il `CompleteConnect` metodo completa una connessione a un pin di output.</span><span class="sxs-lookup"><span data-stu-id="a879f-105">The `CompleteConnect` method completes a connection to an output pin.</span></span> <span data-ttu-id="a879f-106">Questo metodo esegue l'override del metodo [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="a879f-106">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a879f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a879f-107">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="a879f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a879f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a879f-109">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="a879f-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="a879f-110">Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN di output</span><span class="sxs-lookup"><span data-stu-id="a879f-110">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a879f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a879f-111">Return value</span></span>

<span data-ttu-id="a879f-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a879f-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a879f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a879f-113">Requirements</span></span>



| <span data-ttu-id="a879f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a879f-114">Requirement</span></span> | <span data-ttu-id="a879f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a879f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a879f-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a879f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a879f-117"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a879f-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a879f-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="a879f-118">Library</span></span><br/> | <dl> <span data-ttu-id="a879f-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a879f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a879f-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a879f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a879f-121">**Classe CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="a879f-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




