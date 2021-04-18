---
description: Il metodo SetCutsOnly specifica se viene eseguito il rendering della transizione come taglia. In tal caso, la transizione viene eseguita immediatamente in corrispondenza del punto di taglio. Se il rendering di una transizione richiede molto tempo, è possibile visualizzarne l'anteprima come un'anteprima di riduzione per la velocità.
ms.assetid: 9ccff624-e37b-422e-9cb2-c472e6c8b2bb
title: 'Metodo IAMTimelineTrans:: SetCutsOnly (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutsOnly
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b2944d652bffac5bf3bfa72a1e2372f734645bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333794"
---
# <a name="iamtimelinetranssetcutsonly-method"></a><span data-ttu-id="db7f3-105">Metodo IAMTimelineTrans:: SetCutsOnly</span><span class="sxs-lookup"><span data-stu-id="db7f3-105">IAMTimelineTrans::SetCutsOnly method</span></span>

> [!Note]  
> <span data-ttu-id="db7f3-106">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="db7f3-106">\[Deprecated.</span></span> <span data-ttu-id="db7f3-107">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="db7f3-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="db7f3-108">Il `SetCutsOnly` metodo specifica se viene eseguito il rendering della transizione come taglia.</span><span class="sxs-lookup"><span data-stu-id="db7f3-108">The `SetCutsOnly` method specifies whether the transition is rendered as a cut.</span></span> <span data-ttu-id="db7f3-109">In tal caso, la transizione viene eseguita immediatamente in corrispondenza del punto di taglio.</span><span class="sxs-lookup"><span data-stu-id="db7f3-109">If so, the transition occurs instantly at the cut point.</span></span> <span data-ttu-id="db7f3-110">Se il rendering di una transizione richiede molto tempo, è possibile visualizzarne l'anteprima come un'anteprima di riduzione per la velocità.</span><span class="sxs-lookup"><span data-stu-id="db7f3-110">If a transition takes a long time to render, you might want to preview it as a cut to speed preview.</span></span>

## <a name="syntax"></a><span data-ttu-id="db7f3-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db7f3-111">Syntax</span></span>


```C++
HRESULT SetCutsOnly(
   BOOL Val
);
```



## <a name="parameters"></a><span data-ttu-id="db7f3-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="db7f3-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db7f3-113">*Val*</span><span class="sxs-lookup"><span data-stu-id="db7f3-113">*Val*</span></span> 
</dt> <dd>

<span data-ttu-id="db7f3-114">Specifica se eseguire il rendering della transizione come taglia.</span><span class="sxs-lookup"><span data-stu-id="db7f3-114">Specifies whether to render the transition as a cut.</span></span> <span data-ttu-id="db7f3-115">Se **true**, viene eseguito il rendering della transizione come taglia istantanea.</span><span class="sxs-lookup"><span data-stu-id="db7f3-115">If **TRUE**, the transition is rendered as an instantaneous cut.</span></span> <span data-ttu-id="db7f3-116">Se **false**, viene eseguito il rendering della transizione sulla durata normale.</span><span class="sxs-lookup"><span data-stu-id="db7f3-116">If **FALSE**, the transition renders over its normal duration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db7f3-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="db7f3-117">Return value</span></span>

<span data-ttu-id="db7f3-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="db7f3-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="db7f3-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="db7f3-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="db7f3-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="db7f3-120">Remarks</span></span>

<span data-ttu-id="db7f3-121">Il rendering di una transizione come taglia non è compatibile con lo scambio degli input.</span><span class="sxs-lookup"><span data-stu-id="db7f3-121">Rendering a transition as a cut is not compatible with swapping the inputs.</span></span> <span data-ttu-id="db7f3-122">Vedere [**IAMTimelineTrans:: SetSwapInputs**](iamtimelinetrans-setswapinputs.md). Se si chiama `SetCutsOnly` con un valore **true**, viene temporaneamente sostituita l'impostazione **SetSwapInputs** .</span><span class="sxs-lookup"><span data-stu-id="db7f3-122">(See [**IAMTimelineTrans::SetSwapInputs**](iamtimelinetrans-setswapinputs.md).) If you call `SetCutsOnly` with a value of **TRUE**, it temporarily overrides the **SetSwapInputs** setting.</span></span> <span data-ttu-id="db7f3-123">L'impostazione solo per i tagli è pensata per l'anteprima, quindi questa limitazione non influisce sull'output dei file, ma è sufficiente ricordare di chiamare `SetCutsOnly` con il valore **false** prima di scrivere il file.</span><span class="sxs-lookup"><span data-stu-id="db7f3-123">The cuts-only setting is intended for preview, however, so this limitation does not affect file output—just remember to call `SetCutsOnly` with the value **FALSE** before writing the file.</span></span>

> [!Note]  
> <span data-ttu-id="db7f3-124">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="db7f3-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="db7f3-125">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="db7f3-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="db7f3-126">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="db7f3-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="db7f3-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db7f3-127">Requirements</span></span>



| <span data-ttu-id="db7f3-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="db7f3-128">Requirement</span></span> | <span data-ttu-id="db7f3-129">Valore</span><span class="sxs-lookup"><span data-stu-id="db7f3-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db7f3-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="db7f3-130">Header</span></span><br/>  | <dl> <span data-ttu-id="db7f3-131"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="db7f3-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="db7f3-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="db7f3-132">Library</span></span><br/> | <dl> <span data-ttu-id="db7f3-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db7f3-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db7f3-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db7f3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db7f3-135">**Interfaccia IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="db7f3-135">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="db7f3-136">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="db7f3-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




