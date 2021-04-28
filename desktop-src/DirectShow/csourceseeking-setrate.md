---
description: 'Metodo CSourceSeeking.SetRate: il metodo SetRate imposta la velocità di riproduzione. Questo metodo implementa il metodo IMediaSeeking::SetRate.'
ms.assetid: 954e2381-207a-47d9-a0a5-87dc325f52b4
title: Metodo CSourceSeeking.SetRate (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c37d9c94da4a59a2be9b7258881c5bb22b4aa4c5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098739"
---
# <a name="csourceseekingsetrate-method"></a><span data-ttu-id="29145-104">Metodo CSourceSeeking.SetRate</span><span class="sxs-lookup"><span data-stu-id="29145-104">CSourceSeeking.SetRate method</span></span>

<span data-ttu-id="29145-105">Il `SetRate` metodo imposta la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="29145-105">The `SetRate` method sets the playback rate.</span></span> <span data-ttu-id="29145-106">Questo metodo implementa il [**metodo IMediaSeeking::SetRate.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)</span><span class="sxs-lookup"><span data-stu-id="29145-106">This method implements the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="29145-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29145-107">Syntax</span></span>


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="29145-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="29145-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29145-109">*dRate*</span><span class="sxs-lookup"><span data-stu-id="29145-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="29145-110">Velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="29145-110">Playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29145-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="29145-111">Return value</span></span>

<span data-ttu-id="29145-112">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="29145-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="29145-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="29145-113">Remarks</span></span>

<span data-ttu-id="29145-114">Questo metodo aggiorna il valore della variabile membro [**CSourceSeeking::m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) e quindi chiama il metodo virtuale puro [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md).</span><span class="sxs-lookup"><span data-stu-id="29145-114">This method updates the value of the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable, and then calls the pure virtual method [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="29145-115">Il metodo non convalida il *parametro dRate.*</span><span class="sxs-lookup"><span data-stu-id="29145-115">The method does not validate the *dRate* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="29145-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29145-116">Requirements</span></span>



| <span data-ttu-id="29145-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="29145-117">Requirement</span></span> | <span data-ttu-id="29145-118">Valore</span><span class="sxs-lookup"><span data-stu-id="29145-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29145-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="29145-119">Header</span></span><br/>  | <dl> <span data-ttu-id="29145-120"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="29145-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="29145-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="29145-121">Library</span></span><br/> | <dl> <span data-ttu-id="29145-122"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="29145-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29145-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29145-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29145-124">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="29145-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




