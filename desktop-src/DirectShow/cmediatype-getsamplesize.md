---
description: Il metodo GetSampleSize recupera le dimensioni del campione.
ms.assetid: 5cc98556-cca6-46ca-ad33-cd40011ff6f4
title: Metodo CMediaType. GetSampleSize (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.GetSampleSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc5b80e20ad2a16af9c25c68499348ffa744c0fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324006"
---
# <a name="cmediatypegetsamplesize-method"></a><span data-ttu-id="23689-103">CMediaType. GetSampleSize, metodo</span><span class="sxs-lookup"><span data-stu-id="23689-103">CMediaType.GetSampleSize method</span></span>

<span data-ttu-id="23689-104">Il `GetSampleSize` metodo recupera le dimensioni del campione.</span><span class="sxs-lookup"><span data-stu-id="23689-104">The `GetSampleSize` method retrieves the sample size.</span></span>

## <a name="syntax"></a><span data-ttu-id="23689-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23689-105">Syntax</span></span>


```C++
ULONG GetSampleSize() const;
```



## <a name="parameters"></a><span data-ttu-id="23689-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="23689-106">Parameters</span></span>

<span data-ttu-id="23689-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="23689-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="23689-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="23689-108">Return value</span></span>

<span data-ttu-id="23689-109">Se la dimensione del campione è fissa, restituisce le dimensioni del campione in byte.</span><span class="sxs-lookup"><span data-stu-id="23689-109">If the sample size is fixed, returns the sample size in bytes.</span></span> <span data-ttu-id="23689-110">In caso contrario, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="23689-110">Otherwise, returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="23689-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23689-111">Requirements</span></span>



| <span data-ttu-id="23689-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="23689-112">Requirement</span></span> | <span data-ttu-id="23689-113">Valore</span><span class="sxs-lookup"><span data-stu-id="23689-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23689-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="23689-114">Header</span></span><br/>  | <dl> <span data-ttu-id="23689-115"><dt>Mtype. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="23689-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="23689-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="23689-116">Library</span></span><br/> | <dl> <span data-ttu-id="23689-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="23689-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23689-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23689-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23689-119">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="23689-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




