---
description: La \_ variabile membro bModifiesData m indica se il filtro modifica i dati di esempio ricevuti. Il valore viene impostato nel costruttore CTransInPlaceFilter, ma il valore predefinito è TRUE.
ms.assetid: 8ccdba46-315f-4519-b363-6870d1217f98
title: 'Membro CTransInPlaceFilter:: m_bModifiesData (Transip. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bModifiesData
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5bc0d630fd0eda6e9915f8c11f5b15d21b725ce8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328169"
---
# <a name="ctransinplacefilterm_bmodifiesdata-member"></a><span data-ttu-id="e44ed-104">Membro bModifiesData di CTransInPlaceFilter:: m \_</span><span class="sxs-lookup"><span data-stu-id="e44ed-104">CTransInPlaceFilter::m\_bModifiesData member</span></span>

<span data-ttu-id="e44ed-105">La `m_bModifiesData` variabile membro indica se il filtro modifica i dati di esempio ricevuti.</span><span class="sxs-lookup"><span data-stu-id="e44ed-105">The `m_bModifiesData` member variable indicates whether the filter modifies the sample data that is receives.</span></span> <span data-ttu-id="e44ed-106">Il valore viene impostato nel costruttore **CTransInPlaceFilter** , ma il valore predefinito è **true**.</span><span class="sxs-lookup"><span data-stu-id="e44ed-106">The value is set in the **CTransInPlaceFilter** constructor, but defaults to **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e44ed-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e44ed-107">Syntax</span></span>


```C++
bool m_bModifiesData;
```



## <a name="remarks"></a><span data-ttu-id="e44ed-108">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="e44ed-108">Remarks</span></span>

<span data-ttu-id="e44ed-109">Questa variabile influiscono sul modo in cui il filtro negozia l'allocatore.</span><span class="sxs-lookup"><span data-stu-id="e44ed-109">This variable affects how the filter negotiates the allocator.</span></span> <span data-ttu-id="e44ed-110">Se il valore è **true**, il filtro non può utilizzare un allocatore di sola lettura per entrambe le connessioni pin.</span><span class="sxs-lookup"><span data-stu-id="e44ed-110">If the value is **TRUE**, the filter cannot use a read-only allocator for both pin connections.</span></span>

## <a name="requirements"></a><span data-ttu-id="e44ed-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e44ed-111">Requirements</span></span>



| <span data-ttu-id="e44ed-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e44ed-112">Requirement</span></span> | <span data-ttu-id="e44ed-113">Valore</span><span class="sxs-lookup"><span data-stu-id="e44ed-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e44ed-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e44ed-114">Header</span></span><br/>  | <dl> <span data-ttu-id="e44ed-115"><dt>Transip. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e44ed-115"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e44ed-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="e44ed-116">Library</span></span><br/> | <dl> <span data-ttu-id="e44ed-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e44ed-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e44ed-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e44ed-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e44ed-119">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="e44ed-119">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




