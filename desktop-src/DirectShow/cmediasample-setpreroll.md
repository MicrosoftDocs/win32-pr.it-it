---
description: "Il metodo SetPreroll specifica se l'esempio è un esempio di preroll. Non è necessario visualizzare un campione di preroll. Questo metodo implementa il metodo IMediaSample:: SetPreroll."
ms.assetid: 2887e627-5999-407a-88d3-811c803c9a43
title: Metodo CMediaSample. SetPreroll (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 594f26ebb738a986c85a14b88f8896b122b58f47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325306"
---
# <a name="cmediasamplesetpreroll-method"></a><span data-ttu-id="ba5c5-105">CMediaSample. SetPreroll, metodo</span><span class="sxs-lookup"><span data-stu-id="ba5c5-105">CMediaSample.SetPreroll method</span></span>

<span data-ttu-id="ba5c5-106">Il `SetPreroll` metodo specifica se l'esempio è un esempio di preroll.</span><span class="sxs-lookup"><span data-stu-id="ba5c5-106">The `SetPreroll` method specifies whether this sample is a preroll sample.</span></span> <span data-ttu-id="ba5c5-107">Non è necessario visualizzare un campione di preroll.</span><span class="sxs-lookup"><span data-stu-id="ba5c5-107">A preroll sample should not be displayed.</span></span> <span data-ttu-id="ba5c5-108">Questo metodo implementa il metodo [**IMediaSample:: SetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setpreroll) .</span><span class="sxs-lookup"><span data-stu-id="ba5c5-108">This method implements the [**IMediaSample::SetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setpreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba5c5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba5c5-109">Syntax</span></span>


```C++
HRESULT SetPreroll(
   BOOL bIsPreroll
);
```



## <a name="parameters"></a><span data-ttu-id="ba5c5-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="ba5c5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba5c5-111">*bIsPreroll*</span><span class="sxs-lookup"><span data-stu-id="ba5c5-111">*bIsPreroll*</span></span> 
</dt> <dd>

<span data-ttu-id="ba5c5-112">Valore booleano che specifica se si tratta di un campione di preroll.</span><span class="sxs-lookup"><span data-stu-id="ba5c5-112">Boolean value that specifies whether this is a preroll sample.</span></span> <span data-ttu-id="ba5c5-113">Se **true**, si tratta di un esempio di preroll.</span><span class="sxs-lookup"><span data-stu-id="ba5c5-113">If **TRUE**, this is a preroll sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba5c5-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ba5c5-114">Return value</span></span>

<span data-ttu-id="ba5c5-115">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ba5c5-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba5c5-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba5c5-116">Remarks</span></span>

<span data-ttu-id="ba5c5-117">Questo metodo aggiorna la variabile membro [**\_ dwFlags CMediaSample:: m**](cmediasample-m-dwflags.md) , che specifica la proprietà preroll.</span><span class="sxs-lookup"><span data-stu-id="ba5c5-117">This method updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies the preroll property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba5c5-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba5c5-118">Requirements</span></span>



| <span data-ttu-id="ba5c5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba5c5-119">Requirement</span></span> | <span data-ttu-id="ba5c5-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ba5c5-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba5c5-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ba5c5-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ba5c5-122"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba5c5-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ba5c5-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="ba5c5-123">Library</span></span><br/> | <dl> <span data-ttu-id="ba5c5-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ba5c5-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba5c5-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba5c5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba5c5-126">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="ba5c5-126">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




