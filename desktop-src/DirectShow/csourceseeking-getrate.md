---
description: 'Metodo CSourceSeeking.GetRate: il metodo GetRate recupera la velocità di riproduzione. Questo metodo implementa il metodo IMediaSeeking::GetRate.'
ms.assetid: e5c3ef27-6f57-4c74-b197-a3c4efb31239
title: Metodo CSourceSeeking.GetRate (Ctlutil.h)
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
ms.openlocfilehash: fef379ef06cd0982f1eb5742ac2624d706ed73a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085229"
---
# <a name="csourceseekinggetrate-method"></a><span data-ttu-id="b78b0-104">Metodo CSourceSeeking.GetRate</span><span class="sxs-lookup"><span data-stu-id="b78b0-104">CSourceSeeking.GetRate method</span></span>

<span data-ttu-id="b78b0-105">Il `GetRate` metodo recupera la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="b78b0-105">The `GetRate` method retrieves the playback rate.</span></span> <span data-ttu-id="b78b0-106">Questo metodo implementa il [**metodo IMediaSeeking::GetRate.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate)</span><span class="sxs-lookup"><span data-stu-id="b78b0-106">This method implements the [**IMediaSeeking::GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b78b0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b78b0-107">Syntax</span></span>


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="b78b0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b78b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b78b0-109">*pdRate*</span><span class="sxs-lookup"><span data-stu-id="b78b0-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="b78b0-110">Puntatore a una variabile che riceve la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="b78b0-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b78b0-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b78b0-111">Return value</span></span>

<span data-ttu-id="b78b0-112">Restituisce uno dei **valori HRESULT** elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="b78b0-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="b78b0-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b78b0-113">Return code</span></span>                                                                               | <span data-ttu-id="b78b0-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b78b0-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="b78b0-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b78b0-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="b78b0-116">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="b78b0-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="b78b0-117"><dt>**PUNTATORE \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="b78b0-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="b78b0-118">**Valore del** puntatore NULL</span><span class="sxs-lookup"><span data-stu-id="b78b0-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b78b0-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="b78b0-119">Remarks</span></span>

<span data-ttu-id="b78b0-120">La velocità di riproduzione viene specificata dalla [**variabile membro CSourceSeeking::m \_ dRateSeeking.**](csourceseeking-m-drateseeking.md)</span><span class="sxs-lookup"><span data-stu-id="b78b0-120">The playback rate is specified by the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="b78b0-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b78b0-121">Requirements</span></span>



| <span data-ttu-id="b78b0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b78b0-122">Requirement</span></span> | <span data-ttu-id="b78b0-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b78b0-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b78b0-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b78b0-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b78b0-125"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="b78b0-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b78b0-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="b78b0-126">Library</span></span><br/> | <dl> <span data-ttu-id="b78b0-127"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b78b0-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b78b0-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b78b0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b78b0-129">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="b78b0-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




