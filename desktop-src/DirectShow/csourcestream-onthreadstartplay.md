---
description: Il metodo OnThreadStartPlay viene chiamato all'inizio del metodo CSourceStream::D oBufferProcessingLoop.
ms.assetid: 16d3b28f-bfae-49af-b8e4-8cc8cb15ecab
title: Metodo CSourceStream. OnThreadStartPlay (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadStartPlay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 857f27ad39fb9169e1ef67253d5232c7cbc3dbb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330035"
---
# <a name="csourcestreamonthreadstartplay-method"></a><span data-ttu-id="6f97a-103">CSourceStream. OnThreadStartPlay, metodo</span><span class="sxs-lookup"><span data-stu-id="6f97a-103">CSourceStream.OnThreadStartPlay method</span></span>

<span data-ttu-id="6f97a-104">Il `OnThreadStartPlay` metodo viene chiamato all'inizio del metodo [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .</span><span class="sxs-lookup"><span data-stu-id="6f97a-104">The `OnThreadStartPlay` method is called at the start of the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f97a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f97a-105">Syntax</span></span>


```C++
virtual HRESULT OnThreadStartPlay();
```



## <a name="parameters"></a><span data-ttu-id="6f97a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6f97a-106">Parameters</span></span>

<span data-ttu-id="6f97a-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="6f97a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6f97a-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6f97a-108">Return value</span></span>

<span data-ttu-id="6f97a-109">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6f97a-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f97a-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f97a-110">Remarks</span></span>

<span data-ttu-id="6f97a-111">Questo metodo non esegue alcuna operazione nella classe di base. è disponibile per la classe derivata di cui eseguire l'override.</span><span class="sxs-lookup"><span data-stu-id="6f97a-111">This method does nothing in the base class; it is available for the derived class to override.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f97a-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f97a-112">Requirements</span></span>



| <span data-ttu-id="6f97a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f97a-113">Requirement</span></span> | <span data-ttu-id="6f97a-114">Valore</span><span class="sxs-lookup"><span data-stu-id="6f97a-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f97a-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f97a-115">Header</span></span><br/>  | <dl> <span data-ttu-id="6f97a-116"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6f97a-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6f97a-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="6f97a-117">Library</span></span><br/> | <dl> <span data-ttu-id="6f97a-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6f97a-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f97a-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f97a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f97a-120">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="6f97a-120">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




