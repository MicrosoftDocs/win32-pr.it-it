---
description: Il metodo ReallocFormatBuffer rialloca il blocco di formato in una nuova dimensione.
ms.assetid: 49bec677-09cc-4e1a-994a-13e873e61713
title: Metodo CMediaType. ReallocFormatBuffer (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.ReallocFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22e861c61f01a7594d720833e2b3a4b923a1e183
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325517"
---
# <a name="cmediatypereallocformatbuffer-method"></a><span data-ttu-id="3adfc-103">CMediaType. ReallocFormatBuffer, metodo</span><span class="sxs-lookup"><span data-stu-id="3adfc-103">CMediaType.ReallocFormatBuffer method</span></span>

<span data-ttu-id="3adfc-104">Il metodo rialloca `ReallocFormatBuffer` il blocco di formato in una nuova dimensione.</span><span class="sxs-lookup"><span data-stu-id="3adfc-104">The `ReallocFormatBuffer` method reallocates the format block to a new size.</span></span>

## <a name="syntax"></a><span data-ttu-id="3adfc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3adfc-105">Syntax</span></span>


```C++
BYTE* ReallocFormatBuffer(
   ULONG length
);
```



## <a name="parameters"></a><span data-ttu-id="3adfc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3adfc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3adfc-107">*length*</span><span class="sxs-lookup"><span data-stu-id="3adfc-107">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="3adfc-108">Nuove dimensioni richieste per il blocco di formato, in byte.</span><span class="sxs-lookup"><span data-stu-id="3adfc-108">New size required for the format block, in bytes.</span></span> <span data-ttu-id="3adfc-109">Deve essere maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="3adfc-109">Must be greater than zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3adfc-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3adfc-110">Return value</span></span>

<span data-ttu-id="3adfc-111">Restituisce un puntatore al nuovo blocco in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="3adfc-111">Returns a pointer to the new block if successful.</span></span> <span data-ttu-id="3adfc-112">In caso contrario, restituisce un puntatore al blocco di formato precedente o **null**.</span><span class="sxs-lookup"><span data-stu-id="3adfc-112">Otherwise, returns either a pointer to the old format block, or **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3adfc-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="3adfc-113">Remarks</span></span>

<span data-ttu-id="3adfc-114">Questo metodo alloca un nuovo blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="3adfc-114">This method allocates a new format block.</span></span> <span data-ttu-id="3adfc-115">Viene copiato il maggior volume possibile del blocco di formato esistente nel nuovo blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="3adfc-115">It copies as much of the existing format block as possible into the new format block.</span></span> <span data-ttu-id="3adfc-116">Se il nuovo blocco è più piccolo del blocco esistente, il blocco di formato esistente viene troncato.</span><span class="sxs-lookup"><span data-stu-id="3adfc-116">If the new block is smaller than the existing block, the existing format block is truncated.</span></span> <span data-ttu-id="3adfc-117">Se il nuovo blocco è più grande, il contenuto dello spazio aggiuntivo non è definito.</span><span class="sxs-lookup"><span data-stu-id="3adfc-117">If the new block is larger, the contents of the additional space are undefined.</span></span> <span data-ttu-id="3adfc-118">Non vengono impostate in modo esplicito su zero.</span><span class="sxs-lookup"><span data-stu-id="3adfc-118">They are not explicitly set to zero.</span></span>

<span data-ttu-id="3adfc-119">Il metodo aggiorna i membri **cbFormat** e **pbFormat** della struttura **del \_ \_ tipo di supporto am** .</span><span class="sxs-lookup"><span data-stu-id="3adfc-119">The method updates the **cbFormat** and **pbFormat** members of the **AM\_MEDIA\_TYPE** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3adfc-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3adfc-120">Requirements</span></span>



| <span data-ttu-id="3adfc-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3adfc-121">Requirement</span></span> | <span data-ttu-id="3adfc-122">Valore</span><span class="sxs-lookup"><span data-stu-id="3adfc-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3adfc-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3adfc-123">Header</span></span><br/>  | <dl> <span data-ttu-id="3adfc-124"><dt>Mtype. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3adfc-124"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="3adfc-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="3adfc-125">Library</span></span><br/> | <dl> <span data-ttu-id="3adfc-126"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3adfc-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3adfc-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3adfc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3adfc-128">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="3adfc-128">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




