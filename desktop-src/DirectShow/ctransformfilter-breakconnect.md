---
description: Il metodo BreakConnect rilascia un pin da una connessione.
ms.assetid: cc384786-9cba-4f68-9c60-740205b35661
title: Metodo CTransformFilter. BreakConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aec60322a4782d84e84dc2030b69f6c385783e98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325733"
---
# <a name="ctransformfilterbreakconnect-method"></a><span data-ttu-id="c2423-103">CTransformFilter. BreakConnect, metodo</span><span class="sxs-lookup"><span data-stu-id="c2423-103">CTransformFilter.BreakConnect method</span></span>

<span data-ttu-id="c2423-104">Il `BreakConnect` metodo rilascia un pin da una connessione.</span><span class="sxs-lookup"><span data-stu-id="c2423-104">The `BreakConnect` method releases a pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2423-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2423-105">Syntax</span></span>


```C++
virtual HRESULT BreakConnect(
   PIN_DIRECTION dir
);
```



## <a name="parameters"></a><span data-ttu-id="c2423-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2423-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2423-107">*dir*</span><span class="sxs-lookup"><span data-stu-id="c2423-107">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="c2423-108">Membro del tipo enumerato di [**\_ direzione del pin**](/windows/win32/api/strmif/ne-strmif-pin_direction) , che specifica quale connessione del PIN è stata interrotta (input o output).</span><span class="sxs-lookup"><span data-stu-id="c2423-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin connection was broken (input or output).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2423-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c2423-109">Return value</span></span>

<span data-ttu-id="c2423-110">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c2423-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2423-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2423-111">Remarks</span></span>

<span data-ttu-id="c2423-112">I metodi [**CTransformInputPin:: BreakConnect**](ctransforminputpin-breakconnect.md) e [**CTransformOutputPin:: BreakConnect**](ctransformoutputpin-breakconnect.md) chiamano questo metodo quando viene interruppe una connessione al pin.</span><span class="sxs-lookup"><span data-stu-id="c2423-112">The [**CTransformInputPin::BreakConnect**](ctransforminputpin-breakconnect.md) and [**CTransformOutputPin::BreakConnect**](ctransformoutputpin-breakconnect.md) methods call this method when a pin connection is broken.</span></span> <span data-ttu-id="c2423-113">Questo metodo non esegue alcuna operazione nella classe di base.</span><span class="sxs-lookup"><span data-stu-id="c2423-113">This method does nothing in the base class.</span></span> <span data-ttu-id="c2423-114">Se si esegue l'override del metodo [**CheckConnect**](ctransformfilter-checkconnect.md) , eseguire l'override di questo metodo per rilasciare tutte le risorse ottenute nel metodo **CheckConnect** , inclusi i puntatori di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="c2423-114">If you override the [**CheckConnect**](ctransformfilter-checkconnect.md) method, override this method to release any resources obtained in the **CheckConnect** method, including interface pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2423-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2423-115">Requirements</span></span>



| <span data-ttu-id="c2423-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2423-116">Requirement</span></span> | <span data-ttu-id="c2423-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c2423-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2423-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c2423-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c2423-119"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2423-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c2423-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="c2423-120">Library</span></span><br/> | <dl> <span data-ttu-id="c2423-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c2423-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2423-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2423-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2423-123">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="c2423-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




