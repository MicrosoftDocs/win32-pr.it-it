---
description: Il metodo GetPreviewMode recupera la modalità di anteprima per il gruppo.
ms.assetid: 635354e5-5cb2-4045-8a7f-21d31005c5f3
title: 'Metodo IAMTimelineGroup:: GetPreviewMode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetPreviewMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 724c35c57ff90216547a8a343b469cb627e32415
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333682"
---
# <a name="iamtimelinegroupgetpreviewmode-method"></a><span data-ttu-id="a4228-103">Metodo IAMTimelineGroup:: GetPreviewMode</span><span class="sxs-lookup"><span data-stu-id="a4228-103">IAMTimelineGroup::GetPreviewMode method</span></span>

> [!Note]  
> <span data-ttu-id="a4228-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="a4228-104">\[Deprecated.</span></span> <span data-ttu-id="a4228-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a4228-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a4228-106">Il `GetPreviewMode` metodo recupera la modalità di anteprima per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="a4228-106">The `GetPreviewMode` method retrieves the preview mode for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4228-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a4228-107">Syntax</span></span>


```C++
HRESULT GetPreviewMode(
   BOOL *pfPreview
);
```



## <a name="parameters"></a><span data-ttu-id="a4228-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a4228-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4228-109">*pfPreview*</span><span class="sxs-lookup"><span data-stu-id="a4228-109">*pfPreview*</span></span> 
</dt> <dd>

<span data-ttu-id="a4228-110">Riceve un valore booleano che indica la modalità di anteprima.</span><span class="sxs-lookup"><span data-stu-id="a4228-110">Receives a Boolean value indicating the preview mode.</span></span> <span data-ttu-id="a4228-111">Se **true**, il gruppo è in modalità di anteprima.</span><span class="sxs-lookup"><span data-stu-id="a4228-111">If **TRUE**, the group is in preview mode.</span></span> <span data-ttu-id="a4228-112">Se **false**, il gruppo è in modalità di creazione.</span><span class="sxs-lookup"><span data-stu-id="a4228-112">If **FALSE**, the group is in authoring mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4228-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a4228-113">Return value</span></span>

<span data-ttu-id="a4228-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a4228-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a4228-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a4228-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4228-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="a4228-116">Remarks</span></span>

<span data-ttu-id="a4228-117">In modalità di anteprima, i frame vengono eliminati durante le transizioni o gli effetti lenti per sincronizzare il video con l'audio.</span><span class="sxs-lookup"><span data-stu-id="a4228-117">In preview mode, frames are dropped during slow effects or transitions to keep the video synchronized with the audio.</span></span> <span data-ttu-id="a4228-118">Il video potrebbe sembrare frammentato come risultato.</span><span class="sxs-lookup"><span data-stu-id="a4228-118">The video might look choppy as a result.</span></span> <span data-ttu-id="a4228-119">In modalità di creazione, viene eseguito il rendering di ogni fotogramma.</span><span class="sxs-lookup"><span data-stu-id="a4228-119">In authoring mode, every frame is rendered.</span></span> <span data-ttu-id="a4228-120">La modalità di creazione è appropriata per la scrittura di file; per l'anteprima su schermo, il video potrebbe non essere sincronizzato con l'audio.</span><span class="sxs-lookup"><span data-stu-id="a4228-120">Authoring mode is appropriate for writing files; for on-screen preview, the video might become out of sync with the audio.</span></span>

> [!Note]  
> <span data-ttu-id="a4228-121">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="a4228-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a4228-122">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a4228-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a4228-123">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a4228-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a4228-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4228-124">Requirements</span></span>



| <span data-ttu-id="a4228-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4228-125">Requirement</span></span> | <span data-ttu-id="a4228-126">Valore</span><span class="sxs-lookup"><span data-stu-id="a4228-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4228-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a4228-127">Header</span></span><br/>  | <dl> <span data-ttu-id="a4228-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4228-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a4228-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="a4228-129">Library</span></span><br/> | <dl> <span data-ttu-id="a4228-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4228-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4228-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a4228-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4228-132">**Interfaccia IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="a4228-132">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="a4228-133">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="a4228-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




