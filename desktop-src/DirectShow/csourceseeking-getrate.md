---
description: 'Il metodo getrate recupera la velocità di riproduzione. Questo metodo implementa il metodo IMediaSeeking:: getrate.'
ms.assetid: e5c3ef27-6f57-4c74-b197-a3c4efb31239
title: Metodo CSourceSeeking. getrate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b14cad0b043193f7ee410455aaa399e3bcb26715
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329503"
---
# <a name="csourceseekinggetrate-method"></a><span data-ttu-id="2b1d3-104">CSourceSeeking. getrate, metodo</span><span class="sxs-lookup"><span data-stu-id="2b1d3-104">CSourceSeeking.GetRate method</span></span>

<span data-ttu-id="2b1d3-105">Il `GetRate` metodo recupera la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="2b1d3-105">The `GetRate` method retrieves the playback rate.</span></span> <span data-ttu-id="2b1d3-106">Questo metodo implementa il metodo [**IMediaSeeking:: getrate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) .</span><span class="sxs-lookup"><span data-stu-id="2b1d3-106">This method implements the [**IMediaSeeking::GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b1d3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2b1d3-107">Syntax</span></span>


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="2b1d3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2b1d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b1d3-109">*pdRate*</span><span class="sxs-lookup"><span data-stu-id="2b1d3-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="2b1d3-110">Puntatore a una variabile che riceve la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="2b1d3-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b1d3-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2b1d3-111">Return value</span></span>

<span data-ttu-id="2b1d3-112">Restituisce uno dei valori **HRESULT** elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="2b1d3-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="2b1d3-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2b1d3-113">Return code</span></span>                                                                               | <span data-ttu-id="2b1d3-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b1d3-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="2b1d3-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2b1d3-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="2b1d3-116">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="2b1d3-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="2b1d3-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="2b1d3-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="2b1d3-118">Valore del puntatore **null**</span><span class="sxs-lookup"><span data-stu-id="2b1d3-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2b1d3-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="2b1d3-119">Remarks</span></span>

<span data-ttu-id="2b1d3-120">La velocità di riproduzione è specificata dalla variabile membro [**CSourceSeeking:: m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) .</span><span class="sxs-lookup"><span data-stu-id="2b1d3-120">The playback rate is specified by the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b1d3-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b1d3-121">Requirements</span></span>



| <span data-ttu-id="2b1d3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b1d3-122">Requirement</span></span> | <span data-ttu-id="2b1d3-123">Valore</span><span class="sxs-lookup"><span data-stu-id="2b1d3-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b1d3-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2b1d3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2b1d3-125"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b1d3-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2b1d3-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="2b1d3-126">Library</span></span><br/> | <dl> <span data-ttu-id="2b1d3-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2b1d3-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b1d3-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b1d3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b1d3-129">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="2b1d3-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




