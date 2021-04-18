---
description: Il metodo NotifyAllocator informa l'oggetto CDrawImage se l'allocatore per la connessione è un oggetto CImageAllocator.
ms.assetid: cc1604e7-f755-4a7a-9294-6fd06bb434d4
title: Metodo CDrawImage. NotifyAllocator (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7bab7d1d00b70317a7cbb0b79f8a430a603a757
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331921"
---
# <a name="cdrawimagenotifyallocator-method"></a><span data-ttu-id="bbe51-103">CDrawImage. NotifyAllocator, metodo</span><span class="sxs-lookup"><span data-stu-id="bbe51-103">CDrawImage.NotifyAllocator method</span></span>

<span data-ttu-id="bbe51-104">Il `NotifyAllocator` metodo informa l'oggetto **CDrawImage** se l'allocatore per la connessione è un oggetto [**CImageAllocator**](cimageallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="bbe51-104">The `NotifyAllocator` method informs the **CDrawImage** object whether the allocator for the connection is a [**CImageAllocator**](cimageallocator.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbe51-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bbe51-105">Syntax</span></span>


```C++
void NotifyAllocator(
   BOOL bUsingImageAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="bbe51-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bbe51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbe51-107">*bUsingImageAllocator*</span><span class="sxs-lookup"><span data-stu-id="bbe51-107">*bUsingImageAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="bbe51-108">Valore booleano che indica il tipo di allocatore usato.</span><span class="sxs-lookup"><span data-stu-id="bbe51-108">Boolean value that indicates what kind of allocator is being used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbe51-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bbe51-109">Return value</span></span>

<span data-ttu-id="bbe51-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="bbe51-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbe51-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="bbe51-111">Remarks</span></span>

<span data-ttu-id="bbe51-112">Il filtro proprietario deve chiamare questo metodo dopo che i pin accettano un allocatore.</span><span class="sxs-lookup"><span data-stu-id="bbe51-112">The owning filter should call this method after the pins agree to an allocator.</span></span> <span data-ttu-id="bbe51-113">Se il filtro sa che l'allocatore è un oggetto **CImageAllocator** , deve chiamare questo metodo con il valore **true**.</span><span class="sxs-lookup"><span data-stu-id="bbe51-113">If the filter knows the allocator is a **CImageAllocator** object, it should call this method with the value **TRUE**.</span></span> <span data-ttu-id="bbe51-114">In genere, il filtro lo conoscerà solo se è proprietario dell'allocatore in questione. In caso contrario, deve chiamare questo metodo con il valore **false**.</span><span class="sxs-lookup"><span data-stu-id="bbe51-114">(Typically, the filter will know this only if it owns the allocator in question.) Otherwise, it should call this method with the value **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbe51-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bbe51-115">Requirements</span></span>



| <span data-ttu-id="bbe51-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbe51-116">Requirement</span></span> | <span data-ttu-id="bbe51-117">Valore</span><span class="sxs-lookup"><span data-stu-id="bbe51-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbe51-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bbe51-118">Header</span></span><br/>  | <dl> <span data-ttu-id="bbe51-119"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bbe51-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bbe51-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="bbe51-120">Library</span></span><br/> | <dl> <span data-ttu-id="bbe51-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bbe51-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbe51-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bbe51-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbe51-123">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="bbe51-123">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="bbe51-124">**CDrawImage::D rawImage**</span><span class="sxs-lookup"><span data-stu-id="bbe51-124">**CDrawImage::DrawImage**</span></span>](cdrawimage-drawimage.md)
</dt> </dl>

 

 




