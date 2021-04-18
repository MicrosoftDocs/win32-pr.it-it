---
description: Il metodo semutato imposta lo stato di disattivazione dell'oggetto. Un oggetto disattivato non viene sottoposto a rendering, ma rimane nella sequenza temporale.
ms.assetid: 5dcd8533-8e58-4553-ac01-928723485f5d
title: 'Metodo IAMTimelineObj:: tomute (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetMuted
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac3f5b798ef56251fa64b55a92ae1e94e2fd61b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330816"
---
# <a name="iamtimelineobjsetmuted-method"></a><span data-ttu-id="4ba4f-104">Metodo IAMTimelineObj:: tomute</span><span class="sxs-lookup"><span data-stu-id="4ba4f-104">IAMTimelineObj::SetMuted method</span></span>

> [!Note]  
> <span data-ttu-id="4ba4f-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="4ba4f-105">\[Deprecated.</span></span> <span data-ttu-id="4ba4f-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4ba4f-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4ba4f-107">Il `SetMuted` metodo imposta lo stato di disattivazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4ba4f-107">The `SetMuted` method sets the object's muted state.</span></span> <span data-ttu-id="4ba4f-108">Un oggetto disattivato non viene sottoposto a rendering, ma rimane nella sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="4ba4f-108">A muted object is not rendered, but it remains in the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ba4f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ba4f-109">Syntax</span></span>


```C++
HRESULT SetMuted(
   BOOL newVal
);
```



## <a name="parameters"></a><span data-ttu-id="4ba4f-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="4ba4f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ba4f-111">*newVal*</span><span class="sxs-lookup"><span data-stu-id="4ba4f-111">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="4ba4f-112">Flag che specifica lo stato disattivato.</span><span class="sxs-lookup"><span data-stu-id="4ba4f-112">Flag that specifies the muted state.</span></span> <span data-ttu-id="4ba4f-113">Se **true**, l'oggetto e tutti i relativi elementi figlio sono disabilitati.</span><span class="sxs-lookup"><span data-stu-id="4ba4f-113">If **TRUE**, the object and all of its children are muted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ba4f-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4ba4f-114">Return value</span></span>

<span data-ttu-id="4ba4f-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4ba4f-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4ba4f-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4ba4f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ba4f-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="4ba4f-117">Remarks</span></span>

<span data-ttu-id="4ba4f-118">Il muting di un oggetto disattiva anche gli elementi figlio contenuti nell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4ba4f-118">Muting an object also mutes any children contained in the object.</span></span> <span data-ttu-id="4ba4f-119">Se, ad esempio, si disattiva una traccia, anche le transizioni, le origini e gli effetti di tale traccia vengono disabilitati.</span><span class="sxs-lookup"><span data-stu-id="4ba4f-119">For example, if you mute a track, the transitions, sources, and effects in that track are also muted.</span></span> <span data-ttu-id="4ba4f-120">Quando l'oggetto non viene più disattivato, i relativi elementi figlio ripristinano lo stato precedente, che potrebbe essere disattivato o non disattivato.</span><span class="sxs-lookup"><span data-stu-id="4ba4f-120">Once the object is no longer muted, its children revert to their previous state, which might be muted or unmuted.</span></span>

> [!Note]  
> <span data-ttu-id="4ba4f-121">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="4ba4f-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4ba4f-122">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4ba4f-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4ba4f-123">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4ba4f-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4ba4f-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ba4f-124">Requirements</span></span>



| <span data-ttu-id="4ba4f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ba4f-125">Requirement</span></span> | <span data-ttu-id="4ba4f-126">Valore</span><span class="sxs-lookup"><span data-stu-id="4ba4f-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ba4f-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4ba4f-127">Header</span></span><br/>  | <dl> <span data-ttu-id="4ba4f-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ba4f-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4ba4f-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="4ba4f-129">Library</span></span><br/> | <dl> <span data-ttu-id="4ba4f-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ba4f-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ba4f-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ba4f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ba4f-132">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="4ba4f-132">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="4ba4f-133">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="4ba4f-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




