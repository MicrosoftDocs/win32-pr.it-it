---
description: "Metodo CBaseMediaFilter.StreamTime: il metodo StreamTime recupera l'ora corrente del flusso."
ms.assetid: 2e1ff6f1-9815-4ee6-97e8-a5ab5f472b27
title: Metodo CBaseMediaFilter.StreamTime (Amfilter.h)
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
ms.openlocfilehash: a90bb7d97825c14f11c75dd42d696fa302f8e3d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096249"
---
# <a name="cbasemediafilterstreamtime-method"></a><span data-ttu-id="9d5fb-103">Metodo CBaseMediaFilter.StreamTime</span><span class="sxs-lookup"><span data-stu-id="9d5fb-103">CBaseMediaFilter.StreamTime method</span></span>

<span data-ttu-id="9d5fb-104">Il `StreamTime` metodo recupera l'ora corrente del flusso.</span><span class="sxs-lookup"><span data-stu-id="9d5fb-104">The `StreamTime` method retrieves the current stream time.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d5fb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d5fb-105">Syntax</span></span>


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a><span data-ttu-id="9d5fb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9d5fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d5fb-107">*rtStream* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="9d5fb-107">*rtStream* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="9d5fb-108">Riferimento a un [**oggetto CRefTime**](creftime.md) che riceve l'ora corrente del flusso.</span><span class="sxs-lookup"><span data-stu-id="9d5fb-108">Reference to a [**CRefTime**](creftime.md) object that receives the current stream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d5fb-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9d5fb-109">Return value</span></span>

<span data-ttu-id="9d5fb-110">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="9d5fb-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="9d5fb-111">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="9d5fb-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="9d5fb-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9d5fb-112">Return code</span></span>                                                                                      | <span data-ttu-id="9d5fb-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d5fb-113">Description</span></span>                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="9d5fb-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9d5fb-114"><dt>**S\_OK**</dt></span></span> </dl>             | <span data-ttu-id="9d5fb-115">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="9d5fb-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="9d5fb-116"><dt>**VFW \_ E \_ NO \_ CLOCK**</dt></span><span class="sxs-lookup"><span data-stu-id="9d5fb-116"><dt>**VFW\_E\_NO\_CLOCK**</dt></span></span> </dl> | <span data-ttu-id="9d5fb-117">Non è disponibile alcun orologio di riferimento.</span><span class="sxs-lookup"><span data-stu-id="9d5fb-117">No reference clock is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9d5fb-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="9d5fb-118">Remarks</span></span>

<span data-ttu-id="9d5fb-119">L'ora di flusso è definita come ora di riferimento corrente (come specificato dall'orologio di riferimento) meno l'ora di inizio (specificata da [**CBaseMediaFilter::m \_ tStart**](cbasemediafilter-m-tstart.md)).</span><span class="sxs-lookup"><span data-stu-id="9d5fb-119">Stream time is defined as the current reference time (as given by the reference clock) minus the start time (specified by [**CBaseMediaFilter::m\_tStart**](cbasemediafilter-m-tstart.md)).</span></span> <span data-ttu-id="9d5fb-120">Il timestamp di un campione multimediale specifica l'ora del flusso in cui deve essere eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="9d5fb-120">A media sample's time stamp specifies the stream time when it should be rendered.</span></span> <span data-ttu-id="9d5fb-121">Se non è ancora stato eseguito il rendering di un esempio con timestamp inferiore all'ora corrente del flusso, è in ritardo.</span><span class="sxs-lookup"><span data-stu-id="9d5fb-121">If a sample with a time stamp less than the current stream time has not yet been rendered, it is late.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d5fb-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d5fb-122">Requirements</span></span>



| <span data-ttu-id="9d5fb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d5fb-123">Requirement</span></span> | <span data-ttu-id="9d5fb-124">Valore</span><span class="sxs-lookup"><span data-stu-id="9d5fb-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d5fb-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9d5fb-125">Header</span></span><br/>  | <dl> <span data-ttu-id="9d5fb-126"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d5fb-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9d5fb-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="9d5fb-127">Library</span></span><br/> | <dl> <span data-ttu-id="9d5fb-128"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9d5fb-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d5fb-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9d5fb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d5fb-130">**Classe CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="9d5fb-130">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




