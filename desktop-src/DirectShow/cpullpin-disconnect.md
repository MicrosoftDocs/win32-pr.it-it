---
description: Il metodo Disconnect interrompe la connessione con il pin di output.
ms.assetid: 6e362e32-7b74-4392-b46f-1ab47a30a07b
title: Metodo CPullPin. Disconnect (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec13a7f29a06bab4f79ddb58932796f8363adadc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331175"
---
# <a name="cpullpindisconnect-method"></a><span data-ttu-id="58ebd-103">Metodo CPullPin. Disconnect</span><span class="sxs-lookup"><span data-stu-id="58ebd-103">CPullPin.Disconnect method</span></span>

<span data-ttu-id="58ebd-104">Il `Disconnect` metodo interrompe la connessione con il pin di output.</span><span class="sxs-lookup"><span data-stu-id="58ebd-104">The `Disconnect` method breaks the connection with the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="58ebd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58ebd-105">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="58ebd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="58ebd-106">Parameters</span></span>

<span data-ttu-id="58ebd-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="58ebd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="58ebd-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58ebd-108">Return value</span></span>

<span data-ttu-id="58ebd-109">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="58ebd-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="58ebd-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="58ebd-110">Remarks</span></span>

<span data-ttu-id="58ebd-111">Questo metodo interrompe qualsiasi connessione eseguita nel metodo [**CPullPin:: Connect**](cpullpin-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="58ebd-111">This method breaks any connection made in the [**CPullPin::Connect**](cpullpin-connect.md) method.</span></span> <span data-ttu-id="58ebd-112">Chiamare questo metodo all'interno del metodo [**Ipin::D la connessione**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .</span><span class="sxs-lookup"><span data-stu-id="58ebd-112">Call this method inside your [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span> <span data-ttu-id="58ebd-113">Se il pin deriva da [**CBasePin**](cbasepin.md), eseguire l'override di [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) per chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="58ebd-113">(If your pin derives from [**CBasePin**](cbasepin.md), override [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) to call this method.)</span></span>

## <a name="requirements"></a><span data-ttu-id="58ebd-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58ebd-114">Requirements</span></span>



| <span data-ttu-id="58ebd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="58ebd-115">Requirement</span></span> | <span data-ttu-id="58ebd-116">Valore</span><span class="sxs-lookup"><span data-stu-id="58ebd-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58ebd-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58ebd-117">Header</span></span><br/>  | <dl> <span data-ttu-id="58ebd-118"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="58ebd-118"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="58ebd-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="58ebd-119">Library</span></span><br/> | <dl> <span data-ttu-id="58ebd-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="58ebd-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58ebd-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58ebd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58ebd-122">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="58ebd-122">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




