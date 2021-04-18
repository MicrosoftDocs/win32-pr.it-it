---
description: Il metodo CreateImageSample crea un esempio di supporto.
ms.assetid: dae71692-5cbc-4bc7-a363-41766ef17c58
title: Metodo CImageAllocator. CreateImageSample (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CreateImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57463a7025ea816b6fe6bcaa8b964231458903de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329771"
---
# <a name="cimageallocatorcreateimagesample-method"></a><span data-ttu-id="5a76b-103">CImageAllocator. CreateImageSample, metodo</span><span class="sxs-lookup"><span data-stu-id="5a76b-103">CImageAllocator.CreateImageSample method</span></span>

<span data-ttu-id="5a76b-104">Il `CreateImageSample` metodo crea un esempio di supporto.</span><span class="sxs-lookup"><span data-stu-id="5a76b-104">The `CreateImageSample` method creates a media sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a76b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a76b-105">Syntax</span></span>


```C++
virtual CImageSample* CreateImageSample(
   LPBYTE pData,
   LONG   Length
);
```



## <a name="parameters"></a><span data-ttu-id="5a76b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a76b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a76b-107">*pData*</span><span class="sxs-lookup"><span data-stu-id="5a76b-107">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="5a76b-108">Puntatore a un buffer di *lunghezza* di dimensione, allocato dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="5a76b-108">Pointer to a buffer of size *Length*, allocated by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="5a76b-109">*Length*</span><span class="sxs-lookup"><span data-stu-id="5a76b-109">*Length*</span></span> 
</dt> <dd>

<span data-ttu-id="5a76b-110">Lunghezza del buffer.</span><span class="sxs-lookup"><span data-stu-id="5a76b-110">Length of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a76b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a76b-111">Return value</span></span>

<span data-ttu-id="5a76b-112">Restituisce un oggetto [**CImageSample**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="5a76b-112">Returns a [**CImageSample**](cimagesample.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a76b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a76b-113">Remarks</span></span>

<span data-ttu-id="5a76b-114">Questo metodo crea un nuovo esempio di supporto, implementato come oggetto **CImageSample** .</span><span class="sxs-lookup"><span data-stu-id="5a76b-114">This method creates a new media sample, implemented as a **CImageSample** object.</span></span> <span data-ttu-id="5a76b-115">Il metodo [**IMediaSample:: Getpointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) dell'esempio restituisce un puntatore al buffer specificato nel parametro *pData* .</span><span class="sxs-lookup"><span data-stu-id="5a76b-115">The sample's [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) method returns a pointer to the buffer specified in the *pData* parameter.</span></span>

<span data-ttu-id="5a76b-116">Se si deriva una nuova classe allocator da [**CImageAllocator**](cimageallocator.md) e una nuova classe di esempio media da [**CImageSample**](cimagesample.md), è necessario eseguire l'override di questo metodo per creare un'istanza della classe di esempio multimediale.</span><span class="sxs-lookup"><span data-stu-id="5a76b-116">If you derive a new allocator class from [**CImageAllocator**](cimageallocator.md) and a new media sample class from [**CImageSample**](cimagesample.md), you should override this method to create an instance of your media sample class.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a76b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a76b-117">Requirements</span></span>



| <span data-ttu-id="5a76b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a76b-118">Requirement</span></span> | <span data-ttu-id="5a76b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="5a76b-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a76b-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a76b-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5a76b-121"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5a76b-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5a76b-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="5a76b-122">Library</span></span><br/> | <dl> <span data-ttu-id="5a76b-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5a76b-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a76b-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a76b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a76b-125">**Classe CImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="5a76b-125">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> <dt>

[<span data-ttu-id="5a76b-126">**CImageAllocator:: Alloc**</span><span class="sxs-lookup"><span data-stu-id="5a76b-126">**CImageAllocator::Alloc**</span></span>](cimageallocator-alloc.md)
</dt> </dl>

 

 




