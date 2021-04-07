---
title: Proprietà HotKeyAltSpace di IMsRdpClientAdvancedSettings
description: Specifica il codice della chiave virtuale da aggiungere a ALT per determinare la sostituzione del tasto di scelta rapida per ALT + barra spaziatrice.
ms.assetid: 943935e9-a6f1-496e-895c-e993755e25cc
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà HotKeyAltSpace
- Servizi Desktop remoto proprietà HotKeyAltSpace, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà HotKeyAltSpace
- Servizi Desktop remoto proprietà HotKeyAltSpace, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà HotKeyAltSpace
- Servizi Desktop remoto proprietà HotKeyAltSpace, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà HotKeyAltSpace
- Servizi Desktop remoto proprietà HotKeyAltSpace, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà HotKeyAltSpace
- Servizi Desktop remoto proprietà HotKeyAltSpace, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà HotKeyAltSpace
- Servizi Desktop remoto proprietà HotKeyAltSpace, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà HotKeyAltSpace
- Servizi Desktop remoto proprietà HotKeyAltSpace, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà HotKeyAltSpace
- Servizi Desktop remoto proprietà HotKeyAltSpace, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà HotKeyAltSpace
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltSpace
- IMsRdpClientAdvancedSettings.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings2.HotKeyAltSpace
- IMsRdpClientAdvancedSettings2.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings2.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings3.HotKeyAltSpace
- IMsRdpClientAdvancedSettings3.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings3.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings4.HotKeyAltSpace
- IMsRdpClientAdvancedSettings4.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings4.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings5.HotKeyAltSpace
- IMsRdpClientAdvancedSettings5.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings5.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings6.HotKeyAltSpace
- IMsRdpClientAdvancedSettings6.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings6.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings7.HotKeyAltSpace
- IMsRdpClientAdvancedSettings7.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings7.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings8.HotKeyAltSpace
- IMsRdpClientAdvancedSettings8.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings8.put_HotKeyAltSpace
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6b257bd04171f8bff22bbe91ee7310fafe89c13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964141"
---
# <a name="imsrdpclientadvancedsettingshotkeyaltspace-property"></a><span data-ttu-id="7dde7-120">Proprietà IMsRdpClientAdvancedSettings:: HotKeyAltSpace</span><span class="sxs-lookup"><span data-stu-id="7dde7-120">IMsRdpClientAdvancedSettings::HotKeyAltSpace property</span></span>

<span data-ttu-id="7dde7-121">Specifica il codice della chiave virtuale da aggiungere a ALT per determinare la sostituzione del tasto di scelta rapida per ALT + barra spaziatrice.</span><span class="sxs-lookup"><span data-stu-id="7dde7-121">Specifies the virtual-key code to add to ALT to determine the hotkey replacement for ALT+SPACE.</span></span>

<span data-ttu-id="7dde7-122">Questa proprietà è valida solo quando la proprietà [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) non è abilitata.</span><span class="sxs-lookup"><span data-stu-id="7dde7-122">This property is valid only when the [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) property is not enabled.</span></span>

<span data-ttu-id="7dde7-123">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="7dde7-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dde7-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7dde7-124">Syntax</span></span>


```C++
HRESULT put_HotKeyAltSpace(
  [in]  LONG hotKeyAltSpace
);

HRESULT get_HotKeyAltSpace(
  [out] LONG *photKeyAltSpace
);
```



## <a name="property-value"></a><span data-ttu-id="7dde7-125">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="7dde7-125">Property value</span></span>

<span data-ttu-id="7dde7-126">Nuovo codice della chiave virtuale.</span><span class="sxs-lookup"><span data-stu-id="7dde7-126">The new virtual-key code.</span></span> <span data-ttu-id="7dde7-127">**VK \_ DELETE** è l'impostazione predefinita, con ALT + CANC come sequenza risultante.</span><span class="sxs-lookup"><span data-stu-id="7dde7-127">**VK\_DELETE** is the default, with ALT+DELETE as the resulting sequence.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7dde7-128">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="7dde7-128">Error codes</span></span>

<span data-ttu-id="7dde7-129">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="7dde7-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dde7-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="7dde7-130">Remarks</span></span>

<span data-ttu-id="7dde7-131">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="7dde7-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7dde7-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7dde7-132">Requirements</span></span>



| <span data-ttu-id="7dde7-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="7dde7-133">Requirement</span></span> | <span data-ttu-id="7dde7-134">Valore</span><span class="sxs-lookup"><span data-stu-id="7dde7-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dde7-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7dde7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7dde7-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7dde7-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="7dde7-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7dde7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7dde7-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7dde7-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="7dde7-139">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="7dde7-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="7dde7-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7dde7-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="7dde7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7dde7-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7dde7-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7dde7-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="7dde7-143">IID</span><span class="sxs-lookup"><span data-stu-id="7dde7-143">IID</span></span><br/>                      | <span data-ttu-id="7dde7-144">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="7dde7-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7dde7-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7dde7-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dde7-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="7dde7-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="7dde7-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="7dde7-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="7dde7-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="7dde7-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="7dde7-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="7dde7-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="7dde7-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="7dde7-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="7dde7-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="7dde7-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="7dde7-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="7dde7-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="7dde7-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="7dde7-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





