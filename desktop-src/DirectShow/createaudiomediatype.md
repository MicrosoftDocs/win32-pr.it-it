---
description: La funzione CreateAudioMediaType Inizializza un tipo di supporto da una struttura WAVEFORMATEX.
ms.assetid: 2571b7b4-86e9-443f-a99d-9ba48f469522
title: Funzione CreateAudioMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateAudioMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef4e525762d4b6928e6a9095fad34f3f4f2e96fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331320"
---
# <a name="createaudiomediatype-function"></a><span data-ttu-id="e030a-103">CreateAudioMediaType (funzione)</span><span class="sxs-lookup"><span data-stu-id="e030a-103">CreateAudioMediaType function</span></span>

<span data-ttu-id="e030a-104">La funzione **CreateAudioMediaType** Inizializza un tipo di supporto da una struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e030a-104">The **CreateAudioMediaType** function initializes a media type from a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e030a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e030a-105">Syntax</span></span>


```C++
HRESULT STDAPI CreateAudioMediaType(
   const WAVEFORMATEX  *pwfx,
         AM_MEDIA_TYPE *pmt,
         BOOL          bSetFormat
);
```



## <a name="parameters"></a><span data-ttu-id="e030a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e030a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e030a-107">*pwfx*</span><span class="sxs-lookup"><span data-stu-id="e030a-107">*pwfx*</span></span> 
</dt> <dd>

<span data-ttu-id="e030a-108">Puntatore alla struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) fornita.</span><span class="sxs-lookup"><span data-stu-id="e030a-108">Pointer to the supplied [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e030a-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="e030a-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="e030a-110">Puntatore alla struttura [**del \_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) da inizializzare.</span><span class="sxs-lookup"><span data-stu-id="e030a-110">Pointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to initialize.</span></span>

</dd> <dt>

<span data-ttu-id="e030a-111">*bSetFormat*</span><span class="sxs-lookup"><span data-stu-id="e030a-111">*bSetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="e030a-112">Flag che indica se inizializzare il blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="e030a-112">Flag indicating whether to initialize the format block.</span></span> <span data-ttu-id="e030a-113">Specificare **true** per inizializzarlo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e030a-113">Specify **TRUE** to initialize it, or **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e030a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e030a-114">Return value</span></span>

<span data-ttu-id="e030a-115">Restituisce E \_ OutOfMemory se non è stato possibile allocare memoria per i dati del formato. S \_ OK in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e030a-115">Returns E\_OUTOFMEMORY if memory could not be allocated for the format data; S\_OK otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e030a-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="e030a-116">Remarks</span></span>

<span data-ttu-id="e030a-117">Se il parametro *bSetFormat* è **true**, il metodo alloca la memoria per il blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="e030a-117">If the *bSetFormat* parameter is **TRUE**, the method allocates the memory for the format block.</span></span> <span data-ttu-id="e030a-118">Se il parametro *PMT* contiene già un blocco di formato allocato, si verificherà una perdita di memoria.</span><span class="sxs-lookup"><span data-stu-id="e030a-118">If the *pmt* parameter already contains an allocated format block, a memory leak will occur.</span></span> <span data-ttu-id="e030a-119">Per evitare una perdita di memoria, chiamare [**FreeMediaType**](freemediatype.md) prima di chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="e030a-119">To avoid a memory leak, call [**FreeMediaType**](freemediatype.md) before calling this function.</span></span> <span data-ttu-id="e030a-120">Quando il metodo restituisce un risultato, chiamare di nuovo **FreeMediaType** per liberare il blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="e030a-120">After the method returns, call **FreeMediaType** again to free the format block.</span></span>

## <a name="requirements"></a><span data-ttu-id="e030a-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e030a-121">Requirements</span></span>



| <span data-ttu-id="e030a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e030a-122">Requirement</span></span> | <span data-ttu-id="e030a-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e030a-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e030a-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e030a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e030a-125"><dt>Mtype. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e030a-125"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="e030a-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="e030a-126">Library</span></span><br/> | <dl> <span data-ttu-id="e030a-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e030a-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e030a-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e030a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e030a-129">**Funzioni di tipo multimediale**</span><span class="sxs-lookup"><span data-stu-id="e030a-129">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

