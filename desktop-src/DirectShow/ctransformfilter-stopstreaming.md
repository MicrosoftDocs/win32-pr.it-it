---
description: Il metodo StopStreaming viene chiamato quando il filtro passa allo stato interrotto.
ms.assetid: cfebfed2-4105-4dea-8d47-60d6160ee337
title: Metodo CTransformFilter. StopStreaming (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.StopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4990b55ad87a4eb754af7101e762ce227a090993
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329970"
---
# <a name="ctransformfilterstopstreaming-method"></a><span data-ttu-id="be9c4-103">CTransformFilter. StopStreaming, metodo</span><span class="sxs-lookup"><span data-stu-id="be9c4-103">CTransformFilter.StopStreaming method</span></span>

<span data-ttu-id="be9c4-104">Il `StopStreaming` metodo viene chiamato quando il filtro passa allo stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="be9c4-104">The `StopStreaming` method is called when the filter switches to the stopped state.</span></span>

## <a name="syntax"></a><span data-ttu-id="be9c4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="be9c4-105">Syntax</span></span>


```C++
virtual HRESULT StopStreaming();
```



## <a name="parameters"></a><span data-ttu-id="be9c4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="be9c4-106">Parameters</span></span>

<span data-ttu-id="be9c4-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="be9c4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="be9c4-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="be9c4-108">Return value</span></span>

<span data-ttu-id="be9c4-109">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="be9c4-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="be9c4-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="be9c4-110">Remarks</span></span>

<span data-ttu-id="be9c4-111">Questo metodo non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.</span><span class="sxs-lookup"><span data-stu-id="be9c4-111">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="be9c4-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be9c4-112">Requirements</span></span>



| <span data-ttu-id="be9c4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="be9c4-113">Requirement</span></span> | <span data-ttu-id="be9c4-114">Valore</span><span class="sxs-lookup"><span data-stu-id="be9c4-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be9c4-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="be9c4-115">Header</span></span><br/>  | <dl> <span data-ttu-id="be9c4-116"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be9c4-116"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="be9c4-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="be9c4-117">Library</span></span><br/> | <dl> <span data-ttu-id="be9c4-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="be9c4-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be9c4-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be9c4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be9c4-120">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="be9c4-120">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




