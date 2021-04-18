---
description: Il metodo CompleteConnect completa la connessione del PIN di input a un altro pin.
ms.assetid: 8dfc1a50-bc73-436a-a471-d8d3218410d3
title: Metodo CBaseRenderer. CompleteConnect (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9d2d35f99a3b3b8dc5b668b8ee9a9f94f0a53dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329393"
---
# <a name="cbaserenderercompleteconnect-method"></a><span data-ttu-id="5c80a-103">CBaseRenderer. CompleteConnect, metodo</span><span class="sxs-lookup"><span data-stu-id="5c80a-103">CBaseRenderer.CompleteConnect method</span></span>

<span data-ttu-id="5c80a-104">Il `CompleteConnect` metodo completa la connessione del PIN di input a un altro pin.</span><span class="sxs-lookup"><span data-stu-id="5c80a-104">The `CompleteConnect` method completes the input pin's connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c80a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c80a-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="5c80a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c80a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c80a-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="5c80a-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="5c80a-108">Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN di output.</span><span class="sxs-lookup"><span data-stu-id="5c80a-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c80a-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c80a-109">Return value</span></span>

<span data-ttu-id="5c80a-110">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5c80a-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c80a-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c80a-111">Remarks</span></span>

<span data-ttu-id="5c80a-112">Il pin di input del filtro chiama questo metodo dall'interno del proprio `CompleteConnect` metodo, che viene chiamato per completare una connessione del PIN.</span><span class="sxs-lookup"><span data-stu-id="5c80a-112">The filter's input pin calls this method from inside its own `CompleteConnect` method, which is called in order to complete a pin connection.</span></span> <span data-ttu-id="5c80a-113">Per ulteriori informazioni, vedere [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md). Il filtro chiama il metodo [**CBaseRenderer:: SetRepaintStatus**](cbaserenderer-setrepaintstatus.md) per abilitare gli eventi di [**\_ ridisegno EC**](ec-repaint.md) .</span><span class="sxs-lookup"><span data-stu-id="5c80a-113">(For more information, see [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md).) The filter calls the [**CBaseRenderer::SetRepaintStatus**](cbaserenderer-setrepaintstatus.md) method to enable [**EC\_REPAINT**](ec-repaint.md) events.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c80a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c80a-114">Requirements</span></span>



| <span data-ttu-id="5c80a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c80a-115">Requirement</span></span> | <span data-ttu-id="5c80a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="5c80a-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c80a-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c80a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5c80a-118"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5c80a-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5c80a-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="5c80a-119">Library</span></span><br/> | <dl> <span data-ttu-id="5c80a-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5c80a-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c80a-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c80a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c80a-122">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="5c80a-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




