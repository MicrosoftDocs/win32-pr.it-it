---
description: Il metodo GetMediaTime recupera i timestamp nell'esempio corrente.
ms.assetid: 36f3b6d3-b884-4168-94f3-f334a5056c7d
title: Metodo CPosPassThru. GetMediaTime (Ctlutil. h)
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
ms.openlocfilehash: b2748d986f121a38041155dcd43f13a647916486
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325514"
---
# <a name="cpospassthrugetmediatime-method"></a><span data-ttu-id="a4a2f-103">CPosPassThru. GetMediaTime, metodo</span><span class="sxs-lookup"><span data-stu-id="a4a2f-103">CPosPassThru.GetMediaTime method</span></span>

<span data-ttu-id="a4a2f-104">Il `GetMediaTime` metodo recupera i timestamp nell'esempio corrente.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-104">The `GetMediaTime` method retrieves the time stamps on the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4a2f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a4a2f-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="a4a2f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a4a2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4a2f-107">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="a4a2f-107">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="a4a2f-108">Puntatore a una variabile che riceve l'ora di inizio, in unità del formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-108">Pointer to a variable that receives the start time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="a4a2f-109">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="a4a2f-109">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="a4a2f-110">Puntatore a una variabile che riceve l'ora di fine, in unità del formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-110">Pointer to a variable that receives the end time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4a2f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a4a2f-111">Return value</span></span>

<span data-ttu-id="a4a2f-112">Restituisce E ha \_ esito negativo.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-112">Returns E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4a2f-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a4a2f-113">Remarks</span></span>

<span data-ttu-id="a4a2f-114">Eseguire l'override di questo metodo se il filtro memorizza nella cache i timestamp sugli esempi ricevuti.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-114">Override this method if your filter caches the time stamps on the samples it receives.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4a2f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4a2f-115">Requirements</span></span>



| <span data-ttu-id="a4a2f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4a2f-116">Requirement</span></span> | <span data-ttu-id="a4a2f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="a4a2f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4a2f-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a4a2f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a4a2f-119"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a4a2f-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a4a2f-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="a4a2f-120">Library</span></span><br/> | <dl> <span data-ttu-id="a4a2f-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a4a2f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4a2f-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a4a2f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4a2f-123">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="a4a2f-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




