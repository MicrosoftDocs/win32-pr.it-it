---
description: Metodo del distruttore.
ms.assetid: 3714d030-f0bd-4826-a3c5-fc206bb88561
title: Distruttore CBaseObject. ~ CBaseObject (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject.~CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 908f335105fa88f3ed547eed0e92ea50a6f85f26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325524"
---
# <a name="cbaseobjectcbaseobject-destructor"></a><span data-ttu-id="747d0-103">Distruttore CBaseObject. ~ CBaseObject</span><span class="sxs-lookup"><span data-stu-id="747d0-103">CBaseObject.~CBaseObject destructor</span></span>

<span data-ttu-id="747d0-104">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="747d0-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="747d0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="747d0-105">Syntax</span></span>


```C++
~CBaseObject();
```



## <a name="remarks"></a><span data-ttu-id="747d0-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="747d0-106">Remarks</span></span>

<span data-ttu-id="747d0-107">Questo metodo decrementa il conteggio degli oggetti attivi.</span><span class="sxs-lookup"><span data-stu-id="747d0-107">This method decrements the active-object count.</span></span> <span data-ttu-id="747d0-108">Vedere [**CBaseObject:: ObjectsActive**](cbaseobject-objectsactive.md).</span><span class="sxs-lookup"><span data-stu-id="747d0-108">(See [**CBaseObject::ObjectsActive**](cbaseobject-objectsactive.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="747d0-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="747d0-109">Requirements</span></span>



| <span data-ttu-id="747d0-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="747d0-110">Requirement</span></span> | <span data-ttu-id="747d0-111">Valore</span><span class="sxs-lookup"><span data-stu-id="747d0-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="747d0-112">Intestazione</span><span class="sxs-lookup"><span data-stu-id="747d0-112">Header</span></span><br/>  | <dl> <span data-ttu-id="747d0-113"><dt>ComBase. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="747d0-113"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="747d0-114">Libreria</span><span class="sxs-lookup"><span data-stu-id="747d0-114">Library</span></span><br/> | <dl> <span data-ttu-id="747d0-115"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="747d0-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="747d0-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="747d0-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="747d0-117">**Classe CBaseObject**</span><span class="sxs-lookup"><span data-stu-id="747d0-117">**CBaseObject Class**</span></span>](cbaseobject.md)
</dt> </dl>

 

 




