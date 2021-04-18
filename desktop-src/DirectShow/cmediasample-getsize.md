---
description: 'Il metodo GetSize recupera le dimensioni del buffer. Questo metodo implementa il metodo IMediaSample:: GetSize.'
ms.assetid: 14562ef4-f554-4d5a-83d3-1a29abae08a4
title: Metodo CMediaSample. GetSize (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff4146b66ca62905fe54eeb88d1e38ccf56ceea9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324962"
---
# <a name="cmediasamplegetsize-method"></a><span data-ttu-id="e8e14-104">Metodo CMediaSample. GetSize</span><span class="sxs-lookup"><span data-stu-id="e8e14-104">CMediaSample.GetSize method</span></span>

<span data-ttu-id="e8e14-105">Il `GetSize` metodo recupera le dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="e8e14-105">The `GetSize` method retrieves the size of the buffer.</span></span> <span data-ttu-id="e8e14-106">Questo metodo implementa il metodo [**IMediaSample:: GetSize**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getsize) .</span><span class="sxs-lookup"><span data-stu-id="e8e14-106">This method implements the [**IMediaSample::GetSize**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getsize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8e14-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8e14-107">Syntax</span></span>


```C++
LONG GetSize();
```



## <a name="parameters"></a><span data-ttu-id="e8e14-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8e14-108">Parameters</span></span>

<span data-ttu-id="e8e14-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e8e14-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e8e14-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8e14-110">Return value</span></span>

<span data-ttu-id="e8e14-111">Restituisce la dimensione, in byte, del buffer.</span><span class="sxs-lookup"><span data-stu-id="e8e14-111">Returns the size of the buffer, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8e14-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8e14-112">Requirements</span></span>



| <span data-ttu-id="e8e14-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8e14-113">Requirement</span></span> | <span data-ttu-id="e8e14-114">Valore</span><span class="sxs-lookup"><span data-stu-id="e8e14-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8e14-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8e14-115">Header</span></span><br/>  | <dl> <span data-ttu-id="e8e14-116"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8e14-116"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e8e14-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="e8e14-117">Library</span></span><br/> | <dl> <span data-ttu-id="e8e14-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e8e14-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8e14-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8e14-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8e14-120">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="e8e14-120">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




