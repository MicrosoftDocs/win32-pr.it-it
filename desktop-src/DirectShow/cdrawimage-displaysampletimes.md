---
description: Il metodo DisplaySampleTimes disegna i timestamp di un campione multimediale nella parte superiore dell'immagine del video.
ms.assetid: 3741dc74-5311-4cb1-9e6b-4a8bf6113477
title: Metodo CDrawImage. DisplaySampleTimes (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DisplaySampleTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9988aaedf9a1c01c83412cdbe9e00533556c9b15
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333721"
---
# <a name="cdrawimagedisplaysampletimes-method"></a><span data-ttu-id="13781-103">CDrawImage. DisplaySampleTimes, metodo</span><span class="sxs-lookup"><span data-stu-id="13781-103">CDrawImage.DisplaySampleTimes method</span></span>

<span data-ttu-id="13781-104">Il `DisplaySampleTimes` metodo disegna i timestamp di un campione multimediale sulla parte superiore dell'immagine del video.</span><span class="sxs-lookup"><span data-stu-id="13781-104">The `DisplaySampleTimes` method draws the time stamps of a media sample on top of the video image.</span></span>

## <a name="syntax"></a><span data-ttu-id="13781-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13781-105">Syntax</span></span>


```C++
void DisplaySampleTimes(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="13781-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="13781-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13781-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="13781-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="13781-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="13781-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13781-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="13781-109">Return value</span></span>

<span data-ttu-id="13781-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="13781-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="13781-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="13781-111">Remarks</span></span>

<span data-ttu-id="13781-112">Questo metodo viene chiamato solo nelle compilazioni di debug.</span><span class="sxs-lookup"><span data-stu-id="13781-112">This method is called only in debug builds.</span></span>

## <a name="requirements"></a><span data-ttu-id="13781-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13781-113">Requirements</span></span>



| <span data-ttu-id="13781-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="13781-114">Requirement</span></span> | <span data-ttu-id="13781-115">Valore</span><span class="sxs-lookup"><span data-stu-id="13781-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13781-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="13781-116">Header</span></span><br/>  | <dl> <span data-ttu-id="13781-117"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="13781-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="13781-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="13781-118">Library</span></span><br/> | <dl> <span data-ttu-id="13781-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="13781-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13781-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13781-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13781-121">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="13781-121">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




