---
description: 'Metodo CBasePin.CompleteConnect: il metodo CompleteConnect completa una connessione a un altro pin.'
ms.assetid: 10cbf29c-2e1a-419c-b0c0-c99f9a285810
title: Metodo CBasePin.CompleteConnect (Amfilter.h)
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
ms.openlocfilehash: fee207d7a17f12cc81036fbd4f82ec49a99f4a31
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096039"
---
# <a name="cbasepincompleteconnect-method"></a><span data-ttu-id="f44dd-103">Metodo CBasePin.CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="f44dd-103">CBasePin.CompleteConnect method</span></span>

<span data-ttu-id="f44dd-104">Il `CompleteConnect` metodo completa una connessione a un altro pin.</span><span class="sxs-lookup"><span data-stu-id="f44dd-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="f44dd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f44dd-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="f44dd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f44dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f44dd-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="f44dd-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="f44dd-108">Puntatore all'interfaccia [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) dell'altro pin.</span><span class="sxs-lookup"><span data-stu-id="f44dd-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f44dd-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f44dd-109">Return value</span></span>

<span data-ttu-id="f44dd-110">Restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f44dd-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f44dd-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="f44dd-111">Remarks</span></span>

<span data-ttu-id="f44dd-112">Questo metodo viene chiamato su entrambi i pin alla fine del processo di connessione.</span><span class="sxs-lookup"><span data-stu-id="f44dd-112">This method is called on both pins at the end of the connection process.</span></span> <span data-ttu-id="f44dd-113">Il pin di connessione lo chiama dall'interno del metodo [**CBasePin::Connect**](cbasepin-connect.md) e il pin ricevente lo chiama dall'interno del metodo [**CBasePin::ReceiveConnection.**](cbasepin-receiveconnection.md)</span><span class="sxs-lookup"><span data-stu-id="f44dd-113">The connecting pin calls it from within the [**CBasePin::Connect**](cbasepin-connect.md) method, and the receiving pin calls it from within the [**CBasePin::ReceiveConnection**](cbasepin-receiveconnection.md) method.</span></span>

<span data-ttu-id="f44dd-114">Nella classe di base questo metodo restituisce semplicemente S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f44dd-114">In the base class, this method simply returns S\_OK.</span></span> <span data-ttu-id="f44dd-115">Se una classe derivata ha requisiti per il completamento di una connessione, deve eseguire l'override di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="f44dd-115">If a derived class has any requirements for completing a connection, it should override this method.</span></span> <span data-ttu-id="f44dd-116">Ad esempio, la [**classe CBaseOutputPin**](cbaseoutputpin.md) usa questo metodo per decidere l'allocatore di memoria.</span><span class="sxs-lookup"><span data-stu-id="f44dd-116">For example, the [**CBaseOutputPin**](cbaseoutputpin.md) class uses this method to decide the memory allocator.</span></span>

<span data-ttu-id="f44dd-117">Se questo metodo ha esito negativo, anche il tentativo di connessione complessivo ha esito negativo e il pin si disconnette dal pin ricevente.</span><span class="sxs-lookup"><span data-stu-id="f44dd-117">If this method fails, the overall connection attempt also fails, and the pin disconnects from the receiving pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="f44dd-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f44dd-118">Requirements</span></span>



| <span data-ttu-id="f44dd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f44dd-119">Requirement</span></span> | <span data-ttu-id="f44dd-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f44dd-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f44dd-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f44dd-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f44dd-122"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="f44dd-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f44dd-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="f44dd-123">Library</span></span><br/> | <dl> <span data-ttu-id="f44dd-124"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f44dd-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f44dd-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f44dd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f44dd-126">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="f44dd-126">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




