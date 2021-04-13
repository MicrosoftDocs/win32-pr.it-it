---
title: Proprietà UIParentWindowHandle di IMsRdpClientNonScriptable2
description: Imposta o recupera l'handle della finestra che deve essere la finestra padre di tutte le finestre di dialogo visualizzate dal controllo. Ciò consente a qualsiasi finestra visualizzata dal controllo di essere modale correttamente rispetto a qualsiasi finestra visualizzata dall'applicazione padre.
ms.assetid: 5ecf1fc3-492e-4faf-89c5-7f7abb3778a0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà UIParentWindowHandle
- Servizi Desktop remoto proprietà UIParentWindowHandle, interfaccia IMsRdpClientNonScriptable2
- Interfaccia IMsRdpClientNonScriptable2 Servizi Desktop remoto, proprietà UIParentWindowHandle
- Servizi Desktop remoto proprietà UIParentWindowHandle, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, proprietà UIParentWindowHandle
- Servizi Desktop remoto proprietà UIParentWindowHandle, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà UIParentWindowHandle
- Servizi Desktop remoto proprietà UIParentWindowHandle, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà UIParentWindowHandle
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable2.UIParentWindowHandle
- IMsRdpClientNonScriptable2.get_UIParentWindowHandle
- IMsRdpClientNonScriptable2.put_UIParentWindowHandle
- IMsRdpClientNonScriptable3.UIParentWindowHandle
- IMsRdpClientNonScriptable3.get_UIParentWindowHandle
- IMsRdpClientNonScriptable3.put_UIParentWindowHandle
- IMsRdpClientNonScriptable4.UIParentWindowHandle
- IMsRdpClientNonScriptable4.get_UIParentWindowHandle
- IMsRdpClientNonScriptable4.put_UIParentWindowHandle
- IMsRdpClientNonScriptable5.UIParentWindowHandle
- IMsRdpClientNonScriptable5.get_UIParentWindowHandle
- IMsRdpClientNonScriptable5.put_UIParentWindowHandle
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5526fd1a699c87e32c6acadd238c2144d00a10be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475226"
---
# <a name="imsrdpclientnonscriptable2uiparentwindowhandle-property"></a><span data-ttu-id="47be4-113">Proprietà IMsRdpClientNonScriptable2:: UIParentWindowHandle</span><span class="sxs-lookup"><span data-stu-id="47be4-113">IMsRdpClientNonScriptable2::UIParentWindowHandle property</span></span>

<span data-ttu-id="47be4-114">Imposta o recupera l'handle della finestra che deve essere la finestra padre di tutte le finestre di dialogo visualizzate dal controllo.</span><span class="sxs-lookup"><span data-stu-id="47be4-114">Sets or retrieves the window handle to be the parent window for any dialog boxes displayed by the control.</span></span> <span data-ttu-id="47be4-115">Ciò consente a qualsiasi finestra visualizzata dal controllo di essere modale correttamente rispetto a qualsiasi finestra visualizzata dall'applicazione padre.</span><span class="sxs-lookup"><span data-stu-id="47be4-115">This allows any windows displayed by the control to be properly modal with respect to any windows displayed by the parent application.</span></span>

<span data-ttu-id="47be4-116">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="47be4-116">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="47be4-117">Sintassi</span><span class="sxs-lookup"><span data-stu-id="47be4-117">Syntax</span></span>


```C++
HRESULT put_UIParentWindowHandle(
  [in]  HWND hwndUIParentWindowHandle
);

HRESULT get_UIParentWindowHandle(
  [out] HWND *phwndUIParentWindowHandle
);
```



## <a name="property-value"></a><span data-ttu-id="47be4-118">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="47be4-118">Property value</span></span>

<span data-ttu-id="47be4-119">Nuovo handle della finestra.</span><span class="sxs-lookup"><span data-stu-id="47be4-119">The new window handle.</span></span>

## <a name="error-codes"></a><span data-ttu-id="47be4-120">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="47be4-120">Error codes</span></span>

<span data-ttu-id="47be4-121">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="47be4-121">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="47be4-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="47be4-122">Remarks</span></span>

<span data-ttu-id="47be4-123">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="47be4-123">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="47be4-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47be4-124">Requirements</span></span>



| <span data-ttu-id="47be4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="47be4-125">Requirement</span></span> | <span data-ttu-id="47be4-126">Valore</span><span class="sxs-lookup"><span data-stu-id="47be4-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="47be4-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47be4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="47be4-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47be4-128">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="47be4-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47be4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="47be4-130">Windows Server 2008, Windows Server 2008 con SP1</span><span class="sxs-lookup"><span data-stu-id="47be4-130">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                                  |
| <span data-ttu-id="47be4-131">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="47be4-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="47be4-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47be4-132"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="47be4-133">DLL</span><span class="sxs-lookup"><span data-stu-id="47be4-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47be4-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47be4-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="47be4-135">IID</span><span class="sxs-lookup"><span data-stu-id="47be4-135">IID</span></span><br/>                      | <span data-ttu-id="47be4-136">IID \_ IMsRdpClientNonScriptable2 è definito come 17a5e535-4072-4fa4-AF32-c8d0d47345e9</span><span class="sxs-lookup"><span data-stu-id="47be4-136">IID\_IMsRdpClientNonScriptable2 is defined as 17a5e535-4072-4fa4-af32-c8d0d47345e9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="47be4-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="47be4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47be4-138">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="47be4-138">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="47be4-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="47be4-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="47be4-140">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="47be4-140">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="47be4-141">**OnAuthenticationWarningDisplayed**</span><span class="sxs-lookup"><span data-stu-id="47be4-141">**OnAuthenticationWarningDisplayed**</span></span>](imstscaxevents-onauthenticationwarningdisplayed.md)
</dt> <dt>

[<span data-ttu-id="47be4-142">**OnAuthenticationWarningDismissed**</span><span class="sxs-lookup"><span data-stu-id="47be4-142">**OnAuthenticationWarningDismissed**</span></span>](imstscaxevents-onauthenticationwarningdismissed.md)
</dt> <dt>

[<span data-ttu-id="47be4-143">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="47be4-143">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> </dl>

 

 





