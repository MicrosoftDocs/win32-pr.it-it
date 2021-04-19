---
description: Il metodo CompleteConnect completa una connessione a un altro pin.
ms.assetid: 14bc48bc-ddfb-4491-8d5b-9e5ac601ba04
title: Metodo CTransformOutputPin. CompleteConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8d0c9c9fc7096191d7cdedffa21e2639fa0750ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333304"
---
# <a name="ctransformoutputpincompleteconnect-method"></a><span data-ttu-id="c929c-103">CTransformOutputPin. CompleteConnect, metodo</span><span class="sxs-lookup"><span data-stu-id="c929c-103">CTransformOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="c929c-104">Il `CompleteConnect` metodo completa una connessione a un altro pin.</span><span class="sxs-lookup"><span data-stu-id="c929c-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="c929c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c929c-105">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="c929c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c929c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c929c-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="c929c-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="c929c-108">Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) dell'altro pin.</span><span class="sxs-lookup"><span data-stu-id="c929c-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c929c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c929c-109">Return value</span></span>

<span data-ttu-id="c929c-110">Restituisce S \_ OK o un altro valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c929c-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c929c-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c929c-111">Remarks</span></span>

<span data-ttu-id="c929c-112">Questo metodo esegue l'override del metodo [**CBaseOutputPin:: CompleteConnect**](cbaseoutputpin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="c929c-112">This method overrides the [**CBaseOutputPin::CompleteConnect**](cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="c929c-113">Chiama il metodo [**CTransformFilter:: CompleteConnect**](ctransformfilter-completeconnect.md) del filtro, che restituisce \_ OK nella classe di base.</span><span class="sxs-lookup"><span data-stu-id="c929c-113">It calls the filter's [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="c929c-114">La classe derivata può eseguire l'override del metodo **CTransformFilter:: CompleteConnect** per eseguire ulteriori controlli.</span><span class="sxs-lookup"><span data-stu-id="c929c-114">The derived class can override the **CTransformFilter::CompleteConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="c929c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c929c-115">Requirements</span></span>



| <span data-ttu-id="c929c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c929c-116">Requirement</span></span> | <span data-ttu-id="c929c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c929c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c929c-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c929c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c929c-119"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c929c-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c929c-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="c929c-120">Library</span></span><br/> | <dl> <span data-ttu-id="c929c-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c929c-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




