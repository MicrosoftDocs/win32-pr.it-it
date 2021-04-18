---
description: Il metodo StartStreaming viene chiamato quando il filtro passa allo stato sospeso.
ms.assetid: 1e3bbca7-b5b1-41fd-8f70-b7ef39c9491b
title: Metodo CTransformFilter. StartStreaming (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 50df2db2aada7f96744af5e553f474818594d399
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331125"
---
# <a name="ctransformfilterstartstreaming-method"></a><span data-ttu-id="f70cf-103">CTransformFilter. StartStreaming, metodo</span><span class="sxs-lookup"><span data-stu-id="f70cf-103">CTransformFilter.StartStreaming method</span></span>

<span data-ttu-id="f70cf-104">Il `StartStreaming` metodo viene chiamato quando il filtro passa allo stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="f70cf-104">The `StartStreaming` method is called when the filter switches to the paused state.</span></span>

## <a name="syntax"></a><span data-ttu-id="f70cf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f70cf-105">Syntax</span></span>


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="f70cf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f70cf-106">Parameters</span></span>

<span data-ttu-id="f70cf-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f70cf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f70cf-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f70cf-108">Return value</span></span>

<span data-ttu-id="f70cf-109">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f70cf-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f70cf-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="f70cf-110">Remarks</span></span>

<span data-ttu-id="f70cf-111">Questo metodo non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.</span><span class="sxs-lookup"><span data-stu-id="f70cf-111">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="f70cf-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f70cf-112">Requirements</span></span>



| <span data-ttu-id="f70cf-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f70cf-113">Requirement</span></span> | <span data-ttu-id="f70cf-114">Valore</span><span class="sxs-lookup"><span data-stu-id="f70cf-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f70cf-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f70cf-115">Header</span></span><br/>  | <dl> <span data-ttu-id="f70cf-116"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f70cf-116"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f70cf-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="f70cf-117">Library</span></span><br/> | <dl> <span data-ttu-id="f70cf-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f70cf-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f70cf-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f70cf-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f70cf-120">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="f70cf-120">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




