---
description: Metodo del distruttore.
ms.assetid: 678085c2-5999-4e62-8749-99b783787cc6
title: Distruttore CSourceStream. ~ CSourceStream (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.~CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa27d50a9c1acbc9c8a27407cb97673d60158e4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329041"
---
# <a name="csourcestreamcsourcestream-destructor"></a><span data-ttu-id="25f81-103">Distruttore CSourceStream. ~ CSourceStream</span><span class="sxs-lookup"><span data-stu-id="25f81-103">CSourceStream.~CSourceStream destructor</span></span>

<span data-ttu-id="25f81-104">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="25f81-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="25f81-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25f81-105">Syntax</span></span>


```C++
~CSourceStream();
```



## <a name="remarks"></a><span data-ttu-id="25f81-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="25f81-106">Remarks</span></span>

<span data-ttu-id="25f81-107">Il distruttore rimuove automaticamente il pin dal filtro proprietario, chiamando [**CSource:: RemovePin**](csource-removepin.md).</span><span class="sxs-lookup"><span data-stu-id="25f81-107">The destructor automatically removes the pin from the owning filter, by calling [**CSource::RemovePin**](csource-removepin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="25f81-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25f81-108">Requirements</span></span>



| <span data-ttu-id="25f81-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="25f81-109">Requirement</span></span> | <span data-ttu-id="25f81-110">Valore</span><span class="sxs-lookup"><span data-stu-id="25f81-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25f81-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25f81-111">Header</span></span><br/>  | <dl> <span data-ttu-id="25f81-112"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="25f81-112"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="25f81-113">Libreria</span><span class="sxs-lookup"><span data-stu-id="25f81-113">Library</span></span><br/> | <dl> <span data-ttu-id="25f81-114"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="25f81-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25f81-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25f81-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25f81-116">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="25f81-116">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




