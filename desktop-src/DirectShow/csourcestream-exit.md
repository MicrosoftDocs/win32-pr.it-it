---
description: Il metodo Exit segnala al thread di streaming di uscire.
ms.assetid: 1bb59848-e405-40f9-87ec-33de8754e2dd
title: Metodo CSourceStream. Exit (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Exit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1ede6cf2318fa9226b8e220ff526f411def9b0f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329361"
---
# <a name="csourcestreamexit-method"></a><span data-ttu-id="ed87c-103">Metodo CSourceStream. Exit</span><span class="sxs-lookup"><span data-stu-id="ed87c-103">CSourceStream.Exit method</span></span>

<span data-ttu-id="ed87c-104">Il `Exit` metodo segnala al thread di streaming di uscire.</span><span class="sxs-lookup"><span data-stu-id="ed87c-104">The `Exit` method signals the streaming thread to exit.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed87c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed87c-105">Syntax</span></span>


```C++
HRESULT Exit();
```



## <a name="parameters"></a><span data-ttu-id="ed87c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed87c-106">Parameters</span></span>

<span data-ttu-id="ed87c-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="ed87c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ed87c-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed87c-108">Return value</span></span>

<span data-ttu-id="ed87c-109">Restituisce S \_ OK o e \_ imprevisto.</span><span class="sxs-lookup"><span data-stu-id="ed87c-109">Returns S\_OK or E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed87c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed87c-110">Remarks</span></span>

<span data-ttu-id="ed87c-111">Il metodo [**CSourceStream:: inactive**](csourcestream-inactive.md) chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="ed87c-111">The [**CSourceStream::Inactive**](csourcestream-inactive.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed87c-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed87c-112">Requirements</span></span>



| <span data-ttu-id="ed87c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed87c-113">Requirement</span></span> | <span data-ttu-id="ed87c-114">Valore</span><span class="sxs-lookup"><span data-stu-id="ed87c-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed87c-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed87c-115">Header</span></span><br/>  | <dl> <span data-ttu-id="ed87c-116"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed87c-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ed87c-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="ed87c-117">Library</span></span><br/> | <dl> <span data-ttu-id="ed87c-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ed87c-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed87c-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed87c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed87c-120">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="ed87c-120">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




