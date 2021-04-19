---
description: Il metodo init Inizializza il thread di streaming.
ms.assetid: c746e595-de97-478c-8b22-5c4dd5594a8f
title: Metodo CSourceStream.Init (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Init
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a3abf2b4637385616862c0613f72afd676f5b79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330042"
---
# <a name="csourcestreaminit-method"></a><span data-ttu-id="766ec-103">Metodo CSourceStream.Init</span><span class="sxs-lookup"><span data-stu-id="766ec-103">CSourceStream.Init method</span></span>

<span data-ttu-id="766ec-104">Il `Init` metodo inizializza il thread di streaming.</span><span class="sxs-lookup"><span data-stu-id="766ec-104">The `Init` method initializes the streaming thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="766ec-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="766ec-105">Syntax</span></span>


```C++
HRESULT Init();
```



## <a name="parameters"></a><span data-ttu-id="766ec-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="766ec-106">Parameters</span></span>

<span data-ttu-id="766ec-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="766ec-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="766ec-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="766ec-108">Return value</span></span>

<span data-ttu-id="766ec-109">Restituisce S \_ OK o un altro valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="766ec-109">Returns S\_OK, or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="766ec-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="766ec-110">Remarks</span></span>

<span data-ttu-id="766ec-111">Questo metodo deve essere la prima richiesta di thread inviata al metodo [**CSourceStream:: ThreadProc**](csourcestream-threadproc.md) .</span><span class="sxs-lookup"><span data-stu-id="766ec-111">This method must be the first thread request sent to the [**CSourceStream::ThreadProc**](csourcestream-threadproc.md) method.</span></span> <span data-ttu-id="766ec-112">Il metodo [**CSourceStream:: Active**](csourcestream-active.md) chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="766ec-112">The [**CSourceStream::Active**](csourcestream-active.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="766ec-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="766ec-113">Requirements</span></span>



| <span data-ttu-id="766ec-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="766ec-114">Requirement</span></span> | <span data-ttu-id="766ec-115">Valore</span><span class="sxs-lookup"><span data-stu-id="766ec-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="766ec-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="766ec-116">Header</span></span><br/>  | <dl> <span data-ttu-id="766ec-117"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="766ec-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="766ec-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="766ec-118">Library</span></span><br/> | <dl> <span data-ttu-id="766ec-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="766ec-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="766ec-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="766ec-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="766ec-121">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="766ec-121">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




