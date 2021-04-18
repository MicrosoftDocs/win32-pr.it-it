---
description: Il metodo WaitEvent attende fino a quando non viene segnalato l'evento specificato.
ms.assetid: 64880f46-7b8f-4823-9d50-052e30ecf04b
title: Metodo CDynamicOutputPin. WaitEvent (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.WaitEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b27f3c387c82eaeebc119f967deaca8e7314ccd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330405"
---
# <a name="cdynamicoutputpinwaitevent-method"></a><span data-ttu-id="72462-103">CDynamicOutputPin. WaitEvent, metodo</span><span class="sxs-lookup"><span data-stu-id="72462-103">CDynamicOutputPin.WaitEvent method</span></span>

<span data-ttu-id="72462-104">Il `WaitEvent` metodo attende fino a quando non viene segnalato l'evento specificato.</span><span class="sxs-lookup"><span data-stu-id="72462-104">The `WaitEvent` method waits until the specified event is signaled.</span></span>

## <a name="syntax"></a><span data-ttu-id="72462-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="72462-105">Syntax</span></span>


```C++
static HRESULT WaitEvent(
   HANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="72462-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="72462-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72462-107">*hEvent*</span><span class="sxs-lookup"><span data-stu-id="72462-107">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="72462-108">Handle per un evento.</span><span class="sxs-lookup"><span data-stu-id="72462-108">Handle to an event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72462-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="72462-109">Return value</span></span>

<span data-ttu-id="72462-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="72462-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="72462-111">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="72462-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="72462-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="72462-112">Return code</span></span>                                                                                  | <span data-ttu-id="72462-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72462-113">Description</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="72462-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="72462-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="72462-115">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="72462-115">Success.</span></span><br/>          |
| <dl> <span data-ttu-id="72462-116"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="72462-116"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="72462-117">Errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="72462-117">Unexpected error.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="72462-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72462-118">Requirements</span></span>



| <span data-ttu-id="72462-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="72462-119">Requirement</span></span> | <span data-ttu-id="72462-120">Valore</span><span class="sxs-lookup"><span data-stu-id="72462-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72462-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="72462-121">Header</span></span><br/>  | <dl> <span data-ttu-id="72462-122"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="72462-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="72462-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="72462-123">Library</span></span><br/> | <dl> <span data-ttu-id="72462-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="72462-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72462-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72462-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72462-126">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="72462-126">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




