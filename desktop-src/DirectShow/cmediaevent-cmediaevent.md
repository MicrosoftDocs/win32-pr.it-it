---
description: 'Costruttore CMediaEvent.CMediaEvent : metodo costruttore.'
ms.assetid: 7f7a0a9f-e531-4e22-8601-b84ab088e9e7
title: Costruttore CMediaEvent.CMediaEvent (Ctlutil.h)
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
ms.openlocfilehash: 36cd82b086241012542701001c4de1fe16ac2d8e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095559"
---
# <a name="cmediaeventcmediaevent-constructor"></a><span data-ttu-id="8d8b1-103">Costruttore CMediaEvent.CMediaEvent</span><span class="sxs-lookup"><span data-stu-id="8d8b1-103">CMediaEvent.CMediaEvent constructor</span></span>

<span data-ttu-id="8d8b1-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="8d8b1-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d8b1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8d8b1-105">Syntax</span></span>


```C++
CMediaEvent(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="8d8b1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8d8b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d8b1-107">*Pname*</span><span class="sxs-lookup"><span data-stu-id="8d8b1-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="8d8b1-108">Puntatore al nome dell'oggetto a scopo di debug.</span><span class="sxs-lookup"><span data-stu-id="8d8b1-108">Pointer to the name of the object for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="8d8b1-109">*Punk*</span><span class="sxs-lookup"><span data-stu-id="8d8b1-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="8d8b1-110">Puntatore al proprietario dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8d8b1-110">Pointer to the owner of this object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d8b1-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="8d8b1-111">Remarks</span></span>

<span data-ttu-id="8d8b1-112">Allocare *il parametro pName* nella memoria statica.</span><span class="sxs-lookup"><span data-stu-id="8d8b1-112">Allocate the *pName* parameter in static memory.</span></span> <span data-ttu-id="8d8b1-113">Questo nome viene visualizzato nel terminale di debug al momento della creazione e dell'eliminazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8d8b1-113">This name appears on the debugging terminal upon creation and deletion of the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d8b1-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d8b1-114">Requirements</span></span>



| <span data-ttu-id="8d8b1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d8b1-115">Requirement</span></span> | <span data-ttu-id="8d8b1-116">Valore</span><span class="sxs-lookup"><span data-stu-id="8d8b1-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d8b1-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8d8b1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8d8b1-118"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="8d8b1-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8d8b1-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="8d8b1-119">Library</span></span><br/> | <dl> <span data-ttu-id="8d8b1-120"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8d8b1-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d8b1-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d8b1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d8b1-122">**Classe CMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="8d8b1-122">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




