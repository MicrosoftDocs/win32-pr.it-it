---
description: La funzione GetBitmapSize calcola il numero di byte richiesti da una bitmap indipendente dal dispositivo (DIB). Questa funzione chiama semplicemente la macro DIBSIZE.
ms.assetid: ce23cdf2-9804-4d2e-b9ef-16e54b2d571e
title: Funzione GetBitmapSize (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 004201cf3ff839aa1301dcfff0240a73a9128e50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328555"
---
# <a name="getbitmapsize-function"></a><span data-ttu-id="79ea2-104">GetBitmapSize (funzione)</span><span class="sxs-lookup"><span data-stu-id="79ea2-104">GetBitmapSize function</span></span>

<span data-ttu-id="79ea2-105">La `GetBitmapSize` funzione calcola il numero di byte richiesti da una bitmap indipendente dal dispositivo (DIB).</span><span class="sxs-lookup"><span data-stu-id="79ea2-105">The `GetBitmapSize` function calculates the number of bytes required by a device-independent bitmap (DIB).</span></span> <span data-ttu-id="79ea2-106">Questa funzione chiama semplicemente la macro [**DIBSIZE**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize) .</span><span class="sxs-lookup"><span data-stu-id="79ea2-106">This function simply calls the [**DIBSIZE**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize) macro.</span></span>

## <a name="syntax"></a><span data-ttu-id="79ea2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="79ea2-107">Syntax</span></span>


```C++
DWORD GetBitmapSize(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="79ea2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="79ea2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79ea2-109">*pHeader*</span><span class="sxs-lookup"><span data-stu-id="79ea2-109">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="79ea2-110">Puntatore a una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="79ea2-110">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79ea2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="79ea2-111">Return value</span></span>

<span data-ttu-id="79ea2-112">Restituisce le dimensioni in byte.</span><span class="sxs-lookup"><span data-stu-id="79ea2-112">Returns the size in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="79ea2-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="79ea2-113">Requirements</span></span>



| <span data-ttu-id="79ea2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="79ea2-114">Requirement</span></span> | <span data-ttu-id="79ea2-115">Valore</span><span class="sxs-lookup"><span data-stu-id="79ea2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79ea2-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="79ea2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="79ea2-117"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="79ea2-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="79ea2-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="79ea2-118">Library</span></span><br/> | <dl> <span data-ttu-id="79ea2-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="79ea2-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79ea2-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="79ea2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79ea2-121">Funzioni video e immagine</span><span class="sxs-lookup"><span data-stu-id="79ea2-121">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




