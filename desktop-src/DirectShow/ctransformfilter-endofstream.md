---
description: Il metodo EndOfStream notifica al filtro che non sono previsti dati aggiuntivi dal pin di input.
ms.assetid: b8fc3976-e3d4-4f16-82b0-3900ad6a740c
title: Metodo CTransformFilter. EndOfStream (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dea676a42f6df46d0035fdbb6e812b1df15fbb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326933"
---
# <a name="ctransformfilterendofstream-method"></a><span data-ttu-id="8e044-103">CTransformFilter. EndOfStream, metodo</span><span class="sxs-lookup"><span data-stu-id="8e044-103">CTransformFilter.EndOfStream method</span></span>

<span data-ttu-id="8e044-104">Il `EndOfStream` metodo notifica al filtro che non sono previsti dati aggiuntivi dal pin di input.</span><span class="sxs-lookup"><span data-stu-id="8e044-104">The `EndOfStream` method notifies the filter that no additional data is expected from the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e044-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e044-105">Syntax</span></span>


```C++
virtual HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="8e044-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e044-106">Parameters</span></span>

<span data-ttu-id="8e044-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="8e044-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8e044-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8e044-108">Return value</span></span>

<span data-ttu-id="8e044-109">Restituisce S \_ OK o un altro valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8e044-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e044-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e044-110">Remarks</span></span>

<span data-ttu-id="8e044-111">Il metodo [**CTransformInputPin:: EndOfStream**](ctransforminputpin-endofstream.md) del PIN di input chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="8e044-111">The input pin's [**CTransformInputPin::EndOfStream**](ctransforminputpin-endofstream.md) method calls this method.</span></span> <span data-ttu-id="8e044-112">Questo metodo recapita la notifica di fine flusso a valle.</span><span class="sxs-lookup"><span data-stu-id="8e044-112">This method delivers the end-of-stream notification downstream.</span></span> <span data-ttu-id="8e044-113">Se la classe derivata utilizza un thread di lavoro per recapitare gli esempi di contenuti multimediali, deve eseguire l'override di questo metodo e accodare la notifica di fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="8e044-113">If the derived class uses a worker thread to deliver media samples, it should override this method and queue the end-of-stream notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e044-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e044-114">Requirements</span></span>



| <span data-ttu-id="8e044-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e044-115">Requirement</span></span> | <span data-ttu-id="8e044-116">Valore</span><span class="sxs-lookup"><span data-stu-id="8e044-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e044-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e044-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8e044-118"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8e044-118"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8e044-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="8e044-119">Library</span></span><br/> | <dl> <span data-ttu-id="8e044-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8e044-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e044-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e044-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e044-122">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="8e044-122">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




