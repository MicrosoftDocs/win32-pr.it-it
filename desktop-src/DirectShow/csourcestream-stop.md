---
description: Il metodo Stop segnala al thread di streaming di arrestarsi.
ms.assetid: 79bc528a-cf53-43f3-aa17-c459063c99ab
title: Metodo CSourceStream. Stop (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 44c9f845c092280ef5fafa808036654bd868a796
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327529"
---
# <a name="csourcestreamstop-method"></a><span data-ttu-id="955b4-103">Metodo CSourceStream. Stop</span><span class="sxs-lookup"><span data-stu-id="955b4-103">CSourceStream.Stop method</span></span>

<span data-ttu-id="955b4-104">Il `Stop` metodo segnala al thread di streaming di arrestarsi.</span><span class="sxs-lookup"><span data-stu-id="955b4-104">The `Stop` method signals the streaming thread to stop.</span></span>

## <a name="syntax"></a><span data-ttu-id="955b4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="955b4-105">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="955b4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="955b4-106">Parameters</span></span>

<span data-ttu-id="955b4-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="955b4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="955b4-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="955b4-108">Return value</span></span>

<span data-ttu-id="955b4-109">Restituisce S \_ OK o e \_ imprevisto.</span><span class="sxs-lookup"><span data-stu-id="955b4-109">Returns S\_OK or E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="955b4-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="955b4-110">Remarks</span></span>

<span data-ttu-id="955b4-111">Il metodo [**CSourceStream:: inactive**](csourcestream-inactive.md) chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="955b4-111">The [**CSourceStream::Inactive**](csourcestream-inactive.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="955b4-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="955b4-112">Requirements</span></span>



| <span data-ttu-id="955b4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="955b4-113">Requirement</span></span> | <span data-ttu-id="955b4-114">Valore</span><span class="sxs-lookup"><span data-stu-id="955b4-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="955b4-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="955b4-115">Header</span></span><br/>  | <dl> <span data-ttu-id="955b4-116"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="955b4-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="955b4-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="955b4-117">Library</span></span><br/> | <dl> <span data-ttu-id="955b4-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="955b4-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="955b4-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="955b4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="955b4-120">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="955b4-120">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




