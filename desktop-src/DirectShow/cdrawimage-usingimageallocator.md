---
description: Il metodo UsingImageAllocator indica se l'allocatore corrente è un oggetto CImageAllocator.
ms.assetid: 842bbcbc-2cc8-4e9d-b6c0-e07f7e472ca1
title: Metodo CDrawImage. UsingImageAllocator (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.UsingImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a61b4ece94c9c52a0f769a29ec32a26c08b33ee0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333717"
---
# <a name="cdrawimageusingimageallocator-method"></a><span data-ttu-id="32b90-103">CDrawImage. UsingImageAllocator, metodo</span><span class="sxs-lookup"><span data-stu-id="32b90-103">CDrawImage.UsingImageAllocator method</span></span>

<span data-ttu-id="32b90-104">Il `UsingImageAllocator` metodo indica se l'allocatore corrente è un oggetto [**CImageAllocator**](cimageallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="32b90-104">The `UsingImageAllocator` method indicates whether the current allocator is a [**CImageAllocator**](cimageallocator.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="32b90-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32b90-105">Syntax</span></span>


```C++
BOOL UsingImageAllocator();
```



## <a name="parameters"></a><span data-ttu-id="32b90-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="32b90-106">Parameters</span></span>

<span data-ttu-id="32b90-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="32b90-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="32b90-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="32b90-108">Return value</span></span>

<span data-ttu-id="32b90-109">Restituisce **true** se l'allocatore corrente è un oggetto **CImageAllocator** o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="32b90-109">Returns **TRUE** if the current allocator is a **CImageAllocator** object, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="32b90-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32b90-110">Requirements</span></span>



| <span data-ttu-id="32b90-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="32b90-111">Requirement</span></span> | <span data-ttu-id="32b90-112">Valore</span><span class="sxs-lookup"><span data-stu-id="32b90-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32b90-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="32b90-113">Header</span></span><br/>  | <dl> <span data-ttu-id="32b90-114"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32b90-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="32b90-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="32b90-115">Library</span></span><br/> | <dl> <span data-ttu-id="32b90-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="32b90-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32b90-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32b90-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32b90-118">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="32b90-118">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="32b90-119">**CDrawImage::NotifyAllocator**</span><span class="sxs-lookup"><span data-stu-id="32b90-119">**CDrawImage::NotifyAllocator**</span></span>](cdrawimage-notifyallocator.md)
</dt> </dl>

 

 




