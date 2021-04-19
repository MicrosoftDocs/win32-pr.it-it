---
description: Il metodo CompleteConnect completa una connessione a un altro pin.
ms.assetid: 10cbf29c-2e1a-419c-b0c0-c99f9a285810
title: Metodo CBasePin. CompleteConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9068bf63d3168a8c6d9e1bca2ef709f63e80a3c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332652"
---
# <a name="cbasepincompleteconnect-method"></a><span data-ttu-id="8a005-103">CBasePin. CompleteConnect, metodo</span><span class="sxs-lookup"><span data-stu-id="8a005-103">CBasePin.CompleteConnect method</span></span>

<span data-ttu-id="8a005-104">Il `CompleteConnect` metodo completa una connessione a un altro pin.</span><span class="sxs-lookup"><span data-stu-id="8a005-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a005-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a005-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="8a005-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8a005-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a005-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="8a005-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="8a005-108">Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) dell'altro pin.</span><span class="sxs-lookup"><span data-stu-id="8a005-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a005-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8a005-109">Return value</span></span>

<span data-ttu-id="8a005-110">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8a005-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a005-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a005-111">Remarks</span></span>

<span data-ttu-id="8a005-112">Questo metodo viene chiamato su entrambi i pin alla fine del processo di connessione.</span><span class="sxs-lookup"><span data-stu-id="8a005-112">This method is called on both pins at the end of the connection process.</span></span> <span data-ttu-id="8a005-113">Il pin di connessione lo chiama dall'interno del metodo [**CBasePin:: Connect**](cbasepin-connect.md) e il pin ricevente lo chiama dall'interno del metodo [**CBasePin:: ReceiveConnection**](cbasepin-receiveconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="8a005-113">The connecting pin calls it from within the [**CBasePin::Connect**](cbasepin-connect.md) method, and the receiving pin calls it from within the [**CBasePin::ReceiveConnection**](cbasepin-receiveconnection.md) method.</span></span>

<span data-ttu-id="8a005-114">Nella classe di base, questo metodo restituisce semplicemente S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8a005-114">In the base class, this method simply returns S\_OK.</span></span> <span data-ttu-id="8a005-115">Se una classe derivata presenta requisiti per il completamento di una connessione, deve eseguire l'override di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="8a005-115">If a derived class has any requirements for completing a connection, it should override this method.</span></span> <span data-ttu-id="8a005-116">Ad esempio, la classe [**CBaseOutputPin**](cbaseoutputpin.md) usa questo metodo per decidere l'allocatore di memoria.</span><span class="sxs-lookup"><span data-stu-id="8a005-116">For example, the [**CBaseOutputPin**](cbaseoutputpin.md) class uses this method to decide the memory allocator.</span></span>

<span data-ttu-id="8a005-117">Se questo metodo ha esito negativo, anche il tentativo di connessione complessiva ha esito negativo e il pin si disconnette dal pin di ricezione.</span><span class="sxs-lookup"><span data-stu-id="8a005-117">If this method fails, the overall connection attempt also fails, and the pin disconnects from the receiving pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a005-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a005-118">Requirements</span></span>



| <span data-ttu-id="8a005-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a005-119">Requirement</span></span> | <span data-ttu-id="8a005-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8a005-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a005-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8a005-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8a005-122"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8a005-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8a005-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="8a005-123">Library</span></span><br/> | <dl> <span data-ttu-id="8a005-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8a005-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a005-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a005-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a005-126">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="8a005-126">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




