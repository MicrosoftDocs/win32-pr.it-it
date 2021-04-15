---
title: Proprietà HotKeyCtrlAltDel di IMsRdpClientAdvancedSettings
description: Specifica il codice della chiave virtuale da aggiungere a CTRL + ALT per determinare la sostituzione del tasto di scelta rapida per CTRL + ALT + CANC, detto anche firma di sicurezza sicura (SAS).
ms.assetid: bce55cdb-4444-4291-b443-9bc1b3743e23
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà HotKeyCtrlAltDel
- Servizi Desktop remoto proprietà HotKeyCtrlAltDel, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà HotKeyCtrlAltDel
- Servizi Desktop remoto proprietà HotKeyCtrlAltDel, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà HotKeyCtrlAltDel
- Servizi Desktop remoto proprietà HotKeyCtrlAltDel, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà HotKeyCtrlAltDel
- Servizi Desktop remoto proprietà HotKeyCtrlAltDel, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà HotKeyCtrlAltDel
- Servizi Desktop remoto proprietà HotKeyCtrlAltDel, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà HotKeyCtrlAltDel
- Servizi Desktop remoto proprietà HotKeyCtrlAltDel, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà HotKeyCtrlAltDel
- Servizi Desktop remoto proprietà HotKeyCtrlAltDel, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà HotKeyCtrlAltDel
- Servizi Desktop remoto proprietà HotKeyCtrlAltDel, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà HotKeyCtrlAltDel
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings2.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings2.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings2.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings3.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings3.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings3.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings4.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings4.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings4.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings5.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings5.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings5.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings6.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings6.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings6.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings7.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings7.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings7.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings8.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings8.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings8.put_HotKeyCtrlAltDel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00fa4c1f963841d0c1ea0375cdf11913b28d0286
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400315"
---
# <a name="imsrdpclientadvancedsettingshotkeyctrlaltdel-property"></a><span data-ttu-id="4f56e-120">Proprietà IMsRdpClientAdvancedSettings:: HotKeyCtrlAltDel</span><span class="sxs-lookup"><span data-stu-id="4f56e-120">IMsRdpClientAdvancedSettings::HotKeyCtrlAltDel property</span></span>

<span data-ttu-id="4f56e-121">Specifica il codice della chiave virtuale da aggiungere a CTRL + ALT per determinare la sostituzione del tasto di scelta rapida per CTRL + ALT + CANC, detto anche firma di sicurezza sicura (SAS).</span><span class="sxs-lookup"><span data-stu-id="4f56e-121">Specifies the virtual-key code to add to CTRL+ALT to determine the hotkey replacement for CTRL+ALT+DELETE, also called the secure attention sequence (SAS).</span></span>

> [!Note]  
> <span data-ttu-id="4f56e-122">CTRL + ALT + CANC non viene mai reindirizzato al server remoto, anche quando la proprietà [KeyboardHookMode](imsrdpclientsecuredsettings-keyboardhookmode.md) è abilitata; CTRL + ALT + CANC è la sequenza di firma di accesso condiviso locale.</span><span class="sxs-lookup"><span data-stu-id="4f56e-122">CTRL+ALT+DELETE is never redirected to the remote server, even when the [KeyboardHookMode](imsrdpclientsecuredsettings-keyboardhookmode.md) property is enabled; CTRL+ALT+DELETE is the local SAS sequence.</span></span>

 

<span data-ttu-id="4f56e-123">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="4f56e-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f56e-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f56e-124">Syntax</span></span>


```C++
HRESULT put_HotKeyCtrlAltDel(
  [in]  LONG hotKeyCtrlAltDel
);

HRESULT get_HotKeyCtrlAltDel(
  [out] LONG *photKeyCtrlAltDel
);
```



## <a name="property-value"></a><span data-ttu-id="4f56e-125">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4f56e-125">Property value</span></span>

<span data-ttu-id="4f56e-126">Nuovo codice della chiave virtuale.</span><span class="sxs-lookup"><span data-stu-id="4f56e-126">The new virtual-key code.</span></span> <span data-ttu-id="4f56e-127">**VK \_ END** è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="4f56e-127">**VK\_END** is the default.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4f56e-128">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="4f56e-128">Error codes</span></span>

<span data-ttu-id="4f56e-129">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4f56e-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f56e-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f56e-130">Remarks</span></span>

<span data-ttu-id="4f56e-131">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="4f56e-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f56e-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f56e-132">Requirements</span></span>



| <span data-ttu-id="4f56e-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f56e-133">Requirement</span></span> | <span data-ttu-id="4f56e-134">Valore</span><span class="sxs-lookup"><span data-stu-id="4f56e-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f56e-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f56e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4f56e-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f56e-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="4f56e-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f56e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4f56e-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f56e-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="4f56e-139">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="4f56e-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="4f56e-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f56e-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="4f56e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4f56e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f56e-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f56e-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="4f56e-143">IID</span><span class="sxs-lookup"><span data-stu-id="4f56e-143">IID</span></span><br/>                      | <span data-ttu-id="4f56e-144">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="4f56e-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4f56e-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f56e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f56e-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="4f56e-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="4f56e-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="4f56e-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="4f56e-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="4f56e-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="4f56e-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="4f56e-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="4f56e-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="4f56e-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="4f56e-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="4f56e-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="4f56e-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="4f56e-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="4f56e-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="4f56e-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





