---
description: 'Il metodo GetPositions recupera la posizione corrente e la posizione di arresto rispetto alla durata totale del flusso. Questo metodo implementa il metodo IMediaSeeking:: GetPositions.'
ms.assetid: 51e45bc3-ae30-4b05-b9d9-684c1b028f51
title: Metodo CPosPassThru. GetPositions (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0852199e8e143ce5b0348c3b79afd495a5a47627
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329760"
---
# <a name="cpospassthrugetpositions-method"></a><span data-ttu-id="d8c17-104">Metodo CPosPassThru. GetPositions</span><span class="sxs-lookup"><span data-stu-id="d8c17-104">CPosPassThru.GetPositions method</span></span>

<span data-ttu-id="d8c17-105">Il `GetPositions` metodo recupera la posizione corrente e la posizione di arresto rispetto alla durata totale del flusso.</span><span class="sxs-lookup"><span data-stu-id="d8c17-105">The `GetPositions` method retrieves the current position and the stop position, relative to the total duration of the stream.</span></span> <span data-ttu-id="d8c17-106">Questo metodo implementa il metodo [**IMediaSeeking:: GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) .</span><span class="sxs-lookup"><span data-stu-id="d8c17-106">This method implements the [**IMediaSeeking::GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8c17-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d8c17-107">Syntax</span></span>


```C++
HRESULT GetPositions(
   LONGLONG *pCurrent,
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="d8c17-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d8c17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8c17-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="d8c17-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="d8c17-110">Puntatore a una variabile che riceve la posizione corrente, in unità del formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="d8c17-110">Pointer to a variable that receives the current position, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="d8c17-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="d8c17-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="d8c17-112">Puntatore a una variabile che riceve la posizione di arresto, in unità del formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="d8c17-112">Pointer to a variable that receives the stop position, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8c17-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d8c17-113">Return value</span></span>

<span data-ttu-id="d8c17-114">Restituisce il valore **HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="d8c17-114">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8c17-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8c17-115">Requirements</span></span>



| <span data-ttu-id="d8c17-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8c17-116">Requirement</span></span> | <span data-ttu-id="d8c17-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d8c17-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8c17-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d8c17-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d8c17-119"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8c17-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d8c17-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="d8c17-120">Library</span></span><br/> | <dl> <span data-ttu-id="d8c17-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d8c17-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8c17-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8c17-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8c17-123">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="d8c17-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




