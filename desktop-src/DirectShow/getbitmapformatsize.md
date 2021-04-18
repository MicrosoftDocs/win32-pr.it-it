---
description: La funzione GetBitmapFormatSize calcola la dimensione necessaria per una struttura VIDEOINFO che può ospitare una struttura BITMAPINFOHEADER specificata.
ms.assetid: a559415a-070f-4674-be12-a65a46025809
title: Funzione GetBitmapFormatSize (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapFormatSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39a64f6d975e403de6c177906b23ef7e09f29ddf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328556"
---
# <a name="getbitmapformatsize-function"></a><span data-ttu-id="6f5c2-103">GetBitmapFormatSize (funzione)</span><span class="sxs-lookup"><span data-stu-id="6f5c2-103">GetBitmapFormatSize function</span></span>

<span data-ttu-id="6f5c2-104">La `GetBitmapFormatSize` funzione calcola la dimensione necessaria per una struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) che può ospitare una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) specificata.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-104">The `GetBitmapFormatSize` function calculates the size needed for a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure that can hold a specified [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f5c2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f5c2-105">Syntax</span></span>


```C++
LONG GetBitmapFormatSize(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="6f5c2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6f5c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f5c2-107">*pHeader*</span><span class="sxs-lookup"><span data-stu-id="6f5c2-107">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="6f5c2-108">Puntatore a una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="6f5c2-108">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f5c2-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6f5c2-109">Return value</span></span>

<span data-ttu-id="6f5c2-110">Restituisce le dimensioni in byte.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-110">Returns the size, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f5c2-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f5c2-111">Remarks</span></span>

<span data-ttu-id="6f5c2-112">Una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) può essere seguita dalle maschere colori o dalle voci della tavolozza, pertanto può essere difficile determinare il numero di byte necessari per costruire una struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) da una struttura **BITMAPINFOHEADER** esistente.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-112">A [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure might be followed by color masks or palette entries, so it can be difficult to determine the number of bytes required to construct a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure from an existing **BITMAPINFOHEADER** structure.</span></span>

<span data-ttu-id="6f5c2-113">Per copiare una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) in una struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) , usare la macro [**header**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header) , che calcola l'offset corretto.</span><span class="sxs-lookup"><span data-stu-id="6f5c2-113">To copy a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure into a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure, use the [**HEADER**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header) macro, which calculates the correct offset.</span></span>

## <a name="examples"></a><span data-ttu-id="6f5c2-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="6f5c2-114">Examples</span></span>


```
LONG size = GetBitmapFormatSize(&bmi);

VIDEOINFO *pVi = static_cast<VIDEOINFO*>(CoTaskMemAlloc(size));

if (pVi != NULL)
{
    CopyMemory(HEADER(pVi), &bmi, sizeof(BITMAPINFOHEADER));
}
```



## <a name="requirements"></a><span data-ttu-id="6f5c2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f5c2-115">Requirements</span></span>



| <span data-ttu-id="6f5c2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f5c2-116">Requirement</span></span> | <span data-ttu-id="6f5c2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="6f5c2-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f5c2-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f5c2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6f5c2-119"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6f5c2-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6f5c2-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="6f5c2-120">Library</span></span><br/> | <dl> <span data-ttu-id="6f5c2-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6f5c2-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f5c2-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f5c2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f5c2-123">Funzioni video e immagine</span><span class="sxs-lookup"><span data-stu-id="6f5c2-123">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




