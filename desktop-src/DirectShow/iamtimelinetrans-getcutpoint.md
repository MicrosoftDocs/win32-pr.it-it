---
description: Il metodo GetCutPoint Recupera il punto di taglio.
ms.assetid: f54ef17e-3407-4164-911d-3dc7fad656ed
title: 'Metodo IAMTimelineTrans:: GetCutPoint (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e89cc2e7bc6d18842212a58bc5c00b6424947b66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333265"
---
# <a name="iamtimelinetransgetcutpoint-method"></a><span data-ttu-id="7a18d-103">Metodo IAMTimelineTrans:: GetCutPoint</span><span class="sxs-lookup"><span data-stu-id="7a18d-103">IAMTimelineTrans::GetCutPoint method</span></span>

> [!Note]  
> <span data-ttu-id="7a18d-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="7a18d-104">\[Deprecated.</span></span> <span data-ttu-id="7a18d-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7a18d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7a18d-106">Il `GetCutPoint` metodo recupera il punto di taglio.</span><span class="sxs-lookup"><span data-stu-id="7a18d-106">The `GetCutPoint` method retrieves the cut point.</span></span> <span data-ttu-id="7a18d-107">Se si esegue il rendering di una transizione come taglia, il punto di taglio è il momento in cui la transizione passa da un'origine a quella successiva.</span><span class="sxs-lookup"><span data-stu-id="7a18d-107">If you render a transition as a cut, the cut point is the time when the transition cuts from one source to the next.</span></span> <span data-ttu-id="7a18d-108">Per impostazione predefinita, questo valore è il centro della transizione.</span><span class="sxs-lookup"><span data-stu-id="7a18d-108">By default, this value is the middle of the transition.</span></span> <span data-ttu-id="7a18d-109">Ad esempio, in una transizione che si estende su un secondo, il punto di taglio predefinito è di 0,5 secondi nella transizione.</span><span class="sxs-lookup"><span data-stu-id="7a18d-109">For example, in a transition that spans one second, the default cut point is 0.5 seconds into the transition.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a18d-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a18d-110">Syntax</span></span>


```C++
HRESULT GetCutPoint(
   REFERENCE_TIME *pTLTime
);
```



## <a name="parameters"></a><span data-ttu-id="7a18d-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="7a18d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a18d-112">*pTLTime*</span><span class="sxs-lookup"><span data-stu-id="7a18d-112">*pTLTime*</span></span> 
</dt> <dd>

<span data-ttu-id="7a18d-113">Riceve il punto di taglio, relativo all'ora di inizio della transizione, in unità 100-nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="7a18d-113">Receives the cut point, relative to the start time of the transition, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a18d-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7a18d-114">Return value</span></span>

<span data-ttu-id="7a18d-115">Restituisce uno dei seguenti valori **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="7a18d-115">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="7a18d-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7a18d-116">Return code</span></span>                                                                               | <span data-ttu-id="7a18d-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a18d-117">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7a18d-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="7a18d-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="7a18d-119">Il punto di taglio non è stato impostato.</span><span class="sxs-lookup"><span data-stu-id="7a18d-119">The cut point was not set.</span></span> <span data-ttu-id="7a18d-120">Il valore restituito è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="7a18d-120">The value returned is the default value.</span></span><br/> |
| <dl> <span data-ttu-id="7a18d-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7a18d-121"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="7a18d-122">Il punto di taglio è stato impostato su un valore diverso da quello predefinito.</span><span class="sxs-lookup"><span data-stu-id="7a18d-122">The cut point was set to a value other than the default.</span></span><br/>            |
| <dl> <span data-ttu-id="7a18d-123"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="7a18d-123"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="7a18d-124">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="7a18d-124">**NULL** pointer argument.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="7a18d-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a18d-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7a18d-126">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="7a18d-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7a18d-127">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7a18d-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7a18d-128">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7a18d-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7a18d-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a18d-129">Requirements</span></span>



| <span data-ttu-id="7a18d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a18d-130">Requirement</span></span> | <span data-ttu-id="7a18d-131">Valore</span><span class="sxs-lookup"><span data-stu-id="7a18d-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a18d-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a18d-132">Header</span></span><br/>  | <dl> <span data-ttu-id="7a18d-133"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a18d-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7a18d-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="7a18d-134">Library</span></span><br/> | <dl> <span data-ttu-id="7a18d-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a18d-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a18d-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a18d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a18d-137">**Interfaccia IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="7a18d-137">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="7a18d-138">**IAMTimelineTrans::SetCutPoint**</span><span class="sxs-lookup"><span data-stu-id="7a18d-138">**IAMTimelineTrans::SetCutPoint**</span></span>](iamtimelinetrans-setcutpoint.md)
</dt> <dt>

[<span data-ttu-id="7a18d-139">**IAMTimelineTrans::GetCutsOnly**</span><span class="sxs-lookup"><span data-stu-id="7a18d-139">**IAMTimelineTrans::GetCutsOnly**</span></span>](iamtimelinetrans-getcutsonly.md)
</dt> <dt>

[<span data-ttu-id="7a18d-140">**IAMTimeline::TransitionsEnabled**</span><span class="sxs-lookup"><span data-stu-id="7a18d-140">**IAMTimeline::TransitionsEnabled**</span></span>](iamtimeline-transitionsenabled.md)
</dt> <dt>

[<span data-ttu-id="7a18d-141">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="7a18d-141">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




