---
description: Il metodo CompleteConnect completa una connessione pin.
ms.assetid: b687d2ee-4aee-4fae-bc2f-23ee037d0e6d
title: Metodo CTransformFilter. CompleteConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 630950cf9b05c08412394bf9270f2369b3f3b94b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329150"
---
# <a name="ctransformfiltercompleteconnect-method"></a><span data-ttu-id="5bf3a-103">CTransformFilter. CompleteConnect, metodo</span><span class="sxs-lookup"><span data-stu-id="5bf3a-103">CTransformFilter.CompleteConnect method</span></span>

<span data-ttu-id="5bf3a-104">Il `CompleteConnect` metodo completa una connessione pin.</span><span class="sxs-lookup"><span data-stu-id="5bf3a-104">The `CompleteConnect` method completes a pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bf3a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5bf3a-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="5bf3a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5bf3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bf3a-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="5bf3a-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="5bf3a-108">Membro del tipo enumerato di [**\_ direzione del pin**](/windows/win32/api/strmif/ne-strmif-pin_direction) , che specifica quale pin del filtro sta effettuando la connessione.</span><span class="sxs-lookup"><span data-stu-id="5bf3a-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="5bf3a-109">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="5bf3a-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="5bf3a-110">Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) dell'altro pin in questo tentativo di connessione.</span><span class="sxs-lookup"><span data-stu-id="5bf3a-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bf3a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5bf3a-111">Return value</span></span>

<span data-ttu-id="5bf3a-112">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5bf3a-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bf3a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="5bf3a-113">Remarks</span></span>

<span data-ttu-id="5bf3a-114">I metodi [**CTransformInputPin:: CompleteConnect**](ctransforminputpin-completeconnect.md) e [**CTransformOutputPin:: CompleteConnect**](ctransformoutputpin-completeconnect.md) chiamano questo metodo durante il processo di connessione del PIN.</span><span class="sxs-lookup"><span data-stu-id="5bf3a-114">The [**CTransformInputPin::CompleteConnect**](ctransforminputpin-completeconnect.md) and [**CTransformOutputPin::CompleteConnect**](ctransformoutputpin-completeconnect.md) methods call this method during the pin connection process.</span></span> <span data-ttu-id="5bf3a-115">Questo metodo non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.</span><span class="sxs-lookup"><span data-stu-id="5bf3a-115">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bf3a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5bf3a-116">Requirements</span></span>



| <span data-ttu-id="5bf3a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bf3a-117">Requirement</span></span> | <span data-ttu-id="5bf3a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="5bf3a-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bf3a-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5bf3a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="5bf3a-120"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5bf3a-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5bf3a-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="5bf3a-121">Library</span></span><br/> | <dl> <span data-ttu-id="5bf3a-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5bf3a-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bf3a-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5bf3a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bf3a-124">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="5bf3a-124">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




