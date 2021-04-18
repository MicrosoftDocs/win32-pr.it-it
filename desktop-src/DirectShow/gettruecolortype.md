---
description: La funzione GetTrueColorType Recupera il nome leggibile di un sottotipo video.
ms.assetid: 479a020c-b55c-44ec-9096-5528113a4b74
title: Funzione GetTrueColorType (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetTrueColorType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c262031045eed3755fe2d19d3bd703a347e6117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328242"
---
# <a name="gettruecolortype-function"></a><span data-ttu-id="a48b9-103">GetTrueColorType (funzione)</span><span class="sxs-lookup"><span data-stu-id="a48b9-103">GetTrueColorType function</span></span>

<span data-ttu-id="a48b9-104">La funzione **GetTrueColorType** Recupera il nome leggibile di un sottotipo video.</span><span class="sxs-lookup"><span data-stu-id="a48b9-104">The **GetTrueColorType** function retrieves the human-readable name of a video subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="a48b9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a48b9-105">Syntax</span></span>


```C++
const GUID GetTrueColorType(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="a48b9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a48b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a48b9-107">*pHeader*</span><span class="sxs-lookup"><span data-stu-id="a48b9-107">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="a48b9-108">Puntatore a una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) che definisce la bitmap.</span><span class="sxs-lookup"><span data-stu-id="a48b9-108">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure that defines the bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a48b9-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a48b9-109">Return value</span></span>

<span data-ttu-id="a48b9-110">Restituisce MEDIASUBTYPE \_ RGB555 o MEDIASUBTYPE \_ RGB565.</span><span class="sxs-lookup"><span data-stu-id="a48b9-110">Returns MEDIASUBTYPE\_RGB555 or MEDIASUBTYPE\_RGB565.</span></span>

## <a name="requirements"></a><span data-ttu-id="a48b9-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a48b9-111">Requirements</span></span>



| <span data-ttu-id="a48b9-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="a48b9-112">Requirement</span></span> | <span data-ttu-id="a48b9-113">Valore</span><span class="sxs-lookup"><span data-stu-id="a48b9-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a48b9-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a48b9-114">Header</span></span><br/>  | <dl> <span data-ttu-id="a48b9-115"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a48b9-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a48b9-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="a48b9-116">Library</span></span><br/> | <dl> <span data-ttu-id="a48b9-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a48b9-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a48b9-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a48b9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a48b9-119">Funzioni video e immagine</span><span class="sxs-lookup"><span data-stu-id="a48b9-119">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




