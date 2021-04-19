---
description: Il metodo EffectsEnabled determina se gli effetti sono abilitati. Se gli effetti sono disabilitati, rimangono nella sequenza temporale ma non ne viene eseguito il rendering.
ms.assetid: fd8bb2aa-9c10-4a85-9e9d-1b342fbce03b
title: 'Metodo IAMTimeline:: EffectsEnabled (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EffectsEnabled
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d988e8a4c10dc6dba52269c6729b8d7fea1f090e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326801"
---
# <a name="iamtimelineeffectsenabled-method"></a><span data-ttu-id="926b5-104">Metodo IAMTimeline:: EffectsEnabled</span><span class="sxs-lookup"><span data-stu-id="926b5-104">IAMTimeline::EffectsEnabled method</span></span>

> [!Note]  
> <span data-ttu-id="926b5-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="926b5-105">\[Deprecated.</span></span> <span data-ttu-id="926b5-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="926b5-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="926b5-107">Il `EffectsEnabled` metodo determina se gli effetti sono abilitati.</span><span class="sxs-lookup"><span data-stu-id="926b5-107">The `EffectsEnabled` method determines whether effects are enabled.</span></span> <span data-ttu-id="926b5-108">Se gli effetti sono disabilitati, rimangono nella sequenza temporale ma non ne viene eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="926b5-108">If effects are disabled, they remain in the timeline but are not rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="926b5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="926b5-109">Syntax</span></span>


```C++
HRESULT EffectsEnabled(
   BOOL *pfEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="926b5-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="926b5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="926b5-111">*pfEnabled*</span><span class="sxs-lookup"><span data-stu-id="926b5-111">*pfEnabled*</span></span> 
</dt> <dd>

<span data-ttu-id="926b5-112">Riceve un valore booleano che indica se gli effetti sono abilitati.</span><span class="sxs-lookup"><span data-stu-id="926b5-112">Receives a Boolean value indicating whether effects are enabled.</span></span> <span data-ttu-id="926b5-113">Se **true**, gli effetti sono abilitati.</span><span class="sxs-lookup"><span data-stu-id="926b5-113">If **TRUE**, effects are enabled.</span></span> <span data-ttu-id="926b5-114">Se **false**, gli effetti sono disabilitati.</span><span class="sxs-lookup"><span data-stu-id="926b5-114">If **FALSE**, effects are disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="926b5-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="926b5-115">Return value</span></span>

<span data-ttu-id="926b5-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="926b5-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="926b5-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="926b5-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="926b5-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="926b5-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="926b5-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="926b5-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="926b5-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="926b5-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="926b5-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="926b5-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="926b5-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="926b5-122">Requirements</span></span>



| <span data-ttu-id="926b5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="926b5-123">Requirement</span></span> | <span data-ttu-id="926b5-124">Valore</span><span class="sxs-lookup"><span data-stu-id="926b5-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="926b5-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="926b5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="926b5-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="926b5-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="926b5-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="926b5-127">Library</span></span><br/> | <dl> <span data-ttu-id="926b5-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="926b5-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="926b5-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="926b5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="926b5-130">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="926b5-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="926b5-131">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="926b5-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




