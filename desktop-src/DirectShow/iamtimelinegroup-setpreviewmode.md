---
description: Il metodo SetPreviewMode imposta la modalità di anteprima per il gruppo.
ms.assetid: 40b7e9ac-30b3-454e-82ac-10ac99f1b86f
title: 'Metodo IAMTimelineGroup:: SetPreviewMode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetPreviewMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fe03e6be3572b6cc660e51c27551a316db990d80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331625"
---
# <a name="iamtimelinegroupsetpreviewmode-method"></a><span data-ttu-id="e1582-103">Metodo IAMTimelineGroup:: SetPreviewMode</span><span class="sxs-lookup"><span data-stu-id="e1582-103">IAMTimelineGroup::SetPreviewMode method</span></span>

> [!Note]  
> <span data-ttu-id="e1582-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="e1582-104">\[Deprecated.</span></span> <span data-ttu-id="e1582-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e1582-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e1582-106">Il metodo SetPreviewMode imposta la modalità di anteprima per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="e1582-106">The SetPreviewMode method sets the preview mode for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1582-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e1582-107">Syntax</span></span>


```C++
HRESULT SetPreviewMode(
   BOOL fPreview
);
```



## <a name="parameters"></a><span data-ttu-id="e1582-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e1582-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1582-109">*fPreview*</span><span class="sxs-lookup"><span data-stu-id="e1582-109">*fPreview*</span></span> 
</dt> <dd>

<span data-ttu-id="e1582-110">Modalità di anteprima.</span><span class="sxs-lookup"><span data-stu-id="e1582-110">The preview mode.</span></span> <span data-ttu-id="e1582-111">Se **true**, il gruppo è in modalità di anteprima.</span><span class="sxs-lookup"><span data-stu-id="e1582-111">If **TRUE**, the group is in preview mode.</span></span> <span data-ttu-id="e1582-112">Se **false**, il gruppo è in modalità di creazione.</span><span class="sxs-lookup"><span data-stu-id="e1582-112">If **FALSE**, the group is in authoring mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1582-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e1582-113">Return value</span></span>

<span data-ttu-id="e1582-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e1582-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e1582-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e1582-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1582-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="e1582-116">Remarks</span></span>

<span data-ttu-id="e1582-117">In modalità di anteprima, i frame vengono eliminati durante le transizioni o gli effetti lenti per sincronizzare il video con l'audio.</span><span class="sxs-lookup"><span data-stu-id="e1582-117">In preview mode, frames are dropped during slow effects or transitions to keep the video synchronized with the audio.</span></span> <span data-ttu-id="e1582-118">Il video potrebbe sembrare frammentato come risultato.</span><span class="sxs-lookup"><span data-stu-id="e1582-118">The video might look choppy as a result.</span></span> <span data-ttu-id="e1582-119">In modalità di creazione, viene eseguito il rendering di ogni fotogramma.</span><span class="sxs-lookup"><span data-stu-id="e1582-119">In authoring mode, every frame is rendered.</span></span> <span data-ttu-id="e1582-120">La modalità di creazione è appropriata per la scrittura di file; per l'anteprima su schermo, il video potrebbe non essere sincronizzato con l'audio.</span><span class="sxs-lookup"><span data-stu-id="e1582-120">Authoring mode is appropriate for writing files; for on-screen preview, the video might be out of sync with the audio.</span></span>

> [!Note]  
> <span data-ttu-id="e1582-121">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="e1582-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e1582-122">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e1582-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e1582-123">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e1582-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e1582-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1582-124">Requirements</span></span>



| <span data-ttu-id="e1582-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1582-125">Requirement</span></span> | <span data-ttu-id="e1582-126">Valore</span><span class="sxs-lookup"><span data-stu-id="e1582-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1582-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e1582-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e1582-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1582-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e1582-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="e1582-129">Library</span></span><br/> | <dl> <span data-ttu-id="e1582-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1582-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1582-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1582-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1582-132">**Interfaccia IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="e1582-132">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="e1582-133">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="e1582-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




