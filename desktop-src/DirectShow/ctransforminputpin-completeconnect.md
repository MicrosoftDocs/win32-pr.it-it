---
description: 'Metodo CTransformInputPin.CompleteConnect: il metodo CompleteConnect completa una connessione a un altro pin.'
ms.assetid: 568cee55-b9ea-4fc2-ac9d-0080b7de9790
title: Metodo CTransformInputPin.CompleteConnect (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 20f378479209b2614116ba25f51950923358f1b2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085009"
---
# <a name="ctransforminputpincompleteconnect-method"></a><span data-ttu-id="51e58-103">Metodo CTransformInputPin.CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="51e58-103">CTransformInputPin.CompleteConnect method</span></span>

<span data-ttu-id="51e58-104">Il `CompleteConnect` metodo completa una connessione a un altro pin.</span><span class="sxs-lookup"><span data-stu-id="51e58-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="51e58-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="51e58-105">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="51e58-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="51e58-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51e58-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="51e58-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="51e58-108">Puntatore all'interfaccia [**IPin dell'altro**](/windows/desktop/api/Strmif/nn-strmif-ipin) pin.</span><span class="sxs-lookup"><span data-stu-id="51e58-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51e58-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="51e58-109">Return value</span></span>

<span data-ttu-id="51e58-110">Restituisce S \_ OK o un altro valore **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="51e58-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="51e58-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="51e58-111">Remarks</span></span>

<span data-ttu-id="51e58-112">Questo metodo esegue l'override [**del metodo CBasePin::CompleteConnect.**](cbasepin-completeconnect.md)</span><span class="sxs-lookup"><span data-stu-id="51e58-112">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span> <span data-ttu-id="51e58-113">Chiama il metodo [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) del filtro, che restituisce S \_ OK nella classe di base.</span><span class="sxs-lookup"><span data-stu-id="51e58-113">It calls the filter's [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="51e58-114">La classe derivata può eseguire l'override del **metodo CTransformFilter::CompleteConnect** per eseguire controlli aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="51e58-114">The derived class can override the **CTransformFilter::CompleteConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="51e58-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51e58-115">Requirements</span></span>



| <span data-ttu-id="51e58-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="51e58-116">Requirement</span></span> | <span data-ttu-id="51e58-117">Valore</span><span class="sxs-lookup"><span data-stu-id="51e58-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51e58-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="51e58-118">Header</span></span><br/>  | <dl> <span data-ttu-id="51e58-119"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="51e58-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="51e58-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="51e58-120">Library</span></span><br/> | <dl> <span data-ttu-id="51e58-121"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="51e58-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




