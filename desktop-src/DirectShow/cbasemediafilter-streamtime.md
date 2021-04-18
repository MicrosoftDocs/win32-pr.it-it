---
description: Il metodo StreamTime recupera l'ora del flusso corrente.
ms.assetid: 2e1ff6f1-9815-4ee6-97e8-a5ab5f472b27
title: Metodo CBaseMediaFilter. StreamTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27ccc9c721c97742c09d043af4cca5d287747597
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324796"
---
# <a name="cbasemediafilterstreamtime-method"></a><span data-ttu-id="598f1-103">CBaseMediaFilter. StreamTime, metodo</span><span class="sxs-lookup"><span data-stu-id="598f1-103">CBaseMediaFilter.StreamTime method</span></span>

<span data-ttu-id="598f1-104">Il `StreamTime` metodo recupera l'ora del flusso corrente.</span><span class="sxs-lookup"><span data-stu-id="598f1-104">The `StreamTime` method retrieves the current stream time.</span></span>

## <a name="syntax"></a><span data-ttu-id="598f1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="598f1-105">Syntax</span></span>


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a><span data-ttu-id="598f1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="598f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="598f1-107">*rtStream* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="598f1-107">*rtStream* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="598f1-108">Riferimento a un oggetto [**CRefTime**](creftime.md) che riceve l'ora del flusso corrente.</span><span class="sxs-lookup"><span data-stu-id="598f1-108">Reference to a [**CRefTime**](creftime.md) object that receives the current stream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="598f1-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="598f1-109">Return value</span></span>

<span data-ttu-id="598f1-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="598f1-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="598f1-111">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="598f1-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="598f1-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="598f1-112">Return code</span></span>                                                                                      | <span data-ttu-id="598f1-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="598f1-113">Description</span></span>                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="598f1-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="598f1-114"><dt>**S\_OK**</dt></span></span> </dl>             | <span data-ttu-id="598f1-115">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="598f1-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="598f1-116"><dt>**VFW \_ E \_ nessun \_ Clock**</dt></span><span class="sxs-lookup"><span data-stu-id="598f1-116"><dt>**VFW\_E\_NO\_CLOCK**</dt></span></span> </dl> | <span data-ttu-id="598f1-117">Nessun clock di riferimento disponibile.</span><span class="sxs-lookup"><span data-stu-id="598f1-117">No reference clock is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="598f1-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="598f1-118">Remarks</span></span>

<span data-ttu-id="598f1-119">Il tempo di flusso viene definito come ora di riferimento corrente (come indicato dall'orologio di riferimento) meno l'ora di inizio (specificata da [**CBaseMediaFilter:: m \_ tStart**](cbasemediafilter-m-tstart.md)).</span><span class="sxs-lookup"><span data-stu-id="598f1-119">Stream time is defined as the current reference time (as given by the reference clock) minus the start time (specified by [**CBaseMediaFilter::m\_tStart**](cbasemediafilter-m-tstart.md)).</span></span> <span data-ttu-id="598f1-120">Il timestamp di un campione multimediale specifica l'ora del flusso in cui deve essere eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="598f1-120">A media sample's time stamp specifies the stream time when it should be rendered.</span></span> <span data-ttu-id="598f1-121">Se non è ancora stato eseguito il rendering di un campione con un timestamp inferiore al tempo di flusso corrente, è in ritardo.</span><span class="sxs-lookup"><span data-stu-id="598f1-121">If a sample with a time stamp less than the current stream time has not yet been rendered, it is late.</span></span>

## <a name="requirements"></a><span data-ttu-id="598f1-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="598f1-122">Requirements</span></span>



| <span data-ttu-id="598f1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="598f1-123">Requirement</span></span> | <span data-ttu-id="598f1-124">Valore</span><span class="sxs-lookup"><span data-stu-id="598f1-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="598f1-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="598f1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="598f1-126"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="598f1-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="598f1-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="598f1-127">Library</span></span><br/> | <dl> <span data-ttu-id="598f1-128"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="598f1-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="598f1-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="598f1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="598f1-130">**Classe CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="598f1-130">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




