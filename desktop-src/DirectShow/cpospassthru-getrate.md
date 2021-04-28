---
description: 'Metodo CPosPassThru.GetRate: il metodo GetRate recupera la velocità di riproduzione. Questo metodo implementa il metodo IMediaSeeking::GetRate.'
ms.assetid: 19de3ea3-280e-4320-9cce-2c29801bd84b
title: Metodo CPosPassThru.GetRate (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 997323ca2089a0b381b85c3730cb364d0883b1bf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085559"
---
# <a name="cpospassthrugetrate-method"></a><span data-ttu-id="f1841-104">Metodo CPosPassThru.GetRate</span><span class="sxs-lookup"><span data-stu-id="f1841-104">CPosPassThru.GetRate method</span></span>

<span data-ttu-id="f1841-105">Il `GetRate` metodo recupera la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="f1841-105">The `GetRate` method retrieves the playback rate.</span></span> <span data-ttu-id="f1841-106">Questo metodo implementa il [**metodo IMediaSeeking::GetRate.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate)</span><span class="sxs-lookup"><span data-stu-id="f1841-106">This method implements the [**IMediaSeeking::GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1841-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1841-107">Syntax</span></span>


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="f1841-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f1841-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1841-109">*pdRate*</span><span class="sxs-lookup"><span data-stu-id="f1841-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="f1841-110">Puntatore a una variabile che riceve la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="f1841-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1841-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f1841-111">Return value</span></span>

<span data-ttu-id="f1841-112">Restituisce il **valore HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="f1841-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1841-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1841-113">Requirements</span></span>



| <span data-ttu-id="f1841-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1841-114">Requirement</span></span> | <span data-ttu-id="f1841-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f1841-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1841-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f1841-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f1841-117"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1841-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f1841-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="f1841-118">Library</span></span><br/> | <dl> <span data-ttu-id="f1841-119"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f1841-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1841-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1841-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1841-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="f1841-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




