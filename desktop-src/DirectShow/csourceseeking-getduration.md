---
description: 'Metodo CSourceSeeking.GetDuration: il metodo GetDuration recupera la durata del flusso. Questo metodo implementa il metodo IMediaSeeking::GetDuration.'
ms.assetid: 074eb2d0-a7a3-4bc1-82e8-2f42c6d43dac
title: Metodo CSourceSeeking.GetDuration (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d5b961ad62d65c1f728af71e82de1373ea20b1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098769"
---
# <a name="csourceseekinggetduration-method"></a><span data-ttu-id="44fec-104">Metodo CSourceSeeking.GetDuration</span><span class="sxs-lookup"><span data-stu-id="44fec-104">CSourceSeeking.GetDuration method</span></span>

<span data-ttu-id="44fec-105">Il `GetDuration` metodo recupera la durata del flusso.</span><span class="sxs-lookup"><span data-stu-id="44fec-105">The `GetDuration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="44fec-106">Questo metodo implementa il [**metodo IMediaSeeking::GetDuration.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration)</span><span class="sxs-lookup"><span data-stu-id="44fec-106">This method implements the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="44fec-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="44fec-107">Syntax</span></span>


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="44fec-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="44fec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44fec-109">*pDuration*</span><span class="sxs-lookup"><span data-stu-id="44fec-109">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="44fec-110">Puntatore a una variabile che riceve la durata, in unità del formato di ora corrente.</span><span class="sxs-lookup"><span data-stu-id="44fec-110">Pointer to a variable that receives the duration, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44fec-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="44fec-111">Return value</span></span>

<span data-ttu-id="44fec-112">Restituisce uno dei **valori HRESULT** elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="44fec-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="44fec-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="44fec-113">Return code</span></span>                                                                               | <span data-ttu-id="44fec-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44fec-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="44fec-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="44fec-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="44fec-116">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="44fec-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="44fec-117"><dt>**PUNTATORE \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="44fec-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="44fec-118">**Valore del** puntatore NULL</span><span class="sxs-lookup"><span data-stu-id="44fec-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="44fec-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="44fec-119">Remarks</span></span>

<span data-ttu-id="44fec-120">La durata viene specificata dalla [**variabile membro CSourceSeeking::m \_ rtDuration.**](csourceseeking-m-rtduration.md)</span><span class="sxs-lookup"><span data-stu-id="44fec-120">The duration is specified by the [**CSourceSeeking::m\_rtDuration**](csourceseeking-m-rtduration.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="44fec-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44fec-121">Requirements</span></span>



| <span data-ttu-id="44fec-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="44fec-122">Requirement</span></span> | <span data-ttu-id="44fec-123">Valore</span><span class="sxs-lookup"><span data-stu-id="44fec-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44fec-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="44fec-124">Header</span></span><br/>  | <dl> <span data-ttu-id="44fec-125"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="44fec-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="44fec-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="44fec-126">Library</span></span><br/> | <dl> <span data-ttu-id="44fec-127"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="44fec-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44fec-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="44fec-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44fec-129">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="44fec-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




