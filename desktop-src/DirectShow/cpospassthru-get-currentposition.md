---
description: 'Il \_ metodo Get CurrentPosition recupera la posizione corrente rispetto alla durata totale del flusso. Questo metodo implementa il metodo IMediaPosition:: Get \_ CurrentPosition.'
ms.assetid: 6e68af98-440d-4ecc-b1aa-d5e241de4999
title: Metodo CPosPassThru.get_CurrentPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c146eb1ee3d0a48da90973ab181a4bd02182331
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327441"
---
# <a name="cpospassthruget_currentposition-method"></a><span data-ttu-id="dcc6f-104">Metodo CPosPassThru. Get \_ currentPosition</span><span class="sxs-lookup"><span data-stu-id="dcc6f-104">CPosPassThru.get\_CurrentPosition method</span></span>

<span data-ttu-id="dcc6f-105">Il `get_CurrentPosition` metodo recupera la posizione corrente rispetto alla durata totale del flusso.</span><span class="sxs-lookup"><span data-stu-id="dcc6f-105">The `get_CurrentPosition` method retrieves the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="dcc6f-106">Questo metodo implementa il metodo [**IMediaPosition:: Get \_ currentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-get_currentposition) .</span><span class="sxs-lookup"><span data-stu-id="dcc6f-106">This method implements the [**IMediaPosition::get\_CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-get_currentposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcc6f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dcc6f-107">Syntax</span></span>


```C++
HRESULT get_CurrentPosition(
   REFTIME *pllTime
);
```



## <a name="parameters"></a><span data-ttu-id="dcc6f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dcc6f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcc6f-109">*pllTime*</span><span class="sxs-lookup"><span data-stu-id="dcc6f-109">*pllTime*</span></span> 
</dt> <dd>

<span data-ttu-id="dcc6f-110">Puntatore a una variabile che riceve la posizione corrente, in secondi.</span><span class="sxs-lookup"><span data-stu-id="dcc6f-110">Pointer to a variable that receives the current position, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcc6f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dcc6f-111">Return value</span></span>

<span data-ttu-id="dcc6f-112">Restituisce il valore **HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="dcc6f-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcc6f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dcc6f-113">Requirements</span></span>



| <span data-ttu-id="dcc6f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcc6f-114">Requirement</span></span> | <span data-ttu-id="dcc6f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="dcc6f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcc6f-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dcc6f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="dcc6f-117"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dcc6f-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dcc6f-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="dcc6f-118">Library</span></span><br/> | <dl> <span data-ttu-id="dcc6f-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="dcc6f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcc6f-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dcc6f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcc6f-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="dcc6f-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




