---
description: Puntatore a una \_ struttura di filtro AMOVIESETUP.
ms.assetid: 72db601b-78a3-484a-a27f-147ec36022ab
title: 'Membro CFactoryTemplate:: m_pAMovieSetup_Filter (ComBase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAMovieSetup_Filter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 087612acf99a41966ccd98d3b41d2b83255a86f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329816"
---
# <a name="cfactorytemplatem_pamoviesetup_filter-member"></a><span data-ttu-id="9a236-103">\_Membro del filtro pAMovieSetup di CFactoryTemplate:: m \_</span><span class="sxs-lookup"><span data-stu-id="9a236-103">CFactoryTemplate::m\_pAMovieSetup\_Filter member</span></span>

<span data-ttu-id="9a236-104">Puntatore a una struttura di [**\_ filtro AMOVIESETUP**](amoviesetup-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="9a236-104">Pointer to an [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a236-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a236-105">Syntax</span></span>


```C++
const AMOVIESETUP_FILTER *m_pAMovieSetup_Filter;
```



## <a name="remarks"></a><span data-ttu-id="9a236-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="9a236-106">Remarks</span></span>

<span data-ttu-id="9a236-107">Usare questa struttura per applicare un filtro a una registrazione automatica.</span><span class="sxs-lookup"><span data-stu-id="9a236-107">Use this structure to make a filter self-registering.</span></span> <span data-ttu-id="9a236-108">Se il componente non è un filtro, questa variabile membro può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="9a236-108">If your component is not a filter, this member variable can be **NULL**.</span></span> <span data-ttu-id="9a236-109">Per altre informazioni, vedere How to register DirectShow Filters.</span><span class="sxs-lookup"><span data-stu-id="9a236-109">For more information, see How to Register DirectShow Filters.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a236-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a236-110">Requirements</span></span>



| <span data-ttu-id="9a236-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a236-111">Requirement</span></span> | <span data-ttu-id="9a236-112">Valore</span><span class="sxs-lookup"><span data-stu-id="9a236-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a236-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9a236-113">Header</span></span><br/>  | <dl> <span data-ttu-id="9a236-114"><dt>ComBase. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9a236-114"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9a236-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="9a236-115">Library</span></span><br/> | <dl> <span data-ttu-id="9a236-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9a236-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a236-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9a236-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a236-118">**Classe CFactoryTemplate**</span><span class="sxs-lookup"><span data-stu-id="9a236-118">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




