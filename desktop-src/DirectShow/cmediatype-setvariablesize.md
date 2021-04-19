---
description: Il metodo SetVariableSize specifica che gli esempi non hanno dimensioni fisse.
ms.assetid: 2a207cdb-f8e6-44aa-8bf6-868267aeb42d
title: Metodo CMediaType. SetVariableSize (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetVariableSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4621a639b3bc18382bc41ae9425c4de50db920ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333070"
---
# <a name="cmediatypesetvariablesize-method"></a><span data-ttu-id="16e23-103">CMediaType. SetVariableSize, metodo</span><span class="sxs-lookup"><span data-stu-id="16e23-103">CMediaType.SetVariableSize method</span></span>

<span data-ttu-id="16e23-104">Il `SetVariableSize` metodo specifica che gli esempi non hanno dimensioni fisse.</span><span class="sxs-lookup"><span data-stu-id="16e23-104">The `SetVariableSize` method specifies that samples do not have a fixed size.</span></span>

## <a name="syntax"></a><span data-ttu-id="16e23-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="16e23-105">Syntax</span></span>


```C++
void SetVariableSize();
```



## <a name="parameters"></a><span data-ttu-id="16e23-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="16e23-106">Parameters</span></span>

<span data-ttu-id="16e23-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="16e23-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="16e23-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="16e23-108">Return value</span></span>

<span data-ttu-id="16e23-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="16e23-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="16e23-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="16e23-110">Remarks</span></span>

<span data-ttu-id="16e23-111">Questo metodo imposta il membro **bFixedSizeSamples** su **false**.</span><span class="sxs-lookup"><span data-stu-id="16e23-111">This method sets the **bFixedSizeSamples** member to **FALSE**.</span></span> <span data-ttu-id="16e23-112">Le chiamate successive al metodo [**CMediaType:: GetSampleSize**](cmediatype-getsamplesize.md) restituiscono zero.</span><span class="sxs-lookup"><span data-stu-id="16e23-112">Subsequent calls to the [**CMediaType::GetSampleSize**](cmediatype-getsamplesize.md) method return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="16e23-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16e23-113">Requirements</span></span>



| <span data-ttu-id="16e23-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="16e23-114">Requirement</span></span> | <span data-ttu-id="16e23-115">Valore</span><span class="sxs-lookup"><span data-stu-id="16e23-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16e23-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="16e23-116">Header</span></span><br/>  | <dl> <span data-ttu-id="16e23-117"><dt>Mtype. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="16e23-117"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="16e23-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="16e23-118">Library</span></span><br/> | <dl> <span data-ttu-id="16e23-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="16e23-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16e23-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16e23-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16e23-121">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="16e23-121">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




