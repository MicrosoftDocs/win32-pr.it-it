---
description: Metodo del costruttore.
ms.assetid: 7f7a0a9f-e531-4e22-8601-b84ab088e9e7
title: Costruttore CMediaEvent. CMediaEvent (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.CMediaEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77b87fa589728592874b0dea96f7b6efca501471
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328030"
---
# <a name="cmediaeventcmediaevent-constructor"></a><span data-ttu-id="3e130-103">Costruttore CMediaEvent. CMediaEvent</span><span class="sxs-lookup"><span data-stu-id="3e130-103">CMediaEvent.CMediaEvent constructor</span></span>

<span data-ttu-id="3e130-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="3e130-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e130-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e130-105">Syntax</span></span>


```C++
CMediaEvent(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="3e130-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e130-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e130-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="3e130-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="3e130-108">Puntatore al nome dell'oggetto a scopo di debug.</span><span class="sxs-lookup"><span data-stu-id="3e130-108">Pointer to the name of the object for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="3e130-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="3e130-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="3e130-110">Puntatore al proprietario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="3e130-110">Pointer to the owner of this object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e130-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e130-111">Remarks</span></span>

<span data-ttu-id="3e130-112">Allocare il parametro *pname* nella memoria statica.</span><span class="sxs-lookup"><span data-stu-id="3e130-112">Allocate the *pName* parameter in static memory.</span></span> <span data-ttu-id="3e130-113">Questo nome viene visualizzato nel terminale di debug al momento della creazione e dell'eliminazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3e130-113">This name appears on the debugging terminal upon creation and deletion of the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e130-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e130-114">Requirements</span></span>



| <span data-ttu-id="3e130-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e130-115">Requirement</span></span> | <span data-ttu-id="3e130-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3e130-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e130-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e130-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3e130-118"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e130-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3e130-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="3e130-119">Library</span></span><br/> | <dl> <span data-ttu-id="3e130-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3e130-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e130-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e130-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e130-122">**Classe CMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="3e130-122">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




