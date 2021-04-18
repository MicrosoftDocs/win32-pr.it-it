---
description: Il metodo SetTemporalCompression specifica se gli esempi vengono compressi con la compressione temporale (interframe).
ms.assetid: cdd181ee-d1e9-48b0-96f6-e76db9f3f933
title: Metodo CMediaType. SetTemporalCompression (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetTemporalCompression
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a0aba07375c5b5c760c432de704562efb2bea148
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328503"
---
# <a name="cmediatypesettemporalcompression-method"></a><span data-ttu-id="e00d0-103">CMediaType. SetTemporalCompression, metodo</span><span class="sxs-lookup"><span data-stu-id="e00d0-103">CMediaType.SetTemporalCompression method</span></span>

<span data-ttu-id="e00d0-104">Il `SetTemporalCompression` metodo specifica se gli esempi vengono compressi con la compressione temporale (interframe).</span><span class="sxs-lookup"><span data-stu-id="e00d0-104">The `SetTemporalCompression` method specifies whether samples are compressed using temporal (interframe) compression.</span></span>

## <a name="syntax"></a><span data-ttu-id="e00d0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e00d0-105">Syntax</span></span>


```C++
void SetTemporalCompression(
   BOOL bCompressed
);
```



## <a name="parameters"></a><span data-ttu-id="e00d0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e00d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e00d0-107">*bCompressed*</span><span class="sxs-lookup"><span data-stu-id="e00d0-107">*bCompressed*</span></span> 
</dt> <dd>

<span data-ttu-id="e00d0-108">Valore booleano che specifica se il flusso usa la compressione temporale.</span><span class="sxs-lookup"><span data-stu-id="e00d0-108">Boolean value that specifies whether the stream uses temporal compression.</span></span> <span data-ttu-id="e00d0-109">Se il flusso usa la compressione temporale, impostare il valore su **true**.</span><span class="sxs-lookup"><span data-stu-id="e00d0-109">If the stream uses temporal compression, set the value to **TRUE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e00d0-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e00d0-110">Return value</span></span>

<span data-ttu-id="e00d0-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e00d0-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e00d0-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="e00d0-112">Remarks</span></span>

<span data-ttu-id="e00d0-113">Questo metodo imposta il membro **bTemporalCompression** .</span><span class="sxs-lookup"><span data-stu-id="e00d0-113">This method sets the **bTemporalCompression** member.</span></span>

## <a name="requirements"></a><span data-ttu-id="e00d0-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e00d0-114">Requirements</span></span>



| <span data-ttu-id="e00d0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e00d0-115">Requirement</span></span> | <span data-ttu-id="e00d0-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e00d0-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e00d0-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e00d0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e00d0-118"><dt>Mtype. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e00d0-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="e00d0-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="e00d0-119">Library</span></span><br/> | <dl> <span data-ttu-id="e00d0-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e00d0-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e00d0-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e00d0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e00d0-122">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="e00d0-122">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




