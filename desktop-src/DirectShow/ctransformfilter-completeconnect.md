---
description: 'Metodo CTransformFilter.CompleteConnect: il metodo CompleteConnect completa una connessione pin.'
ms.assetid: b687d2ee-4aee-4fae-bc2f-23ee037d0e6d
title: Metodo CTransformFilter.CompleteConnect (Transfrm.h)
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
ms.openlocfilehash: d2251ba45c7a39ec9bf205fdd6643e02392e40e5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095169"
---
# <a name="ctransformfiltercompleteconnect-method"></a><span data-ttu-id="f8877-103">Metodo CTransformFilter.CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="f8877-103">CTransformFilter.CompleteConnect method</span></span>

<span data-ttu-id="f8877-104">Il `CompleteConnect` metodo completa una connessione pin.</span><span class="sxs-lookup"><span data-stu-id="f8877-104">The `CompleteConnect` method completes a pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8877-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8877-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="f8877-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8877-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8877-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="f8877-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="f8877-108">Membro del [**tipo enumerato PIN \_ DIRECTION,**](/windows/win32/api/strmif/ne-strmif-pin_direction) che specifica quale pin nel filtro sta effettuando la connessione.</span><span class="sxs-lookup"><span data-stu-id="f8877-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="f8877-109">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="f8877-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="f8877-110">Puntatore [**all'interfaccia IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) dell'altro pin in questo tentativo di connessione.</span><span class="sxs-lookup"><span data-stu-id="f8877-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8877-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f8877-111">Return value</span></span>

<span data-ttu-id="f8877-112">Restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f8877-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8877-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8877-113">Remarks</span></span>

<span data-ttu-id="f8877-114">I [**metodi CTransformInputPin::CompleteConnect**](ctransforminputpin-completeconnect.md) e [**CTransformOutputPin::CompleteConnect**](ctransformoutputpin-completeconnect.md) chiamano questo metodo durante il processo di connessione del pin.</span><span class="sxs-lookup"><span data-stu-id="f8877-114">The [**CTransformInputPin::CompleteConnect**](ctransforminputpin-completeconnect.md) and [**CTransformOutputPin::CompleteConnect**](ctransformoutputpin-completeconnect.md) methods call this method during the pin connection process.</span></span> <span data-ttu-id="f8877-115">Questo metodo non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.</span><span class="sxs-lookup"><span data-stu-id="f8877-115">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8877-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8877-116">Requirements</span></span>



| <span data-ttu-id="f8877-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8877-117">Requirement</span></span> | <span data-ttu-id="f8877-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f8877-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8877-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f8877-119">Header</span></span><br/>  | <dl> <span data-ttu-id="f8877-120"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8877-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f8877-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="f8877-121">Library</span></span><br/> | <dl> <span data-ttu-id="f8877-122"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f8877-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8877-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8877-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8877-124">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="f8877-124">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




