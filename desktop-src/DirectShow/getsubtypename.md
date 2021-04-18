---
description: La funzione GetSubtypeName Recupera il nome leggibile di un sottotipo video.
ms.assetid: 493b434e-2d36-4897-a5b2-7be0eb0a560f
title: Funzione GetSubtypeName (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSubtypeName
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f5cae835a3a7f1b5510d85ecf3f2ae9d15251a45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330932"
---
# <a name="getsubtypename-function"></a><span data-ttu-id="26f18-103">GetSubtypeName (funzione)</span><span class="sxs-lookup"><span data-stu-id="26f18-103">GetSubtypeName function</span></span>

<span data-ttu-id="26f18-104">La `GetSubtypeName` funzione recupera il nome leggibile di un sottotipo video.</span><span class="sxs-lookup"><span data-stu-id="26f18-104">The `GetSubtypeName` function retrieves the human-readable name of a video subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="26f18-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26f18-105">Syntax</span></span>


```C++
TCHAR* GetSubtypeName(
   const GUID *pSubtype
);
```



## <a name="parameters"></a><span data-ttu-id="26f18-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="26f18-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26f18-107">*pSubtype*</span><span class="sxs-lookup"><span data-stu-id="26f18-107">*pSubtype*</span></span> 
</dt> <dd>

<span data-ttu-id="26f18-108">Puntatore a un **GUID** del sottotipo video.</span><span class="sxs-lookup"><span data-stu-id="26f18-108">Pointer to a video subtype **GUID**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26f18-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="26f18-109">Return value</span></span>

<span data-ttu-id="26f18-110">Restituisce una stringa contenente il nome.</span><span class="sxs-lookup"><span data-stu-id="26f18-110">Returns a string containing the name.</span></span>

## <a name="requirements"></a><span data-ttu-id="26f18-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26f18-111">Requirements</span></span>



| <span data-ttu-id="26f18-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="26f18-112">Requirement</span></span> | <span data-ttu-id="26f18-113">Valore</span><span class="sxs-lookup"><span data-stu-id="26f18-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26f18-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26f18-114">Header</span></span><br/>  | <dl> <span data-ttu-id="26f18-115"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="26f18-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="26f18-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="26f18-116">Library</span></span><br/> | <dl> <span data-ttu-id="26f18-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="26f18-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26f18-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26f18-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26f18-119">Funzioni video e immagine</span><span class="sxs-lookup"><span data-stu-id="26f18-119">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




