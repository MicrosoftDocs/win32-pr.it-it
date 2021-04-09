---
title: Codici di errore DirectComposition (Dcomp. h)
description: In questa sezione vengono descritti i codici di errore specifici per DirectComposition.
ms.assetid: 8DFBFC34-DBD0-4731-8305-B33E90C96C54
topic_type:
- apiref
api_name:
- DCOMPOSITION_ERROR_ACCESS_DENIED
- DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED
- DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED
- DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED
api_location:
- Dcomp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96a76a7527bacf8caa756a0fad75ca70f4bf9a77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120579"
---
# <a name="directcomposition-error-codes"></a><span data-ttu-id="5a98a-103">Codici di errore DirectComposition</span><span class="sxs-lookup"><span data-stu-id="5a98a-103">DirectComposition error codes</span></span>

<span data-ttu-id="5a98a-104">Se si verifica un errore, Microsoft DirectComposition restituisce un codice come valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5a98a-104">If an error occurs, Microsoft DirectComposition returns a code as an **HRESULT** value.</span></span> <span data-ttu-id="5a98a-105">In questa sezione vengono descritti i codici di errore specifici per DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="5a98a-105">This section describes the error codes that are specific to DirectComposition.</span></span> <span data-ttu-id="5a98a-106">Per un elenco di codici di errore generali Component Object Model (COM), vedere [codici di errore com](/windows/desktop/com/com-error-codes).</span><span class="sxs-lookup"><span data-stu-id="5a98a-106">For a list of general Component Object Model (COM) error codes, see [COM Error Codes](/windows/desktop/com/com-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="5a98a-107"><span id="DCOMPOSITION_ERROR_ACCESS_DENIED"></span><span id="dcomposition_error_access_denied"></span>**\_accesso agli errori di DCOMPOSITION \_ \_ negato**</span><span class="sxs-lookup"><span data-stu-id="5a98a-107"><span id="DCOMPOSITION_ERROR_ACCESS_DENIED"></span><span id="dcomposition_error_access_denied"></span>**DCOMPOSITION\_ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="5a98a-108"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="5a98a-108"><dt>


</dt> <dt></span></span>



<span data-ttu-id="5a98a-109">L'handle di finestra specificato in una chiamata al metodo [**IDCompositionDevice:: CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) appartiene a un processo diverso da quello che ha creato l'oggetto dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5a98a-109">The window handle that was specified in a call to the [**IDCompositionDevice::CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) method belongs to a different process from the one that created the device object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a98a-110"><span id="DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED"></span><span id="dcomposition_error_surface_being_rendered"></span>**\_ \_ \_ viene \_ eseguito il rendering della superficie di errore DCOMPOSITION**</span><span class="sxs-lookup"><span data-stu-id="5a98a-110"><span id="DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED"></span><span id="dcomposition_error_surface_being_rendered"></span>**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="5a98a-111"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="5a98a-111"><dt>


</dt> <dt></span></span>



<span data-ttu-id="5a98a-112">È stato già eseguito il rendering della superficie quando l'applicazione ha chiamato il metodo [**IDCompositionSurface:: BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw), [**IDCompositionSurface:: SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw)o [**IDCompositionSurface:: ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) .</span><span class="sxs-lookup"><span data-stu-id="5a98a-112">The surface was already being rendered when the application called the [**IDCompositionSurface::BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw), [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), or [**IDCompositionSurface::ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) method.</span></span> <span data-ttu-id="5a98a-113">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="5a98a-113">For more information, see Remarks.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a98a-114"><span id="DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED"></span><span id="dcomposition_error_surface_not_being_rendered"></span>**\_ \_ \_ non \_ è stato eseguito il \_ rendering della superficie di errore DCOMPOSITION**</span><span class="sxs-lookup"><span data-stu-id="5a98a-114"><span id="DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED"></span><span id="dcomposition_error_surface_not_being_rendered"></span>**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="5a98a-115"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="5a98a-115"><dt>


</dt> <dt></span></span>



<span data-ttu-id="5a98a-116">L'applicazione ha chiamato il metodo [**IDCompositionSurface:: SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), [**IDCompositionSurface:: ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)o [**IDCompositionSurface:: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) per una superficie di cui non è stato eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="5a98a-116">The application called the [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), [**IDCompositionSurface::ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw), or [**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) method for a surface that is not being rendered.</span></span> <span data-ttu-id="5a98a-117">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="5a98a-117">For more information, see Remarks.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a98a-118"><span id="DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED"></span><span id="dcomposition_error_window_already_composed"></span>**\_finestra di errore DCOMPOSITION \_ \_ già \_ composta**</span><span class="sxs-lookup"><span data-stu-id="5a98a-118"><span id="DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED"></span><span id="dcomposition_error_window_already_composed"></span>**DCOMPOSITION\_ERROR\_WINDOW\_ALREADY\_COMPOSED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="5a98a-119"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="5a98a-119"><dt>


</dt> <dt></span></span>



<span data-ttu-id="5a98a-120">Il metodo [**IDCompositionDevice:: CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) è stato chiamato con HWND *e i* parametri in primo piano per i quali è già presente una struttura ad albero visuale. </span><span class="sxs-lookup"><span data-stu-id="5a98a-120">The [**IDCompositionDevice::CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) method was called with *hwnd* and *topmost* parameters for which a visual tree already exists.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a98a-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a98a-121">Remarks</span></span>

<span data-ttu-id="5a98a-122">Se una chiamata a [**IDCompositionSurface:: BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) è stata l'azione più recente:</span><span class="sxs-lookup"><span data-stu-id="5a98a-122">If a call to the [**IDCompositionSurface::BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) was the most recent action:</span></span>



| <span data-ttu-id="5a98a-123">Chiamata a questo metodo:</span><span class="sxs-lookup"><span data-stu-id="5a98a-123">Calling this method:</span></span>                                    | <span data-ttu-id="5a98a-124">Restituisce questo valore:</span><span class="sxs-lookup"><span data-stu-id="5a98a-124">Returns this value:</span></span>                               |
|---------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="5a98a-125">**BeginDraw**</span><span class="sxs-lookup"><span data-stu-id="5a98a-125">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="5a98a-126">**\_ \_ \_ viene \_ eseguito il rendering della superficie di errore DCOMPOSITION**</span><span class="sxs-lookup"><span data-stu-id="5a98a-126">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |
| [<span data-ttu-id="5a98a-127">**EndDraw**</span><span class="sxs-lookup"><span data-stu-id="5a98a-127">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="5a98a-128">\_OK</span><span class="sxs-lookup"><span data-stu-id="5a98a-128">S\_OK</span></span>                                             |
| [<span data-ttu-id="5a98a-129">**SuspendDraw**</span><span class="sxs-lookup"><span data-stu-id="5a98a-129">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="5a98a-130">\_OK</span><span class="sxs-lookup"><span data-stu-id="5a98a-130">S\_OK</span></span>                                             |
| [<span data-ttu-id="5a98a-131">**ResumeDraw**</span><span class="sxs-lookup"><span data-stu-id="5a98a-131">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="5a98a-132">**\_ \_ \_ viene \_ eseguito il rendering della superficie di errore DCOMPOSITION**</span><span class="sxs-lookup"><span data-stu-id="5a98a-132">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |



 

<span data-ttu-id="5a98a-133">Se una chiamata a [**IDCompositionSurface:: SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) è stata l'azione più recente:</span><span class="sxs-lookup"><span data-stu-id="5a98a-133">If a call to the [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) was the most recent action:</span></span>



| <span data-ttu-id="5a98a-134">Chiamata a questo metodo:</span><span class="sxs-lookup"><span data-stu-id="5a98a-134">Calling this method:</span></span>                                    | <span data-ttu-id="5a98a-135">Restituisce questo valore:</span><span class="sxs-lookup"><span data-stu-id="5a98a-135">Returns this value:</span></span>                               |
|---------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="5a98a-136">**BeginDraw**</span><span class="sxs-lookup"><span data-stu-id="5a98a-136">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="5a98a-137">**\_ \_ \_ viene \_ eseguito il rendering della superficie di errore DCOMPOSITION**</span><span class="sxs-lookup"><span data-stu-id="5a98a-137">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |
| [<span data-ttu-id="5a98a-138">**EndDraw**</span><span class="sxs-lookup"><span data-stu-id="5a98a-138">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="5a98a-139">\_OK</span><span class="sxs-lookup"><span data-stu-id="5a98a-139">S\_OK</span></span>                                             |
| [<span data-ttu-id="5a98a-140">**SuspendDraw**</span><span class="sxs-lookup"><span data-stu-id="5a98a-140">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="5a98a-141">**\_ \_ \_ viene \_ eseguito il rendering della superficie di errore DCOMPOSITION**</span><span class="sxs-lookup"><span data-stu-id="5a98a-141">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |
| [<span data-ttu-id="5a98a-142">**ResumeDraw**</span><span class="sxs-lookup"><span data-stu-id="5a98a-142">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="5a98a-143">\_OK</span><span class="sxs-lookup"><span data-stu-id="5a98a-143">S\_OK</span></span>                                             |



 

<span data-ttu-id="5a98a-144">Se una chiamata a [**IDCompositionSurface:: ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) è stata l'azione più recente:</span><span class="sxs-lookup"><span data-stu-id="5a98a-144">If a call to the [**IDCompositionSurface::ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) was the most recent action:</span></span>



| <span data-ttu-id="5a98a-145">Chiamata a questo metodo:</span><span class="sxs-lookup"><span data-stu-id="5a98a-145">Calling this method:</span></span>                                    | <span data-ttu-id="5a98a-146">Restituisce questo valore:</span><span class="sxs-lookup"><span data-stu-id="5a98a-146">Returns this value:</span></span>                                |
|---------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="5a98a-147">**BeginDraw**</span><span class="sxs-lookup"><span data-stu-id="5a98a-147">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="5a98a-148">**\_ \_ \_ viene \_ eseguito il rendering della superficie di errore DCOMPOSITION**</span><span class="sxs-lookup"><span data-stu-id="5a98a-148">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span>  |
| [<span data-ttu-id="5a98a-149">**EndDraw**</span><span class="sxs-lookup"><span data-stu-id="5a98a-149">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="5a98a-150">\_OK</span><span class="sxs-lookup"><span data-stu-id="5a98a-150">S\_OK</span></span>                                              |
| [<span data-ttu-id="5a98a-151">**SuspendDraw**</span><span class="sxs-lookup"><span data-stu-id="5a98a-151">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="5a98a-152">\_OK</span><span class="sxs-lookup"><span data-stu-id="5a98a-152">S\_OK</span></span>                                              |
| [<span data-ttu-id="5a98a-153">**ResumeDraw**</span><span class="sxs-lookup"><span data-stu-id="5a98a-153">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="5a98a-154">**\_viene eseguito il rendering della superficie di errore DCOMPOSITION \_ \_ \_ .**</span><span class="sxs-lookup"><span data-stu-id="5a98a-154">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED.**</span></span> |



 

<span data-ttu-id="5a98a-155">Se una chiamata a [**IDCompositionSurface:: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) è stata l'azione più recente:</span><span class="sxs-lookup"><span data-stu-id="5a98a-155">If a call to the [**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) was the most recent action:</span></span>



| <span data-ttu-id="5a98a-156">Chiamata a questo metodo:</span><span class="sxs-lookup"><span data-stu-id="5a98a-156">Calling this method:</span></span>                                    | <span data-ttu-id="5a98a-157">Restituisce questo valore:</span><span class="sxs-lookup"><span data-stu-id="5a98a-157">Returns this value:</span></span>                                     |
|---------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="5a98a-158">**BeginDraw**</span><span class="sxs-lookup"><span data-stu-id="5a98a-158">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="5a98a-159">\_OK</span><span class="sxs-lookup"><span data-stu-id="5a98a-159">S\_OK</span></span>                                                   |
| [<span data-ttu-id="5a98a-160">**EndDraw**</span><span class="sxs-lookup"><span data-stu-id="5a98a-160">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="5a98a-161">**\_ \_ \_ non \_ è stato eseguito il rendering della superficie di errore DCOMPOSITION \_ .**</span><span class="sxs-lookup"><span data-stu-id="5a98a-161">**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED.**</span></span> |
| [<span data-ttu-id="5a98a-162">**SuspendDraw**</span><span class="sxs-lookup"><span data-stu-id="5a98a-162">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="5a98a-163">**\_ \_ \_ non \_ è stato eseguito il rendering della superficie di errore DCOMPOSITION \_ .**</span><span class="sxs-lookup"><span data-stu-id="5a98a-163">**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED.**</span></span> |
| [<span data-ttu-id="5a98a-164">**ResumeDraw**</span><span class="sxs-lookup"><span data-stu-id="5a98a-164">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="5a98a-165">**\_ \_ \_ non \_ è stato eseguito il rendering della superficie di errore DCOMPOSITION \_ .**</span><span class="sxs-lookup"><span data-stu-id="5a98a-165">**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED.**</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="5a98a-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a98a-166">Requirements</span></span>



| <span data-ttu-id="5a98a-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a98a-167">Requirement</span></span> | <span data-ttu-id="5a98a-168">Valore</span><span class="sxs-lookup"><span data-stu-id="5a98a-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5a98a-169">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a98a-169">Minimum supported client</span></span><br/> | <span data-ttu-id="5a98a-170">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5a98a-170">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5a98a-171">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a98a-171">Minimum supported server</span></span><br/> | <span data-ttu-id="5a98a-172">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5a98a-172">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5a98a-173">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a98a-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a98a-174"><dt>Dcomp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a98a-174"><dt>Dcomp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a98a-175">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a98a-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a98a-176">Riferimento a DirectComposition</span><span class="sxs-lookup"><span data-stu-id="5a98a-176">DirectComposition Reference</span></span>](reference.md)
</dt> </dl>

 

