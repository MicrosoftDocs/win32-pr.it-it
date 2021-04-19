---
description: Il metodo EnableEffects Abilita o Disabilita tutti gli effetti nella sequenza temporale. Se gli effetti sono disabilitati, rimangono nella sequenza temporale ma non ne viene eseguito il rendering.
ms.assetid: 5344cd49-6515-4211-9637-ca58219b3b56
title: 'Metodo IAMTimeline:: EnableEffects (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableEffects
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e090f115083e2d1433e60d7a8707ded9b89ba433
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326799"
---
# <a name="iamtimelineenableeffects-method"></a><span data-ttu-id="4a863-104">Metodo IAMTimeline:: EnableEffects</span><span class="sxs-lookup"><span data-stu-id="4a863-104">IAMTimeline::EnableEffects method</span></span>

> [!Note]  
> <span data-ttu-id="4a863-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="4a863-105">\[Deprecated.</span></span> <span data-ttu-id="4a863-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4a863-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4a863-107">Il `EnableEffects` Metodo Abilita o Disabilita tutti gli effetti nella sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="4a863-107">The `EnableEffects` method enables or disables all effects in the timeline.</span></span> <span data-ttu-id="4a863-108">Se gli effetti sono disabilitati, rimangono nella sequenza temporale ma non ne viene eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="4a863-108">If effects are disabled, they remain in the timeline but are not rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a863-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a863-109">Syntax</span></span>


```C++
HRESULT EnableEffects(
   BOOL fEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="4a863-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a863-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a863-111">*fEnabled*</span><span class="sxs-lookup"><span data-stu-id="4a863-111">*fEnabled*</span></span> 
</dt> <dd>

<span data-ttu-id="4a863-112">Valore booleano che specifica se abilitare o disabilitare gli effetti.</span><span class="sxs-lookup"><span data-stu-id="4a863-112">Boolean value that specifies whether to enable or disable effects.</span></span> <span data-ttu-id="4a863-113">Se **true**, gli effetti sono abilitati.</span><span class="sxs-lookup"><span data-stu-id="4a863-113">If **TRUE**, effects are enabled.</span></span> <span data-ttu-id="4a863-114">Se **false**, gli effetti sono disabilitati.</span><span class="sxs-lookup"><span data-stu-id="4a863-114">If **FALSE**, effects are disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a863-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a863-115">Return value</span></span>

<span data-ttu-id="4a863-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4a863-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4a863-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4a863-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a863-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="4a863-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4a863-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="4a863-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4a863-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4a863-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4a863-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4a863-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4a863-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a863-122">Requirements</span></span>



| <span data-ttu-id="4a863-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a863-123">Requirement</span></span> | <span data-ttu-id="4a863-124">Valore</span><span class="sxs-lookup"><span data-stu-id="4a863-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a863-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4a863-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4a863-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a863-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4a863-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="4a863-127">Library</span></span><br/> | <dl> <span data-ttu-id="4a863-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a863-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a863-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a863-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a863-130">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="4a863-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="4a863-131">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="4a863-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




