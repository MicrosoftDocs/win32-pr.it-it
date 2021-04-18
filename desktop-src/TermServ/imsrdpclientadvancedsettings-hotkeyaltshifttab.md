---
title: Proprietà HotKeyAltShiftTab di IMsRdpClientAdvancedSettings
description: Specifica il codice della chiave virtuale da aggiungere a ALT per determinare la sostituzione del tasto di scelta rapida per ALT + MAIUSC + TAB.
ms.assetid: da52f2fb-15cc-4d55-b26e-cf5465290889
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà HotKeyAltShiftTab
- Servizi Desktop remoto proprietà HotKeyAltShiftTab, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà HotKeyAltShiftTab
- Servizi Desktop remoto proprietà HotKeyAltShiftTab, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà HotKeyAltShiftTab
- Servizi Desktop remoto proprietà HotKeyAltShiftTab, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà HotKeyAltShiftTab
- Servizi Desktop remoto proprietà HotKeyAltShiftTab, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà HotKeyAltShiftTab
- Servizi Desktop remoto proprietà HotKeyAltShiftTab, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà HotKeyAltShiftTab
- Servizi Desktop remoto proprietà HotKeyAltShiftTab, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà HotKeyAltShiftTab
- Servizi Desktop remoto proprietà HotKeyAltShiftTab, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà HotKeyAltShiftTab
- Servizi Desktop remoto proprietà HotKeyAltShiftTab, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà HotKeyAltShiftTab
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings2.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings2.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings2.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings3.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings3.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings3.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings4.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings4.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings4.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings5.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings5.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings5.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings6.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings6.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings6.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings7.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings7.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings7.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings8.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings8.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings8.put_HotKeyAltShiftTab
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9819ddcba3f9cb10450525467eb8accce958c2f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301314"
---
# <a name="imsrdpclientadvancedsettingshotkeyaltshifttab-property"></a><span data-ttu-id="55c8a-120">Proprietà IMsRdpClientAdvancedSettings:: HotKeyAltShiftTab</span><span class="sxs-lookup"><span data-stu-id="55c8a-120">IMsRdpClientAdvancedSettings::HotKeyAltShiftTab property</span></span>

<span data-ttu-id="55c8a-121">Specifica il codice della chiave virtuale da aggiungere a ALT per determinare la sostituzione del tasto di scelta rapida per ALT + MAIUSC + TAB.</span><span class="sxs-lookup"><span data-stu-id="55c8a-121">Specifies the virtual-key code to add to ALT to determine the hotkey replacement for ALT+SHIFT+TAB.</span></span>

<span data-ttu-id="55c8a-122">Questa proprietà è valida solo quando la proprietà [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) non è abilitata.</span><span class="sxs-lookup"><span data-stu-id="55c8a-122">This property is valid only when the [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) property is not enabled.</span></span>

<span data-ttu-id="55c8a-123">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="55c8a-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="55c8a-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55c8a-124">Syntax</span></span>


```C++
HRESULT put_HotKeyAltShiftTab(
  [in]  LONG hotKeyAltShiftTab
);

HRESULT get_HotKeyAltShiftTab(
  [out] LONG *photKeyAltShiftTab
);
```



## <a name="property-value"></a><span data-ttu-id="55c8a-125">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="55c8a-125">Property value</span></span>

<span data-ttu-id="55c8a-126">Nuovo codice della chiave virtuale.</span><span class="sxs-lookup"><span data-stu-id="55c8a-126">The new virtual-key code.</span></span> <span data-ttu-id="55c8a-127">**VK \_ NEXT** è il valore predefinito, con ALT + PGGIÙ come sequenza risultante.</span><span class="sxs-lookup"><span data-stu-id="55c8a-127">**VK\_NEXT** is the default value, with ALT+PAGE DOWN as the resulting sequence.</span></span>

## <a name="error-codes"></a><span data-ttu-id="55c8a-128">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="55c8a-128">Error codes</span></span>

<span data-ttu-id="55c8a-129">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="55c8a-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="55c8a-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="55c8a-130">Remarks</span></span>

<span data-ttu-id="55c8a-131">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="55c8a-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55c8a-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55c8a-132">Requirements</span></span>



| <span data-ttu-id="55c8a-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="55c8a-133">Requirement</span></span> | <span data-ttu-id="55c8a-134">Valore</span><span class="sxs-lookup"><span data-stu-id="55c8a-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55c8a-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55c8a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="55c8a-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55c8a-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="55c8a-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55c8a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="55c8a-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55c8a-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="55c8a-139">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="55c8a-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="55c8a-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55c8a-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="55c8a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="55c8a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55c8a-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55c8a-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="55c8a-143">IID</span><span class="sxs-lookup"><span data-stu-id="55c8a-143">IID</span></span><br/>                      | <span data-ttu-id="55c8a-144">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="55c8a-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="55c8a-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55c8a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55c8a-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="55c8a-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="55c8a-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="55c8a-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="55c8a-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="55c8a-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="55c8a-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="55c8a-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="55c8a-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="55c8a-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="55c8a-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="55c8a-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="55c8a-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="55c8a-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="55c8a-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="55c8a-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





