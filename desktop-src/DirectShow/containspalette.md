---
description: La funzione ContainsPalette determina se una struttura VIDEOINFOHEADER specificata contiene una tavolozza.
ms.assetid: e87ab1af-a822-45d8-9326-08b450e11279
title: Funzione ContainsPalette (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContainsPalette
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9417d9dd39f958e4a4caf68ef368d231a2097de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329761"
---
# <a name="containspalette-function"></a><span data-ttu-id="3e45d-103">ContainsPalette (funzione)</span><span class="sxs-lookup"><span data-stu-id="3e45d-103">ContainsPalette function</span></span>

<span data-ttu-id="3e45d-104">La funzione **ContainsPalette** determina se una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) specificata contiene una tavolozza.</span><span class="sxs-lookup"><span data-stu-id="3e45d-104">The **ContainsPalette** function determines whether a specified [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure contains a palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e45d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e45d-105">Syntax</span></span>


```C++
BOOL ContainsPalette(
   const VIDEOINFOHEADER *pVideoInfo

);
```



## <a name="parameters"></a><span data-ttu-id="3e45d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e45d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e45d-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="3e45d-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="3e45d-108">Puntatore a una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="3e45d-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e45d-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e45d-109">Return value</span></span>

<span data-ttu-id="3e45d-110">Restituisce **true** se bitdepth è 8 o less (**bmiHeader. biBitCount**) o il numero di indici di colore è maggiore di zero (**bmiHeader. biClrUsed**).</span><span class="sxs-lookup"><span data-stu-id="3e45d-110">Returns **TRUE** if the bitdepth is 8 or less (**bmiHeader.biBitCount**), or the number of color indexes is more than zero (**bmiHeader.biClrUsed**).</span></span> <span data-ttu-id="3e45d-111">In caso contrario, restituisce **false** .</span><span class="sxs-lookup"><span data-stu-id="3e45d-111">Returns **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e45d-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e45d-112">Requirements</span></span>



| <span data-ttu-id="3e45d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e45d-113">Requirement</span></span> | <span data-ttu-id="3e45d-114">Valore</span><span class="sxs-lookup"><span data-stu-id="3e45d-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e45d-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e45d-115">Header</span></span><br/>  | <dl> <span data-ttu-id="3e45d-116"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e45d-116"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3e45d-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="3e45d-117">Library</span></span><br/> | <dl> <span data-ttu-id="3e45d-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3e45d-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e45d-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e45d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e45d-120">Funzioni video e immagine</span><span class="sxs-lookup"><span data-stu-id="3e45d-120">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




