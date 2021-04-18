---
description: Il metodo CompleteConnect completa una connessione a un pin di input.
ms.assetid: 44c28c71-2c69-40ca-9bc4-c10394475a0f
title: Metodo CBaseOutputPin. CompleteConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4614e8531a21d88a1c2f4cfd75fcbe05a9210f13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329551"
---
# <a name="cbaseoutputpincompleteconnect-method"></a><span data-ttu-id="33a91-103">CBaseOutputPin. CompleteConnect, metodo</span><span class="sxs-lookup"><span data-stu-id="33a91-103">CBaseOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="33a91-104">Il `CompleteConnect` metodo completa una connessione a un pin di input.</span><span class="sxs-lookup"><span data-stu-id="33a91-104">The `CompleteConnect` method completes a connection to an input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="33a91-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="33a91-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="33a91-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="33a91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33a91-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="33a91-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="33a91-108">Puntatore al pin di input.</span><span class="sxs-lookup"><span data-stu-id="33a91-108">Pointer to the input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33a91-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="33a91-109">Return value</span></span>

<span data-ttu-id="33a91-110">Restituisce \_ OK se ha esito positivo o un valore **HRESULT** che indica la ragione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="33a91-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="33a91-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="33a91-111">Remarks</span></span>

<span data-ttu-id="33a91-112">Questo metodo esegue l'override del metodo [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="33a91-112">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span> <span data-ttu-id="33a91-113">Chiama il metodo [**DecideAllocator**](cbaseoutputpin-decideallocator.md) , che seleziona l'allocatore di memoria da usare per questa connessione.</span><span class="sxs-lookup"><span data-stu-id="33a91-113">It calls the [**DecideAllocator**](cbaseoutputpin-decideallocator.md) method, which selects the memory allocator to use for this connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="33a91-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33a91-114">Requirements</span></span>



| <span data-ttu-id="33a91-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="33a91-115">Requirement</span></span> | <span data-ttu-id="33a91-116">Valore</span><span class="sxs-lookup"><span data-stu-id="33a91-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33a91-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="33a91-117">Header</span></span><br/>  | <dl> <span data-ttu-id="33a91-118"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33a91-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="33a91-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="33a91-119">Library</span></span><br/> | <dl> <span data-ttu-id="33a91-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="33a91-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33a91-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33a91-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33a91-122">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="33a91-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




