---
description: "Il metodo GetNextTrans2 recupera la prima transizione visualizzata all'ora specificata o successiva. Questo metodo è equivalente a IAMTimelineTransable:: GetNextTrans, ma accetta un valore REFTIME."
ms.assetid: e6910e94-f289-4a5d-9976-1e8f7373c882
title: 'Metodo IAMTimelineTransable:: GetNextTrans2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2c5f79ff20507247fbcac3badceaf2c3e28f0303
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332972"
---
# <a name="iamtimelinetransablegetnexttrans2-method"></a><span data-ttu-id="82e0c-104">Metodo IAMTimelineTransable:: GetNextTrans2</span><span class="sxs-lookup"><span data-stu-id="82e0c-104">IAMTimelineTransable::GetNextTrans2 method</span></span>

> [!Note]  
> <span data-ttu-id="82e0c-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="82e0c-105">\[Deprecated.</span></span> <span data-ttu-id="82e0c-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="82e0c-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="82e0c-107">Il `GetNextTrans2` metodo recupera la prima transizione visualizzata all'ora specificata o successiva.</span><span class="sxs-lookup"><span data-stu-id="82e0c-107">The `GetNextTrans2` method retrieves the first transition that appears at the specified time or later.</span></span> <span data-ttu-id="82e0c-108">Questo metodo è equivalente a [**IAMTimelineTransable:: GetNextTrans**](iamtimelinetransable-getnexttrans.md), ma accetta un valore [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="82e0c-108">This method is equivalent to [**IAMTimelineTransable::GetNextTrans**](iamtimelinetransable-getnexttrans.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="82e0c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82e0c-109">Syntax</span></span>


```C++
HRESULT GetNextTrans2(
  [out] IAMTimelineObj **ppTrans,
        REFTIME        *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="82e0c-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="82e0c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82e0c-111">*ppTrans* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="82e0c-111">*ppTrans* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82e0c-112">Riceve un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) dell'oggetto di transizione.</span><span class="sxs-lookup"><span data-stu-id="82e0c-112">Receives a pointer to the transition object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="82e0c-113">*pInOut*</span><span class="sxs-lookup"><span data-stu-id="82e0c-113">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="82e0c-114">Puntatore a una variabile che specifica il tempo in secondi.</span><span class="sxs-lookup"><span data-stu-id="82e0c-114">Pointer to a variable that specifies the time in seconds.</span></span> <span data-ttu-id="82e0c-115">In input, questo valore specifica l'ora da cui trovare la transizione.</span><span class="sxs-lookup"><span data-stu-id="82e0c-115">On input, this value specifies the time from which to find the transition.</span></span> <span data-ttu-id="82e0c-116">Nell'output, se viene recuperata una transizione, questo valore viene impostato sull'ora di arresto della transizione.</span><span class="sxs-lookup"><span data-stu-id="82e0c-116">On output, if a transition is retrieved, this value is set to the stop time of the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82e0c-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="82e0c-117">Return value</span></span>

<span data-ttu-id="82e0c-118">Restituisce \_ OK se il metodo recupera una transizione o S \_ false se non trova una transizione.</span><span class="sxs-lookup"><span data-stu-id="82e0c-118">Returns S\_OK if the method retrieves a transition, or S\_FALSE if it does not find a transition.</span></span> <span data-ttu-id="82e0c-119">In caso contrario, restituisce un valore **HRESULT** che indica la cause dell'errore.</span><span class="sxs-lookup"><span data-stu-id="82e0c-119">Otherwise, returns an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="82e0c-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="82e0c-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="82e0c-121">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="82e0c-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="82e0c-122">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="82e0c-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="82e0c-123">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="82e0c-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="82e0c-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82e0c-124">Requirements</span></span>



| <span data-ttu-id="82e0c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="82e0c-125">Requirement</span></span> | <span data-ttu-id="82e0c-126">Valore</span><span class="sxs-lookup"><span data-stu-id="82e0c-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82e0c-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="82e0c-127">Header</span></span><br/>  | <dl> <span data-ttu-id="82e0c-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="82e0c-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="82e0c-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="82e0c-129">Library</span></span><br/> | <dl> <span data-ttu-id="82e0c-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82e0c-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82e0c-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82e0c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82e0c-132">**Interfaccia IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="82e0c-132">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="82e0c-133">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="82e0c-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




