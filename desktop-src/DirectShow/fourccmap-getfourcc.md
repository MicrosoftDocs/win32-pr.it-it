---
description: Recupera FOURCC&\# 160; DWORD dall'oggetto FOURCCMap.
ms.assetid: bb382a57-8499-44c0-b287-2d31f5f5d1d0
title: 'Metodo FOURCCMap:: GetFOURCC (fourcc. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.GetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c76493ff172f7a5611367fd50aa3b7957cf5441b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325924"
---
# <a name="fourccmapgetfourcc-method"></a><span data-ttu-id="2e714-103">Metodo FOURCCMap:: GetFOURCC</span><span class="sxs-lookup"><span data-stu-id="2e714-103">FOURCCMap::GetFOURCC method</span></span>

<span data-ttu-id="2e714-104">Recupera il  **valore DWORD** FourCC dall'oggetto [**FOURCCMap**](fourccmap.md) .</span><span class="sxs-lookup"><span data-stu-id="2e714-104">Retrieves the **FOURCC** **DWORD** from the [**FOURCCMap**](fourccmap.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e714-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e714-105">Syntax</span></span>


```C++
DWORD GetFOURCC();
```



## <a name="parameters"></a><span data-ttu-id="2e714-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e714-106">Parameters</span></span>

<span data-ttu-id="2e714-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="2e714-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2e714-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e714-108">Return value</span></span>

<span data-ttu-id="2e714-109">Restituisce il valore **DWORD** **fourcc** .</span><span class="sxs-lookup"><span data-stu-id="2e714-109">Returns the **FOURCC** **DWORD** value.</span></span> <span data-ttu-id="2e714-110">Si noti che se si costruisce un **GUID** che non è stato originariamente derivato da un **fourcc**, il valore restituito sarà essenzialmente casuale.</span><span class="sxs-lookup"><span data-stu-id="2e714-110">Note that if you construct a **GUID** that was not originally derived from a **FOURCC**, the return value will be essentially random.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e714-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e714-111">Requirements</span></span>



| <span data-ttu-id="2e714-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e714-112">Requirement</span></span> | <span data-ttu-id="2e714-113">Valore</span><span class="sxs-lookup"><span data-stu-id="2e714-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e714-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2e714-114">Header</span></span><br/>  | <dl> <span data-ttu-id="2e714-115"><dt>FourCC. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2e714-115"><dt>Fourcc.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="2e714-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="2e714-116">Library</span></span><br/> | <dl> <span data-ttu-id="2e714-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2e714-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e714-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e714-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e714-119">**Classe FOURCCMap**</span><span class="sxs-lookup"><span data-stu-id="2e714-119">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




