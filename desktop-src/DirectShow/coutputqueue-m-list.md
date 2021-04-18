---
description: Coda di esempio multimediale.
ms.assetid: 910f1c0c-2ce9-452f-a97b-aa424da9a93e
title: 'Membro COutputQueue:: m_List (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_List
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32840ed0ed9f976cceb1e0dc6dc8debc3f774377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328254"
---
# <a name="coutputqueuem_list-member"></a><span data-ttu-id="d0a31-103">Membro elenco COutputQueue:: m \_</span><span class="sxs-lookup"><span data-stu-id="d0a31-103">COutputQueue::m\_List member</span></span>

<span data-ttu-id="d0a31-104">Coda di esempio multimediale.</span><span class="sxs-lookup"><span data-stu-id="d0a31-104">Media sample queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0a31-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0a31-105">Syntax</span></span>


```C++
CSampleList *m_List;
```



## <a name="remarks"></a><span data-ttu-id="d0a31-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="d0a31-106">Remarks</span></span>

<span data-ttu-id="d0a31-107">Questa variabile membro è un puntatore a un oggetto [**CGenericList**](cgenericlist.md) che include puntatori [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) .</span><span class="sxs-lookup"><span data-stu-id="d0a31-107">This member variable is a pointer to a [**CGenericList**](cgenericlist.md) object that holds [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pointers.</span></span> <span data-ttu-id="d0a31-108">Il tipo **CSampleList** è definito come segue:</span><span class="sxs-lookup"><span data-stu-id="d0a31-108">The **CSampleList** type is defined as follows:</span></span>

``` syntax
typedef CGenericList<IMediaSample> CSampleList;
```

## <a name="requirements"></a><span data-ttu-id="d0a31-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0a31-109">Requirements</span></span>



| <span data-ttu-id="d0a31-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0a31-110">Requirement</span></span> | <span data-ttu-id="d0a31-111">Valore</span><span class="sxs-lookup"><span data-stu-id="d0a31-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0a31-112">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0a31-112">Header</span></span><br/>  | <dl> <span data-ttu-id="d0a31-113"><dt>Outputq. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0a31-113"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d0a31-114">Libreria</span><span class="sxs-lookup"><span data-stu-id="d0a31-114">Library</span></span><br/> | <dl> <span data-ttu-id="d0a31-115"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d0a31-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0a31-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0a31-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0a31-117">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="d0a31-117">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




