---
description: 'Distruttore CBaseObject.~CBaseObject : metodo del distruttore.'
ms.assetid: 3714d030-f0bd-4826-a3c5-fc206bb88561
title: Distruttore CBaseObject.~CBaseObject (Combase.h)
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
ms.openlocfilehash: 552dbcc764f335e639cb50e2e01411dee200068f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096239"
---
# <a name="cbaseobjectcbaseobject-destructor"></a><span data-ttu-id="ec2f7-103">Distruttore CBaseObject.~CBaseObject</span><span class="sxs-lookup"><span data-stu-id="ec2f7-103">CBaseObject.~CBaseObject destructor</span></span>

<span data-ttu-id="ec2f7-104">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="ec2f7-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec2f7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec2f7-105">Syntax</span></span>


```C++
~CBaseObject();
```



## <a name="remarks"></a><span data-ttu-id="ec2f7-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="ec2f7-106">Remarks</span></span>

<span data-ttu-id="ec2f7-107">Questo metodo decrementa il numero di oggetti attivi.</span><span class="sxs-lookup"><span data-stu-id="ec2f7-107">This method decrements the active-object count.</span></span> <span data-ttu-id="ec2f7-108">Vedere [**CBaseObject::ObjectsActive.**](cbaseobject-objectsactive.md)</span><span class="sxs-lookup"><span data-stu-id="ec2f7-108">(See [**CBaseObject::ObjectsActive**](cbaseobject-objectsactive.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="ec2f7-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec2f7-109">Requirements</span></span>



| <span data-ttu-id="ec2f7-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec2f7-110">Requirement</span></span> | <span data-ttu-id="ec2f7-111">Valore</span><span class="sxs-lookup"><span data-stu-id="ec2f7-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec2f7-112">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec2f7-112">Header</span></span><br/>  | <dl> <span data-ttu-id="ec2f7-113"><dt>Combase.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec2f7-113"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ec2f7-114">Libreria</span><span class="sxs-lookup"><span data-stu-id="ec2f7-114">Library</span></span><br/> | <dl> <span data-ttu-id="ec2f7-115"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ec2f7-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec2f7-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec2f7-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec2f7-117">**Classe CBaseObject**</span><span class="sxs-lookup"><span data-stu-id="ec2f7-117">**CBaseObject Class**</span></span>](cbaseobject.md)
</dt> </dl>

 

 




