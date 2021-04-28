---
description: 'Metodo CBaseOutputPin.CompleteConnect: il metodo CompleteConnect completa una connessione a un pin di input.'
ms.assetid: 44c28c71-2c69-40ca-9bc4-c10394475a0f
title: Metodo CBaseOutputPin.CompleteConnect (Amfilter.h)
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
ms.openlocfilehash: cd4bc52db99b88c4d6f16c549fbb558bb6423730
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099539"
---
# <a name="cbaseoutputpincompleteconnect-method"></a><span data-ttu-id="c332c-103">Metodo CBaseOutputPin.CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="c332c-103">CBaseOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="c332c-104">Il `CompleteConnect` metodo completa una connessione a un pin di input.</span><span class="sxs-lookup"><span data-stu-id="c332c-104">The `CompleteConnect` method completes a connection to an input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="c332c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c332c-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="c332c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c332c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c332c-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="c332c-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="c332c-108">Puntatore al pin di input.</span><span class="sxs-lookup"><span data-stu-id="c332c-108">Pointer to the input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c332c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c332c-109">Return value</span></span>

<span data-ttu-id="c332c-110">Restituisce S OK in caso di esito positivo o un \_ **valore HRESULT** che indica la causa dell'errore.</span><span class="sxs-lookup"><span data-stu-id="c332c-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="c332c-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c332c-111">Remarks</span></span>

<span data-ttu-id="c332c-112">Questo metodo esegue l'override [**del metodo CBasePin::CompleteConnect.**](cbasepin-completeconnect.md)</span><span class="sxs-lookup"><span data-stu-id="c332c-112">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span> <span data-ttu-id="c332c-113">Chiama il [**metodo DecideAllocator,**](cbaseoutputpin-decideallocator.md) che seleziona l'allocatore di memoria da usare per questa connessione.</span><span class="sxs-lookup"><span data-stu-id="c332c-113">It calls the [**DecideAllocator**](cbaseoutputpin-decideallocator.md) method, which selects the memory allocator to use for this connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="c332c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c332c-114">Requirements</span></span>



| <span data-ttu-id="c332c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c332c-115">Requirement</span></span> | <span data-ttu-id="c332c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c332c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c332c-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c332c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c332c-118"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c332c-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c332c-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="c332c-119">Library</span></span><br/> | <dl> <span data-ttu-id="c332c-120"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c332c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c332c-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c332c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c332c-122">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="c332c-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




