---
description: Il metodo CancelNotification Annulla l'evento timer che pianifica il rendering.
ms.assetid: 56ddf692-a2e3-40f2-848f-2d592601ec00
title: Metodo CBaseRenderer. CancelNotification (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CancelNotification
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3330f369c5fcc45fe051a1964a504d5d40fcd091
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329403"
---
# <a name="cbaserenderercancelnotification-method"></a><span data-ttu-id="c0d7b-103">CBaseRenderer. CancelNotification, metodo</span><span class="sxs-lookup"><span data-stu-id="c0d7b-103">CBaseRenderer.CancelNotification method</span></span>

<span data-ttu-id="c0d7b-104">Il `CancelNotification` metodo annulla l'evento timer che pianifica il rendering.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-104">The `CancelNotification` method cancels the timer event that schedules rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0d7b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c0d7b-105">Syntax</span></span>


```C++
virtual HRESULT CancelNotification();
```



## <a name="parameters"></a><span data-ttu-id="c0d7b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c0d7b-106">Parameters</span></span>

<span data-ttu-id="c0d7b-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c0d7b-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c0d7b-108">Return value</span></span>

<span data-ttu-id="c0d7b-109">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="c0d7b-110">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c0d7b-110">Return code</span></span>                                                                             | <span data-ttu-id="c0d7b-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0d7b-111">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c0d7b-112"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="c0d7b-112"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="c0d7b-113">Nessun evento timer in sospeso.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-113">There was no pending timer event.</span></span><br/> |
| <dl> <span data-ttu-id="c0d7b-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c0d7b-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="c0d7b-115">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-115">Success.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="c0d7b-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="c0d7b-116">Remarks</span></span>

<span data-ttu-id="c0d7b-117">Il filtro chiama questo metodo quando il flusso viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-117">The filter calls this method when streaming stops.</span></span> <span data-ttu-id="c0d7b-118">Il metodo annulla qualsiasi rendering pianificato.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-118">The method cancels any scheduled rendering.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0d7b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0d7b-119">Requirements</span></span>



| <span data-ttu-id="c0d7b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0d7b-120">Requirement</span></span> | <span data-ttu-id="c0d7b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c0d7b-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0d7b-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c0d7b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c0d7b-123"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c0d7b-123"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c0d7b-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="c0d7b-124">Library</span></span><br/> | <dl> <span data-ttu-id="c0d7b-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c0d7b-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0d7b-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0d7b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0d7b-127">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="c0d7b-127">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




