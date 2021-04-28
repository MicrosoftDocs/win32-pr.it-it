---
description: 'Metodo CPosPassThru.SetRate: il metodo SetRate imposta la velocità di riproduzione. Questo metodo implementa il metodo IMediaSeeking::SetRate.'
ms.assetid: 1b38eb5d-38fd-408b-9f20-4f8d18158f92
title: Metodo CPosPassThru.SetRate (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bccc0d7044ccf17ac1c97e4fc5a185bdf6c7f0be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095219"
---
# <a name="cpospassthrusetrate-method"></a><span data-ttu-id="ab626-104">Metodo CPosPassThru.SetRate</span><span class="sxs-lookup"><span data-stu-id="ab626-104">CPosPassThru.SetRate method</span></span>

<span data-ttu-id="ab626-105">Il `SetRate` metodo imposta la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="ab626-105">The `SetRate` method sets the playback rate.</span></span> <span data-ttu-id="ab626-106">Questo metodo implementa il [**metodo IMediaSeeking::SetRate.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)</span><span class="sxs-lookup"><span data-stu-id="ab626-106">This method implements the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab626-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab626-107">Syntax</span></span>


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="ab626-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab626-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab626-109">*dRate*</span><span class="sxs-lookup"><span data-stu-id="ab626-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="ab626-110">Velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="ab626-110">Playback rate.</span></span> <span data-ttu-id="ab626-111">Non deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="ab626-111">Must not be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab626-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab626-112">Return value</span></span>

<span data-ttu-id="ab626-113">Restituisce E \_ INVALIDARG se *dRate* è zero.</span><span class="sxs-lookup"><span data-stu-id="ab626-113">Returns E\_INVALIDARG if *dRate* is zero.</span></span> <span data-ttu-id="ab626-114">In caso contrario, restituisce il **valore HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="ab626-114">Otherwise, returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab626-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab626-115">Requirements</span></span>



| <span data-ttu-id="ab626-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab626-116">Requirement</span></span> | <span data-ttu-id="ab626-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ab626-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab626-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ab626-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ab626-119"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab626-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ab626-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="ab626-120">Library</span></span><br/> | <dl> <span data-ttu-id="ab626-121"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ab626-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab626-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab626-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab626-123">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="ab626-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




