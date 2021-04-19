---
description: Il metodo AllocFormatBuffer alloca memoria per il blocco di formato.
ms.assetid: 5ff716c7-f9cf-4b1c-9d3a-62ab955c1392
title: Metodo CMediaType. AllocFormatBuffer (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.AllocFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6a9314fd06734adcc367b7be34dc8d6d1b9d996
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324021"
---
# <a name="cmediatypeallocformatbuffer-method"></a><span data-ttu-id="4f6c5-103">CMediaType. AllocFormatBuffer, metodo</span><span class="sxs-lookup"><span data-stu-id="4f6c5-103">CMediaType.AllocFormatBuffer method</span></span>

<span data-ttu-id="4f6c5-104">Il `AllocFormatBuffer` metodo alloca memoria per il blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="4f6c5-104">The `AllocFormatBuffer` method allocates memory for the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f6c5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f6c5-105">Syntax</span></span>


```C++
BYTE* AllocFormatBuffer(
   ULONG length
);
```



## <a name="parameters"></a><span data-ttu-id="4f6c5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4f6c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f6c5-107">*length*</span><span class="sxs-lookup"><span data-stu-id="4f6c5-107">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="4f6c5-108">Dimensioni richieste per il blocco di formato, in byte.</span><span class="sxs-lookup"><span data-stu-id="4f6c5-108">Size required for the format block, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f6c5-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4f6c5-109">Return value</span></span>

<span data-ttu-id="4f6c5-110">Restituisce un puntatore al nuovo blocco in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4f6c5-110">Returns a pointer to the new block if successful.</span></span> <span data-ttu-id="4f6c5-111">In caso contrario, restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="4f6c5-111">Otherwise, returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f6c5-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f6c5-112">Remarks</span></span>

<span data-ttu-id="4f6c5-113">Se il metodo esegue correttamente l'allocazione di un nuovo blocco di formato, libera il blocco di formato esistente.</span><span class="sxs-lookup"><span data-stu-id="4f6c5-113">If the method successfully allocates a new format block, it frees the existing format block.</span></span> <span data-ttu-id="4f6c5-114">Se l'allocazione ha esito negativo, il metodo lascia il blocco di formato esistente.</span><span class="sxs-lookup"><span data-stu-id="4f6c5-114">If the allocation fails, the method leaves the existing format block.</span></span>

<span data-ttu-id="4f6c5-115">Il metodo aggiorna i membri **cbFormat** e **pbFormat** della struttura **del \_ \_ tipo di supporto am** .</span><span class="sxs-lookup"><span data-stu-id="4f6c5-115">The method updates the **cbFormat** and **pbFormat** members of the **AM\_MEDIA\_TYPE** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f6c5-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f6c5-116">Requirements</span></span>



| <span data-ttu-id="4f6c5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f6c5-117">Requirement</span></span> | <span data-ttu-id="4f6c5-118">Valore</span><span class="sxs-lookup"><span data-stu-id="4f6c5-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f6c5-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4f6c5-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4f6c5-120"><dt>Mtype. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f6c5-120"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="4f6c5-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="4f6c5-121">Library</span></span><br/> | <dl> <span data-ttu-id="4f6c5-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4f6c5-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f6c5-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f6c5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f6c5-124">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="4f6c5-124">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




