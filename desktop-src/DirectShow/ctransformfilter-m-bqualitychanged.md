---
description: Flag che indica se la qualità è stata modificata.
ms.assetid: 9084ab1d-b6a0-4e87-a653-86e64c74b07f
title: 'Membro CTransformFilter:: m_bQualityChanged (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bQualityChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abd0371389d6c17a074580643a06c3fe25bdf433
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331145"
---
# <a name="ctransformfilterm_bqualitychanged-member"></a><span data-ttu-id="a3bb4-103">Membro bQualityChanged di CTransformFilter:: m \_</span><span class="sxs-lookup"><span data-stu-id="a3bb4-103">CTransformFilter::m\_bQualityChanged member</span></span>

<span data-ttu-id="a3bb4-104">Flag che indica se la qualità è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="a3bb4-104">Flag that indicates whether the quality has changed.</span></span> <span data-ttu-id="a3bb4-105">La prima volta che il filtro elimina un campione, invia un evento [**di \_ \_ modifica della qualità EC**](ec-quality-change.md) al gestore del grafico del filtro e imposta questo flag su **true**.</span><span class="sxs-lookup"><span data-stu-id="a3bb4-105">The first time that the filter drops a sample, it sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the filter graph manager and sets this flag to **TRUE**.</span></span> <span data-ttu-id="a3bb4-106">Questo evento non viene inviato di nuovo fino a quando il filtro non viene arrestato e riavviato, anche se nel frattempo continua a eliminare i campioni.</span><span class="sxs-lookup"><span data-stu-id="a3bb4-106">It does not send this event again until the filter stops and restarts, even if it continues to drop samples in the meantime.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3bb4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3bb4-107">Syntax</span></span>


```C++
BOOL m_bQualityChanged;
```



## <a name="requirements"></a><span data-ttu-id="a3bb4-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3bb4-108">Requirements</span></span>



| <span data-ttu-id="a3bb4-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3bb4-109">Requirement</span></span> | <span data-ttu-id="a3bb4-110">Valore</span><span class="sxs-lookup"><span data-stu-id="a3bb4-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3bb4-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3bb4-111">Header</span></span><br/>  | <dl> <span data-ttu-id="a3bb4-112"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3bb4-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a3bb4-113">Libreria</span><span class="sxs-lookup"><span data-stu-id="a3bb4-113">Library</span></span><br/> | <dl> <span data-ttu-id="a3bb4-114"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a3bb4-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3bb4-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3bb4-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3bb4-116">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="a3bb4-116">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




