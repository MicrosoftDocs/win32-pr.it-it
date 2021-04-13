---
title: Proprietà ContainerHandledFullScreen di IMsTscAdvancedSettings
description: Specifica se la modalità a schermo intero gestita dal contenitore è abilitata.
ms.assetid: 67679323-4a74-4d91-abd0-607415295f3d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà ContainerHandledFullScreen
- Servizi Desktop remoto proprietà ContainerHandledFullScreen, interfaccia IMsTscAdvancedSettings
- Interfaccia IMsTscAdvancedSettings Servizi Desktop remoto, proprietà ContainerHandledFullScreen
- Servizi Desktop remoto proprietà ContainerHandledFullScreen, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà ContainerHandledFullScreen
- Servizi Desktop remoto proprietà ContainerHandledFullScreen, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà ContainerHandledFullScreen
- Servizi Desktop remoto proprietà ContainerHandledFullScreen, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà ContainerHandledFullScreen
- Servizi Desktop remoto proprietà ContainerHandledFullScreen, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà ContainerHandledFullScreen
- Servizi Desktop remoto proprietà ContainerHandledFullScreen, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà ContainerHandledFullScreen
- Servizi Desktop remoto proprietà ContainerHandledFullScreen, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà ContainerHandledFullScreen
- Servizi Desktop remoto proprietà ContainerHandledFullScreen, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà ContainerHandledFullScreen
- Servizi Desktop remoto proprietà ContainerHandledFullScreen, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà ContainerHandledFullScreen
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.ContainerHandledFullScreen
- IMsTscAdvancedSettings.get_ContainerHandledFullScreen
- IMsTscAdvancedSettings.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.put_ContainerHandledFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7442ce16e2ff30ca2d9b3bd529d37382d1df41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400739"
---
# <a name="imstscadvancedsettingscontainerhandledfullscreen-property"></a><span data-ttu-id="bf5b1-122">Proprietà IMsTscAdvancedSettings:: ContainerHandledFullScreen</span><span class="sxs-lookup"><span data-stu-id="bf5b1-122">IMsTscAdvancedSettings::ContainerHandledFullScreen property</span></span>

<span data-ttu-id="bf5b1-123">Specifica se la modalità a schermo intero gestita dal contenitore è abilitata.</span><span class="sxs-lookup"><span data-stu-id="bf5b1-123">Specifies whether the container-handled full-screen mode is enabled.</span></span>

> [!Note]  
> <span data-ttu-id="bf5b1-124">Il valore della proprietà **ContainerHandledFullScreen** non ha alcun effetto quando il controllo ActiveX Desktop remoto è sicuro per lo scripting e restituisce **\_ false** quando viene effettuato un tentativo di modificare il valore.</span><span class="sxs-lookup"><span data-stu-id="bf5b1-124">The value of the **ContainerHandledFullScreen** property has no effect when the Remote Desktop ActiveX control is safe for scripting, and returns **S\_FALSE** when an attempt is made to change the value.</span></span>

 

<span data-ttu-id="bf5b1-125">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="bf5b1-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf5b1-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf5b1-126">Syntax</span></span>


```C++
HRESULT put_ContainerHandledFullScreen(
  [in]  BOOL ContainerHandledFullScreen
);

HRESULT get_ContainerHandledFullScreen(
  [out] BOOL *pContainerHandledFullScreen
);
```



## <a name="property-value"></a><span data-ttu-id="bf5b1-127">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="bf5b1-127">Property value</span></span>

<span data-ttu-id="bf5b1-128">Impostare questo parametro su **true** per abilitare la modalità o un altro valore per disabilitare la modalità.</span><span class="sxs-lookup"><span data-stu-id="bf5b1-128">Set this parameter to **TRUE** to enable the mode or another value to disable the mode.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bf5b1-129">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="bf5b1-129">Error codes</span></span>

<span data-ttu-id="bf5b1-130">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="bf5b1-130">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="bf5b1-131">Restituisce **\_ false** se non è supportato.</span><span class="sxs-lookup"><span data-stu-id="bf5b1-131">Returns **S\_FALSE** if not supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf5b1-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf5b1-132">Remarks</span></span>

<span data-ttu-id="bf5b1-133">Quando questa modalità è abilitata, il contenitore corrente elabora il passaggio in e fuori dalla modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="bf5b1-133">When this mode is enabled, the current container processes the switch into and out of full-screen mode.</span></span> <span data-ttu-id="bf5b1-134">Questo metodo deve essere utilizzato solo se il contenitore corrente necessita di un controllo esteso sul comportamento della modalità a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="bf5b1-134">This method should be used only if the current container needs extensive control over full-screen mode behavior.</span></span> <span data-ttu-id="bf5b1-135">Quando questa proprietà è impostata, il controllo non entra o esce dalla modalità a schermo intero in risposta alla combinazione di tasti di scelta rapida della modalità schermo intero (CTRL + ALT + INTERr); vengono invece chiamati gli eventi [**IMsTscAxEvents:: OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md) e [**IMsTscAxEvents:: OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md) .</span><span class="sxs-lookup"><span data-stu-id="bf5b1-135">When this property is set, the control does not enter or leave full-screen mode in response to the full-screen mode shortcut key combination (CTRL+ALT+BREAK); instead, the [**IMsTscAxEvents::OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md) and [**IMsTscAxEvents::OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md) events are called.</span></span> <span data-ttu-id="bf5b1-136">Per ulteriori informazioni su questi eventi, vedere [**IMsTscAxEvents**](imstscaxevents-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="bf5b1-136">See [**IMsTscAxEvents**](imstscaxevents-interface.md) for more information about these events.</span></span>

<span data-ttu-id="bf5b1-137">La maggior parte delle applicazioni contenitore non dovrà usare la modalità a schermo intero gestita dal contenitore.</span><span class="sxs-lookup"><span data-stu-id="bf5b1-137">Most container applications will not need to use container-handled full-screen mode.</span></span>

<span data-ttu-id="bf5b1-138">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="bf5b1-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf5b1-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf5b1-139">Requirements</span></span>



| <span data-ttu-id="bf5b1-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf5b1-140">Requirement</span></span> | <span data-ttu-id="bf5b1-141">Valore</span><span class="sxs-lookup"><span data-stu-id="bf5b1-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf5b1-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf5b1-142">Minimum supported client</span></span><br/> | <span data-ttu-id="bf5b1-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf5b1-143">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="bf5b1-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf5b1-144">Minimum supported server</span></span><br/> | <span data-ttu-id="bf5b1-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf5b1-145">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="bf5b1-146">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="bf5b1-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="bf5b1-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf5b1-147"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="bf5b1-148">DLL</span><span class="sxs-lookup"><span data-stu-id="bf5b1-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf5b1-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf5b1-149"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="bf5b1-150">IID</span><span class="sxs-lookup"><span data-stu-id="bf5b1-150">IID</span></span><br/>                      | <span data-ttu-id="bf5b1-151">IID \_ IMsTscAdvancedSettings è definito come 809945cc-4b3b-4A92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="bf5b1-151">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bf5b1-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf5b1-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf5b1-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="bf5b1-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="bf5b1-154">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="bf5b1-154">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="bf5b1-155">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="bf5b1-155">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="bf5b1-156">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="bf5b1-156">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="bf5b1-157">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="bf5b1-157">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="bf5b1-158">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="bf5b1-158">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="bf5b1-159">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="bf5b1-159">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="bf5b1-160">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="bf5b1-160">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="bf5b1-161">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="bf5b1-161">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





