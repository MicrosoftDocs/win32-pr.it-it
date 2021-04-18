---
description: La funzione GetBitCount restituisce il numero di bit per pixel usato da un sottotipo video specificato. Questa funzione è valida solo per sottotipi RGB non compressi.
ms.assetid: 876b91c8-50ba-4217-b79c-7f7ec1c22b83
title: Funzione GetBitCount (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fed9b24ebf2e95b2408de30a407904e6bd3c1c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328251"
---
# <a name="getbitcount-function"></a><span data-ttu-id="14f7a-104">GetBitCount (funzione)</span><span class="sxs-lookup"><span data-stu-id="14f7a-104">GetBitCount function</span></span>

<span data-ttu-id="14f7a-105">La `GetBitCount` funzione restituisce il numero di bit per pixel utilizzato da un sottotipo video specificato.</span><span class="sxs-lookup"><span data-stu-id="14f7a-105">The `GetBitCount` function returns the number of bits per pixel used by a specified video subtype.</span></span> <span data-ttu-id="14f7a-106">Questa funzione è valida solo per sottotipi RGB non compressi.</span><span class="sxs-lookup"><span data-stu-id="14f7a-106">This function is valid for uncompressed RGB subtypes only.</span></span>

## <a name="syntax"></a><span data-ttu-id="14f7a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14f7a-107">Syntax</span></span>


```C++
WORD GetBitCount(
   const GUID *pSubtype
);
```



## <a name="parameters"></a><span data-ttu-id="14f7a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="14f7a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14f7a-109">*pSubtype*</span><span class="sxs-lookup"><span data-stu-id="14f7a-109">*pSubtype*</span></span> 
</dt> <dd>

<span data-ttu-id="14f7a-110">Puntatore a un **GUID** del sottotipo video.</span><span class="sxs-lookup"><span data-stu-id="14f7a-110">Pointer to a video subtype **GUID**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14f7a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14f7a-111">Return value</span></span>

<span data-ttu-id="14f7a-112">Restituisce il numero di bit per pixel per questo sottotipo oppure il valore **USHRT \_ Max** se il sottotipo non è riconosciuto.</span><span class="sxs-lookup"><span data-stu-id="14f7a-112">Returns the number of bits per pixel for this subtype, or the value **USHRT\_MAX** if the subtype is not recognized.</span></span>

## <a name="requirements"></a><span data-ttu-id="14f7a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14f7a-113">Requirements</span></span>



| <span data-ttu-id="14f7a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="14f7a-114">Requirement</span></span> | <span data-ttu-id="14f7a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="14f7a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14f7a-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14f7a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="14f7a-117"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14f7a-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="14f7a-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="14f7a-118">Library</span></span><br/> | <dl> <span data-ttu-id="14f7a-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="14f7a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14f7a-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14f7a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14f7a-121">Funzioni video e immagine</span><span class="sxs-lookup"><span data-stu-id="14f7a-121">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




