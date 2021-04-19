---
description: La funzione DbgTerminate pulisce la libreria di debug. Ignorato nelle compilazioni al dettaglio.
ms.assetid: a0e23c57-b4b5-4bcf-8c63-0dee40cc71a7
title: Funzione DbgTerminate (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgTerminate
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d29e5fde86b9573261e39a0dbe2e9d87018ff23c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326659"
---
# <a name="dbgterminate-function"></a><span data-ttu-id="d89ed-104">DbgTerminate (funzione)</span><span class="sxs-lookup"><span data-stu-id="d89ed-104">DbgTerminate function</span></span>

<span data-ttu-id="d89ed-105">La funzione **DbgTerminate** pulisce la libreria di debug.</span><span class="sxs-lookup"><span data-stu-id="d89ed-105">The **DbgTerminate** function cleans up the debug library.</span></span> <span data-ttu-id="d89ed-106">Ignorato nelle compilazioni al dettaglio.</span><span class="sxs-lookup"><span data-stu-id="d89ed-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="d89ed-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d89ed-107">Syntax</span></span>


```C++
void DbgTerminate(void);
```



## <a name="parameters"></a><span data-ttu-id="d89ed-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d89ed-108">Parameters</span></span>

<span data-ttu-id="d89ed-109">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="d89ed-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d89ed-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d89ed-110">Return value</span></span>

<span data-ttu-id="d89ed-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="d89ed-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d89ed-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="d89ed-112">Remarks</span></span>

<span data-ttu-id="d89ed-113">Chiamare questa funzione se si chiama la funzione [**DbgInitialise**](dbginitialise.md) .</span><span class="sxs-lookup"><span data-stu-id="d89ed-113">Call this function if you call the [**DbgInitialise**](dbginitialise.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d89ed-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d89ed-114">Requirements</span></span>



| <span data-ttu-id="d89ed-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d89ed-115">Requirement</span></span> | <span data-ttu-id="d89ed-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d89ed-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d89ed-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d89ed-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d89ed-118"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d89ed-118"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d89ed-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="d89ed-119">Library</span></span><br/> | <dl> <span data-ttu-id="d89ed-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d89ed-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d89ed-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d89ed-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d89ed-122">Funzioni di output di debug</span><span class="sxs-lookup"><span data-stu-id="d89ed-122">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




