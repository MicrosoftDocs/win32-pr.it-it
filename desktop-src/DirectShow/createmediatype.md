---
description: La funzione CreateMediaType alloca una nuova \_ \_ struttura del tipo di supporto AM, incluso il blocco di formato.
ms.assetid: 841a8c51-6027-49d6-b3d8-b5e21e3d5f13
title: Funzione CreateMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03ea3eaee03ebf98ac22d702bde9a165fda21e51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331316"
---
# <a name="createmediatype-function"></a><span data-ttu-id="07a30-103">CreateMediaType (funzione)</span><span class="sxs-lookup"><span data-stu-id="07a30-103">CreateMediaType function</span></span>

<span data-ttu-id="07a30-104">La funzione **CreateMediaType** alloca una nuova struttura [**del \_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) , incluso il blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="07a30-104">The **CreateMediaType** function allocates a new [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure, including the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="07a30-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07a30-105">Syntax</span></span>


```C++
AM_MEDIA_TYPE* WINAPI CreateMediaType(
   AM_MEDIA_TYPE const *pSrc
);
```



## <a name="parameters"></a><span data-ttu-id="07a30-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="07a30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07a30-107">*pSrc*</span><span class="sxs-lookup"><span data-stu-id="07a30-107">*pSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="07a30-108">Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="07a30-108">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="07a30-109">Il metodo copia questa struttura nella nuova struttura.</span><span class="sxs-lookup"><span data-stu-id="07a30-109">The method copies this structure into the new structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07a30-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07a30-110">Return value</span></span>

<span data-ttu-id="07a30-111">Restituisce una nuova struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) oppure **null** se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="07a30-111">Returns a new [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure, or **NULL** if there is an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="07a30-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="07a30-112">Remarks</span></span>

<span data-ttu-id="07a30-113">Per liberare la memoria allocata da questa funzione, chiamare [**DeleteMediaType**](deletemediatype.md).</span><span class="sxs-lookup"><span data-stu-id="07a30-113">To free the memory allocated by this function, call [**DeleteMediaType**](deletemediatype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="07a30-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07a30-114">Requirements</span></span>



| <span data-ttu-id="07a30-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="07a30-115">Requirement</span></span> | <span data-ttu-id="07a30-116">Valore</span><span class="sxs-lookup"><span data-stu-id="07a30-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07a30-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07a30-117">Header</span></span><br/>  | <dl> <span data-ttu-id="07a30-118"><dt>Mtype. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="07a30-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="07a30-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="07a30-119">Library</span></span><br/> | <dl> <span data-ttu-id="07a30-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="07a30-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07a30-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07a30-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07a30-122">**Funzioni di tipo multimediale**</span><span class="sxs-lookup"><span data-stu-id="07a30-122">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

 




