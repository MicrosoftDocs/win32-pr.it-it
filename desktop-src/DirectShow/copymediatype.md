---
description: La funzione CopyMediaType copia una \_ struttura del tipo di supporto am \_ in un'altra struttura, incluso il blocco di formato
ms.assetid: 5b47e197-abb5-4b2c-ad65-a506c5e239be
title: Funzione CopyMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CopyMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e37f277244ae9b82c395d7901917e1fc1e78b35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330219"
---
# <a name="copymediatype-function"></a><span data-ttu-id="cbf6c-103">CopyMediaType (funzione)</span><span class="sxs-lookup"><span data-stu-id="cbf6c-103">CopyMediaType function</span></span>

<span data-ttu-id="cbf6c-104">La funzione **CopyMediaType** copia una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) in un'altra struttura, incluso il blocco di formato</span><span class="sxs-lookup"><span data-stu-id="cbf6c-104">The **CopyMediaType** function copies an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure into another structure, including the format block</span></span>

## <a name="syntax"></a><span data-ttu-id="cbf6c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cbf6c-105">Syntax</span></span>


```C++
HRESULT WINAPI CopyMediaType(
         AM_MEDIA_TYPE *pmtTarget,
   const AM_MEDIA_TYPE *pmtSource
);
```



## <a name="parameters"></a><span data-ttu-id="cbf6c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cbf6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbf6c-107">*pmtTarget*</span><span class="sxs-lookup"><span data-stu-id="cbf6c-107">*pmtTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="cbf6c-108">Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="cbf6c-108">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="cbf6c-109">Il metodo copia il tipo di supporto in questa struttura.</span><span class="sxs-lookup"><span data-stu-id="cbf6c-109">The method copies the media type into this structure.</span></span>

</dd> <dt>

<span data-ttu-id="cbf6c-110">*pmtSource*</span><span class="sxs-lookup"><span data-stu-id="cbf6c-110">*pmtSource*</span></span> 
</dt> <dd>

<span data-ttu-id="cbf6c-111">Puntatore a una struttura [**di \_ \_ tipo multimediale**](/windows/win32/api/strmif/ns-strmif-am_media_type) di origine per la copia.</span><span class="sxs-lookup"><span data-stu-id="cbf6c-111">Pointer to a source [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to copy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbf6c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cbf6c-112">Return value</span></span>

<span data-ttu-id="cbf6c-113">Restituisce S \_ OK o e \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="cbf6c-113">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbf6c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="cbf6c-114">Remarks</span></span>

<span data-ttu-id="cbf6c-115">Questa funzione alloca la memoria per il blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="cbf6c-115">This function allocates the memory for the format block.</span></span> <span data-ttu-id="cbf6c-116">Se il parametro *pmtTarget* contiene già un blocco di formato allocato, si verificherà una perdita di memoria.</span><span class="sxs-lookup"><span data-stu-id="cbf6c-116">If the *pmtTarget* parameter already contains an allocated format block, a memory leak will occur.</span></span> <span data-ttu-id="cbf6c-117">Per evitare una perdita di memoria, chiamare [**FreeMediaType**](freemediatype.md) prima di chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="cbf6c-117">To avoid a memory leak, call [**FreeMediaType**](freemediatype.md) before calling this function.</span></span>

<span data-ttu-id="cbf6c-118">Dopo la restituzione del metodo, chiamare [**FreeMediaType**](freemediatype.md) su *pmtTarget* per liberare il blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="cbf6c-118">After the method returns, call [**FreeMediaType**](freemediatype.md) on *pmtTarget* to free the format block.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbf6c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cbf6c-119">Requirements</span></span>



| <span data-ttu-id="cbf6c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbf6c-120">Requirement</span></span> | <span data-ttu-id="cbf6c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="cbf6c-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf6c-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cbf6c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="cbf6c-123"><dt>Mtype. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cbf6c-123"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="cbf6c-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="cbf6c-124">Library</span></span><br/> | <dl> <span data-ttu-id="cbf6c-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cbf6c-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbf6c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cbf6c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbf6c-127">**Funzioni di tipo multimediale**</span><span class="sxs-lookup"><span data-stu-id="cbf6c-127">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

 




