---
description: "Metodo CPosPassThru.GetMediaTime: il metodo GetMediaTime recupera i timestamp nell'esempio corrente."
ms.assetid: 36f3b6d3-b884-4168-94f3-f334a5056c7d
title: Metodo CPosPassThru.GetMediaTime (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 328a0ae09c80a687863cfedb994f5a80cebebf14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095259"
---
# <a name="cpospassthrugetmediatime-method"></a><span data-ttu-id="08e60-103">Metodo CPosPassThru.GetMediaTime</span><span class="sxs-lookup"><span data-stu-id="08e60-103">CPosPassThru.GetMediaTime method</span></span>

<span data-ttu-id="08e60-104">Il `GetMediaTime` metodo recupera i timestamp nell'esempio corrente.</span><span class="sxs-lookup"><span data-stu-id="08e60-104">The `GetMediaTime` method retrieves the time stamps on the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="08e60-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08e60-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="08e60-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="08e60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08e60-107">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="08e60-107">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="08e60-108">Puntatore a una variabile che riceve l'ora di inizio, in unità del formato di ora corrente.</span><span class="sxs-lookup"><span data-stu-id="08e60-108">Pointer to a variable that receives the start time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="08e60-109">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="08e60-109">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="08e60-110">Puntatore a una variabile che riceve l'ora di fine, in unità del formato di ora corrente.</span><span class="sxs-lookup"><span data-stu-id="08e60-110">Pointer to a variable that receives the end time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08e60-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="08e60-111">Return value</span></span>

<span data-ttu-id="08e60-112">Restituisce E \_ FAIL.</span><span class="sxs-lookup"><span data-stu-id="08e60-112">Returns E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="08e60-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="08e60-113">Remarks</span></span>

<span data-ttu-id="08e60-114">Eseguire l'override di questo metodo se il filtro memorizza nella cache i timestamp nei campioni ricevuti.</span><span class="sxs-lookup"><span data-stu-id="08e60-114">Override this method if your filter caches the time stamps on the samples it receives.</span></span>

## <a name="requirements"></a><span data-ttu-id="08e60-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08e60-115">Requirements</span></span>



| <span data-ttu-id="08e60-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="08e60-116">Requirement</span></span> | <span data-ttu-id="08e60-117">Valore</span><span class="sxs-lookup"><span data-stu-id="08e60-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08e60-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="08e60-118">Header</span></span><br/>  | <dl> <span data-ttu-id="08e60-119"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="08e60-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="08e60-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="08e60-120">Library</span></span><br/> | <dl> <span data-ttu-id="08e60-121"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="08e60-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08e60-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08e60-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08e60-123">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="08e60-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




