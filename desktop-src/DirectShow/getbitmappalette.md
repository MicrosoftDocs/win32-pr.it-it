---
description: La funzione GetBitmapPalette restituisce la prima voce della tavolozza in una struttura VIDEOINFOHEADER.
ms.assetid: 7c620f81-31d9-408f-954d-aeff39f93956
title: Funzione GetBitmapPalette (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapPalette
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ffa4139c7aaece3e92a26fbf69fc02b8759f1613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328248"
---
# <a name="getbitmappalette-function"></a><span data-ttu-id="84087-103">GetBitmapPalette (funzione)</span><span class="sxs-lookup"><span data-stu-id="84087-103">GetBitmapPalette function</span></span>

<span data-ttu-id="84087-104">La `GetBitmapPalette` funzione restituisce la prima voce della tavolozza in una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="84087-104">The `GetBitmapPalette` function returns the first palette entry in a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="84087-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="84087-105">Syntax</span></span>


```C++
const RGBQUAD* GetBitmapPalette(
   const VIDEOINFOHEADER *pVideoInfo
);
```



## <a name="parameters"></a><span data-ttu-id="84087-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="84087-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84087-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="84087-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="84087-108">Puntatore a una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="84087-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84087-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="84087-109">Return value</span></span>

<span data-ttu-id="84087-110">Restituisce un puntatore alla prima voce della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="84087-110">Returns a pointer to the first palette entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="84087-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84087-111">Requirements</span></span>



| <span data-ttu-id="84087-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="84087-112">Requirement</span></span> | <span data-ttu-id="84087-113">Valore</span><span class="sxs-lookup"><span data-stu-id="84087-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84087-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="84087-114">Header</span></span><br/>  | <dl> <span data-ttu-id="84087-115"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="84087-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="84087-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="84087-116">Library</span></span><br/> | <dl> <span data-ttu-id="84087-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="84087-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




