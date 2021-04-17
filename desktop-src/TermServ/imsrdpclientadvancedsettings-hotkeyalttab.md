---
title: Proprietà HotKeyAltTab di IMsRdpClientAdvancedSettings
description: Specifica il codice della chiave virtuale da aggiungere a ALT per determinare la sostituzione del tasto di scelta rapida per ALT + TAB.
ms.assetid: d7066fb4-f53f-4e55-ba12-fb4078ece144
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà HotKeyAltTab
- Servizi Desktop remoto proprietà HotKeyAltTab, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà HotKeyAltTab
- Servizi Desktop remoto proprietà HotKeyAltTab, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà HotKeyAltTab
- Servizi Desktop remoto proprietà HotKeyAltTab, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà HotKeyAltTab
- Servizi Desktop remoto proprietà HotKeyAltTab, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà HotKeyAltTab
- Servizi Desktop remoto proprietà HotKeyAltTab, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà HotKeyAltTab
- Servizi Desktop remoto proprietà HotKeyAltTab, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà HotKeyAltTab
- Servizi Desktop remoto proprietà HotKeyAltTab, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà HotKeyAltTab
- Servizi Desktop remoto proprietà HotKeyAltTab, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà HotKeyAltTab
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltTab
- IMsRdpClientAdvancedSettings.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings2.HotKeyAltTab
- IMsRdpClientAdvancedSettings2.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings2.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings3.HotKeyAltTab
- IMsRdpClientAdvancedSettings3.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings3.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings4.HotKeyAltTab
- IMsRdpClientAdvancedSettings4.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings4.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings5.HotKeyAltTab
- IMsRdpClientAdvancedSettings5.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings5.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings6.HotKeyAltTab
- IMsRdpClientAdvancedSettings6.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings6.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings7.HotKeyAltTab
- IMsRdpClientAdvancedSettings7.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings7.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings8.HotKeyAltTab
- IMsRdpClientAdvancedSettings8.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings8.put_HotKeyAltTab
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec7834a95b83ec43553d0ced1e056860cfb5abe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400451"
---
# <a name="imsrdpclientadvancedsettingshotkeyalttab-property"></a><span data-ttu-id="a697c-120">Proprietà IMsRdpClientAdvancedSettings:: HotKeyAltTab</span><span class="sxs-lookup"><span data-stu-id="a697c-120">IMsRdpClientAdvancedSettings::HotKeyAltTab property</span></span>

<span data-ttu-id="a697c-121">Specifica il codice della chiave virtuale da aggiungere a ALT per determinare la sostituzione del tasto di scelta rapida per ALT + TAB.</span><span class="sxs-lookup"><span data-stu-id="a697c-121">Specifies the virtual-key code to add to ALT to determine the hotkey replacement for ALT+TAB.</span></span>

<span data-ttu-id="a697c-122">Questa proprietà è valida solo quando la proprietà [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) non è abilitata.</span><span class="sxs-lookup"><span data-stu-id="a697c-122">This property is valid only when the [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) property is not enabled.</span></span>

<span data-ttu-id="a697c-123">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a697c-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a697c-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a697c-124">Syntax</span></span>


```C++
HRESULT put_HotKeyAltTab(
  [in]  LONG hotKeyAltTab
);

HRESULT get_HotKeyAltTab(
  [out] LONG *photKeyAltTab
);
```



## <a name="property-value"></a><span data-ttu-id="a697c-125">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a697c-125">Property value</span></span>

<span data-ttu-id="a697c-126">Nuovo codice della chiave virtuale.</span><span class="sxs-lookup"><span data-stu-id="a697c-126">The new virtual-key code.</span></span> <span data-ttu-id="a697c-127">**VK \_ PRIMA** è il valore predefinito, con ALT + PGSU come sequenza risultante.</span><span class="sxs-lookup"><span data-stu-id="a697c-127">**VK\_PRIOR** is the default value, with ALT+PAGE UP as the resulting sequence.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a697c-128">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="a697c-128">Error codes</span></span>

<span data-ttu-id="a697c-129">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="a697c-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a697c-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="a697c-130">Remarks</span></span>

<span data-ttu-id="a697c-131">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a697c-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a697c-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a697c-132">Requirements</span></span>



| <span data-ttu-id="a697c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a697c-133">Requirement</span></span> | <span data-ttu-id="a697c-134">Valore</span><span class="sxs-lookup"><span data-stu-id="a697c-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a697c-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a697c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a697c-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a697c-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="a697c-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a697c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a697c-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a697c-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="a697c-139">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a697c-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="a697c-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a697c-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="a697c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a697c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a697c-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a697c-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="a697c-143">IID</span><span class="sxs-lookup"><span data-stu-id="a697c-143">IID</span></span><br/>                      | <span data-ttu-id="a697c-144">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="a697c-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a697c-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a697c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a697c-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="a697c-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="a697c-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="a697c-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="a697c-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="a697c-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="a697c-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="a697c-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="a697c-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="a697c-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="a697c-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="a697c-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="a697c-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="a697c-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="a697c-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="a697c-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





