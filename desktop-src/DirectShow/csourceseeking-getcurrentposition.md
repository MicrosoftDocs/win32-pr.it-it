---
description: Il metodo GetCurrentPosition recupera la posizione corrente rispetto alla durata totale del flusso. Non implementato.
ms.assetid: 386f41e4-a673-4c67-a28f-e155810fbb5a
title: Metodo CSourceSeeking. GetCurrentPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52f99323e5ce3a62f1964cad2586a18ad473cdc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329510"
---
# <a name="csourceseekinggetcurrentposition-method"></a><span data-ttu-id="1864f-104">CSourceSeeking. GetCurrentPosition, metodo</span><span class="sxs-lookup"><span data-stu-id="1864f-104">CSourceSeeking.GetCurrentPosition method</span></span>

<span data-ttu-id="1864f-105">Il `GetCurrentPosition` metodo recupera la posizione corrente rispetto alla durata totale del flusso.</span><span class="sxs-lookup"><span data-stu-id="1864f-105">The `GetCurrentPosition` method retrieves the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="1864f-106">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="1864f-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="1864f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1864f-107">Syntax</span></span>


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a><span data-ttu-id="1864f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1864f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1864f-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="1864f-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="1864f-110">Puntatore a una variabile che riceve la posizione corrente, in unità del formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="1864f-110">Pointer to a variable that receives the current position, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1864f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1864f-111">Return value</span></span>

<span data-ttu-id="1864f-112">Restituisce E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="1864f-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="1864f-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="1864f-113">Remarks</span></span>

<span data-ttu-id="1864f-114">I filtri di origine in genere non supportano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="1864f-114">Source filters typically do not support this method.</span></span> <span data-ttu-id="1864f-115">Al contrario, i filtri renderer segnalano la posizione corrente tramite la classe [**CRendererPosPassThru**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="1864f-115">Instead, renderer filters report the current position through the [**CRendererPosPassThru**](crendererpospassthru.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="1864f-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1864f-116">Requirements</span></span>



| <span data-ttu-id="1864f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1864f-117">Requirement</span></span> | <span data-ttu-id="1864f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="1864f-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1864f-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1864f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="1864f-120"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1864f-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1864f-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="1864f-121">Library</span></span><br/> | <dl> <span data-ttu-id="1864f-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1864f-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1864f-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1864f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1864f-124">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="1864f-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




