---
description: 'Distruttore CSourceStream.~CSourceStream : metodo del distruttore.'
ms.assetid: 678085c2-5999-4e62-8749-99b783787cc6
title: Distruttore CSourceStream.~CSourceStream (Source.h)
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
ms.openlocfilehash: bbf53184dadc42145758ab387d15e8b0a1bfe09d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085209"
---
# <a name="csourcestreamcsourcestream-destructor"></a><span data-ttu-id="7d6b9-103">Distruttore CSourceStream.~CSourceStream</span><span class="sxs-lookup"><span data-stu-id="7d6b9-103">CSourceStream.~CSourceStream destructor</span></span>

<span data-ttu-id="7d6b9-104">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="7d6b9-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d6b9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7d6b9-105">Syntax</span></span>


```C++
~CSourceStream();
```



## <a name="remarks"></a><span data-ttu-id="7d6b9-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="7d6b9-106">Remarks</span></span>

<span data-ttu-id="7d6b9-107">Il distruttore rimuove automaticamente il segnaposto dal filtro proprietario chiamando [**CSource::RemovePin**](csource-removepin.md).</span><span class="sxs-lookup"><span data-stu-id="7d6b9-107">The destructor automatically removes the pin from the owning filter, by calling [**CSource::RemovePin**](csource-removepin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d6b9-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d6b9-108">Requirements</span></span>



| <span data-ttu-id="7d6b9-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d6b9-109">Requirement</span></span> | <span data-ttu-id="7d6b9-110">Valore</span><span class="sxs-lookup"><span data-stu-id="7d6b9-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d6b9-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d6b9-111">Header</span></span><br/>  | <dl> <span data-ttu-id="7d6b9-112"><dt>Source.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="7d6b9-112"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7d6b9-113">Libreria</span><span class="sxs-lookup"><span data-stu-id="7d6b9-113">Library</span></span><br/> | <dl> <span data-ttu-id="7d6b9-114"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7d6b9-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d6b9-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d6b9-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d6b9-116">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="7d6b9-116">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




