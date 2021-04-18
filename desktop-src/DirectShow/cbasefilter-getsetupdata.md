---
description: Il metodo GetSetupData recupera i dati di registrazione per il filtro.
ms.assetid: 93582c75-4f40-492c-919c-c8a06dce7715
title: Metodo CBaseFilter. GetSetupData (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetSetupData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40223a22f4de4a078ce84f8ebe49bddd5ab13575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331548"
---
# <a name="cbasefiltergetsetupdata-method"></a><span data-ttu-id="ad072-103">CBaseFilter. GetSetupData, metodo</span><span class="sxs-lookup"><span data-stu-id="ad072-103">CBaseFilter.GetSetupData method</span></span>

<span data-ttu-id="ad072-104">Il `GetSetupData` metodo recupera i dati di registrazione per il filtro.</span><span class="sxs-lookup"><span data-stu-id="ad072-104">The `GetSetupData` method retrieves the registration data for the filter.</span></span>

> [!Note]  
> <span data-ttu-id="ad072-105">Questo metodo è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="ad072-105">This method is obsolete.</span></span> <span data-ttu-id="ad072-106">Viene chiamato dai metodi [**CBaseFilter:: Register**](cbasefilter-register.md) e [**CBaseFilter:: Unregister**](cbasefilter-unregister.md) .</span><span class="sxs-lookup"><span data-stu-id="ad072-106">It is called by the [**CBaseFilter::Register**](cbasefilter-register.md) and [**CBaseFilter::Unregister**](cbasefilter-unregister.md) methods.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ad072-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ad072-107">Syntax</span></span>


```C++
virtual LPAMOVIESETUP_FILTER GetSetupData();
```



## <a name="parameters"></a><span data-ttu-id="ad072-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ad072-108">Parameters</span></span>

<span data-ttu-id="ad072-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="ad072-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ad072-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ad072-110">Return value</span></span>

<span data-ttu-id="ad072-111">Restituisce un puntatore a una struttura di [**\_ filtro AMOVIESETUP**](amoviesetup-filter.md) contenente le informazioni di registrazione per il filtro.</span><span class="sxs-lookup"><span data-stu-id="ad072-111">Returns a pointer to an [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) structure containing registration information for the filter.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad072-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad072-112">Remarks</span></span>

<span data-ttu-id="ad072-113">La classe base restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="ad072-113">The base class returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad072-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad072-114">Requirements</span></span>



| <span data-ttu-id="ad072-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad072-115">Requirement</span></span> | <span data-ttu-id="ad072-116">Valore</span><span class="sxs-lookup"><span data-stu-id="ad072-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad072-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ad072-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ad072-118"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad072-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ad072-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="ad072-119">Library</span></span><br/> | <dl> <span data-ttu-id="ad072-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ad072-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad072-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad072-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad072-122">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="ad072-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




