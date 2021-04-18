---
title: Proprietà GrabFocusOnConnect di IMsRdpClientAdvancedSettings
description: Specifica se il controllo client deve avere lo stato attivo durante la connessione.
ms.assetid: c67fc284-6e07-4749-84bf-70c0ae4d1b2b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GrabFocusOnConnect
- Servizi Desktop remoto proprietà GrabFocusOnConnect, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà GrabFocusOnConnect
- Servizi Desktop remoto proprietà GrabFocusOnConnect, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà GrabFocusOnConnect
- Servizi Desktop remoto proprietà GrabFocusOnConnect, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà GrabFocusOnConnect
- Servizi Desktop remoto proprietà GrabFocusOnConnect, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà GrabFocusOnConnect
- Servizi Desktop remoto proprietà GrabFocusOnConnect, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà GrabFocusOnConnect
- Servizi Desktop remoto proprietà GrabFocusOnConnect, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà GrabFocusOnConnect
- Servizi Desktop remoto proprietà GrabFocusOnConnect, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà GrabFocusOnConnect
- Servizi Desktop remoto proprietà GrabFocusOnConnect, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà GrabFocusOnConnect
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings2.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings2.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings2.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings3.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings3.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings3.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings4.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings4.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings4.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings5.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings5.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings5.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings6.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings6.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings6.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings7.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings7.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings7.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings8.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings8.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings8.put_GrabFocusOnConnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e7fb04c00bd7aaaf4de1252d961206ffee0e6b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302464"
---
# <a name="imsrdpclientadvancedsettingsgrabfocusonconnect-property"></a><span data-ttu-id="0968e-120">Proprietà IMsRdpClientAdvancedSettings:: GrabFocusOnConnect</span><span class="sxs-lookup"><span data-stu-id="0968e-120">IMsRdpClientAdvancedSettings::GrabFocusOnConnect property</span></span>

<span data-ttu-id="0968e-121">Specifica se il controllo client deve avere lo stato attivo durante la connessione.</span><span class="sxs-lookup"><span data-stu-id="0968e-121">Specifies if the client control should have the focus while connecting.</span></span> <span data-ttu-id="0968e-122">Il controllo non tenterà di acquisire lo stato attivo da una finestra in esecuzione in un processo diverso.</span><span class="sxs-lookup"><span data-stu-id="0968e-122">The control will not attempt to grab focus from a window running in a different process.</span></span>

<span data-ttu-id="0968e-123">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="0968e-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0968e-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0968e-124">Syntax</span></span>


```C++
HRESULT put_GrabFocusOnConnect(
  [in]  VARIANT_BOOL fGrabFocusOnConnect
);

HRESULT get_GrabFocusOnConnect(
  [out] VARIANT_BOOL pfGrabFocusOnConnect
);
```



## <a name="property-value"></a><span data-ttu-id="0968e-125">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0968e-125">Property value</span></span>

<span data-ttu-id="0968e-126">Impostare questo parametro su **Variant \_ false** per disabilitare la funzionalità o la **variante \_ true** per abilitare la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="0968e-126">Set this parameter to **VARIANT\_FALSE** to disable the feature or **VARIANT\_TRUE** to enable the feature.</span></span> <span data-ttu-id="0968e-127">L'impostazione di questa proprietà su **Variant \_ false** impedisce al controllo di catturare lo stato attivo durante la connessione.</span><span class="sxs-lookup"><span data-stu-id="0968e-127">Setting this property to **VARIANT\_FALSE** prevents the control from grabbing focus when connecting.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0968e-128">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="0968e-128">Error codes</span></span>

<span data-ttu-id="0968e-129">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0968e-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="0968e-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="0968e-130">Remarks</span></span>

<span data-ttu-id="0968e-131">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0968e-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0968e-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0968e-132">Requirements</span></span>



| <span data-ttu-id="0968e-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="0968e-133">Requirement</span></span> | <span data-ttu-id="0968e-134">Valore</span><span class="sxs-lookup"><span data-stu-id="0968e-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0968e-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0968e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0968e-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0968e-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="0968e-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0968e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0968e-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0968e-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="0968e-139">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="0968e-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="0968e-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0968e-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="0968e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0968e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0968e-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0968e-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="0968e-143">IID</span><span class="sxs-lookup"><span data-stu-id="0968e-143">IID</span></span><br/>                      | <span data-ttu-id="0968e-144">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="0968e-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0968e-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0968e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0968e-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="0968e-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="0968e-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="0968e-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="0968e-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="0968e-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="0968e-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="0968e-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="0968e-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="0968e-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="0968e-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="0968e-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="0968e-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="0968e-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="0968e-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="0968e-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





