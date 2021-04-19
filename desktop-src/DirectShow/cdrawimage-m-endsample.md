---
description: La \_ variabile membro EndSample m specifica l'ora di arresto dell'esempio più recente.
ms.assetid: 694815b6-8da5-4174-b2c7-7d686a557c6c
title: 'Membro CDrawImage:: m_EndSample (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_EndSample
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 78268e8335d6dd8c24497a9e4d74b0caab205a99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328946"
---
# <a name="cdrawimagem_endsample-member"></a><span data-ttu-id="1b339-103">Membro EndSample di CDrawImage:: m \_</span><span class="sxs-lookup"><span data-stu-id="1b339-103">CDrawImage::m\_EndSample member</span></span>

<span data-ttu-id="1b339-104">La `m_EndSample` variabile membro specifica l'ora di arresto dell'esempio più recente.</span><span class="sxs-lookup"><span data-stu-id="1b339-104">The `m_EndSample` member variable specifies the stop time of the most recent sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b339-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1b339-105">Syntax</span></span>


```C++
CRefTime m_EndSample;
```



## <a name="remarks"></a><span data-ttu-id="1b339-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="1b339-106">Remarks</span></span>

<span data-ttu-id="1b339-107">Il valore è valido solo all'interno del metodo [**CDrawImage::D isplaysampletimes**](cdrawimage-displaysampletimes.md) .</span><span class="sxs-lookup"><span data-stu-id="1b339-107">The value is only valid inside the [**CDrawImage::DisplaySampleTimes**](cdrawimage-displaysampletimes.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b339-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1b339-108">Requirements</span></span>



| <span data-ttu-id="1b339-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b339-109">Requirement</span></span> | <span data-ttu-id="1b339-110">Valore</span><span class="sxs-lookup"><span data-stu-id="1b339-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b339-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1b339-111">Header</span></span><br/>  | <dl> <span data-ttu-id="1b339-112"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1b339-112"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1b339-113">Libreria</span><span class="sxs-lookup"><span data-stu-id="1b339-113">Library</span></span><br/> | <dl> <span data-ttu-id="1b339-114"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1b339-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b339-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1b339-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b339-116">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="1b339-116">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




