---
description: Indica la fine dell'arrivo degli esempi nel renderer, in unità di tempo di riferimento. Sintassi.
ms.assetid: 7b30fbe1-5e57-4aa4-8e87-ddd584f186e4
title: 'Membro CVideoTransformFilter:: m_itrLate (Vtrans. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_itrLate
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3ed93a4612d8fa5d4fe79239c6a7f4f5e479717
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330190"
---
# <a name="cvideotransformfilterm_itrlate-member"></a><span data-ttu-id="9da11-104">Membro itrLate di CVideoTransformFilter:: m \_</span><span class="sxs-lookup"><span data-stu-id="9da11-104">CVideoTransformFilter::m\_itrLate member</span></span>

<span data-ttu-id="9da11-105">Indica la fine dell'arrivo degli esempi nel renderer, in unità di tempo di riferimento.</span><span class="sxs-lookup"><span data-stu-id="9da11-105">Indicates how late the samples are arriving at the renderer, in reference time units.</span></span> <span data-ttu-id="9da11-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9da11-106">Syntax</span></span>

## <a name="syntax"></a><span data-ttu-id="9da11-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9da11-107">Syntax</span></span>


```C++
int m_itrLate;
```



## <a name="remarks"></a><span data-ttu-id="9da11-108">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="9da11-108">Remarks</span></span>

<span data-ttu-id="9da11-109">Quando il filtro riceve un messaggio di qualità da downstream, archivia il valore di latenza in questa variabile.</span><span class="sxs-lookup"><span data-stu-id="9da11-109">When the filter receives a quality message from downstream, it stores the lateness value in this variable.</span></span> <span data-ttu-id="9da11-110">Quando il filtro elimina i frame, questo valore viene aggiornato sottraendo la durata di ogni fotogramma.</span><span class="sxs-lookup"><span data-stu-id="9da11-110">As the filter drops frames, it updates this value by subtracting the duration of each frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="9da11-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9da11-111">Requirements</span></span>



| <span data-ttu-id="9da11-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="9da11-112">Requirement</span></span> | <span data-ttu-id="9da11-113">Valore</span><span class="sxs-lookup"><span data-stu-id="9da11-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9da11-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9da11-114">Header</span></span><br/>  | <dl> <span data-ttu-id="9da11-115"><dt>Vtrans. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9da11-115"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9da11-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="9da11-116">Library</span></span><br/> | <dl> <span data-ttu-id="9da11-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9da11-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9da11-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9da11-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9da11-119">**Classe CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="9da11-119">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




