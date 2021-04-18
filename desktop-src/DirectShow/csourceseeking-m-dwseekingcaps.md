---
description: Funzionalità di ricerca.
ms.assetid: c849db20-7567-41e0-9a57-85070a6e6a3a
title: 'Membro CSourceSeeking:: m_dwSeekingCaps (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwSeekingCaps
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4addb06b120801b0d5e697c7df93ab8ba620bbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329489"
---
# <a name="csourceseekingm_dwseekingcaps-member"></a><span data-ttu-id="8eeb0-103">Membro dwSeekingCaps di CSourceSeeking:: m \_</span><span class="sxs-lookup"><span data-stu-id="8eeb0-103">CSourceSeeking::m\_dwSeekingCaps member</span></span>

<span data-ttu-id="8eeb0-104">Funzionalità di ricerca.</span><span class="sxs-lookup"><span data-stu-id="8eeb0-104">Seeking capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eeb0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8eeb0-105">Syntax</span></span>


```C++
DWORD m_dwSeekingCaps;
```



## <a name="remarks"></a><span data-ttu-id="8eeb0-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="8eeb0-106">Remarks</span></span>

<span data-ttu-id="8eeb0-107">Per impostazione predefinita, il valore è impostato sulla combinazione bit per bit dei flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="8eeb0-107">By default, the value is set to the bitwise combination of the following flags:</span></span>

-   <span data-ttu-id="8eeb0-108">\_Ricerca di \_ CanSeekForwards</span><span class="sxs-lookup"><span data-stu-id="8eeb0-108">AM\_SEEKING\_CanSeekForwards</span></span>
-   <span data-ttu-id="8eeb0-109">\_Ricerca di \_ CanSeekBackwards</span><span class="sxs-lookup"><span data-stu-id="8eeb0-109">AM\_SEEKING\_CanSeekBackwards</span></span>
-   <span data-ttu-id="8eeb0-110">\_Ricerca di \_ CanSeekAbsolute</span><span class="sxs-lookup"><span data-stu-id="8eeb0-110">AM\_SEEKING\_CanSeekAbsolute</span></span>
-   <span data-ttu-id="8eeb0-111">\_Ricerca di \_ CanGetStopPos</span><span class="sxs-lookup"><span data-stu-id="8eeb0-111">AM\_SEEKING\_CanGetStopPos</span></span>
-   <span data-ttu-id="8eeb0-112">\_Ricerca di \_ CanGetDuration</span><span class="sxs-lookup"><span data-stu-id="8eeb0-112">AM\_SEEKING\_CanGetDuration</span></span>

<span data-ttu-id="8eeb0-113">Se il filtro supporta un set di funzionalità diverso, eseguire l'override di questo valore.</span><span class="sxs-lookup"><span data-stu-id="8eeb0-113">If the filter supports a different set of capabilities, override this value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8eeb0-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8eeb0-114">Requirements</span></span>



| <span data-ttu-id="8eeb0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8eeb0-115">Requirement</span></span> | <span data-ttu-id="8eeb0-116">Valore</span><span class="sxs-lookup"><span data-stu-id="8eeb0-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eeb0-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8eeb0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8eeb0-118"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8eeb0-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8eeb0-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="8eeb0-119">Library</span></span><br/> | <dl> <span data-ttu-id="8eeb0-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8eeb0-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8eeb0-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8eeb0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eeb0-122">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="8eeb0-122">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




