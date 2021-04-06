---
title: Proprietà HotKeyFullScreen di IMsRdpClientAdvancedSettings
description: Specifica il codice della chiave virtuale da aggiungere a CTRL + ALT per determinare la sostituzione del tasto di scelta rapida per passare alla modalità schermo intero.
ms.assetid: 75fda212-ec68-4b68-b7db-2bfcdee7a7de
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà HotKeyFullScreen
- Servizi Desktop remoto proprietà HotKeyFullScreen, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà HotKeyFullScreen
- Servizi Desktop remoto proprietà HotKeyFullScreen, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà HotKeyFullScreen
- Servizi Desktop remoto proprietà HotKeyFullScreen, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà HotKeyFullScreen
- Servizi Desktop remoto proprietà HotKeyFullScreen, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà HotKeyFullScreen
- Servizi Desktop remoto proprietà HotKeyFullScreen, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà HotKeyFullScreen
- Servizi Desktop remoto proprietà HotKeyFullScreen, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà HotKeyFullScreen
- Servizi Desktop remoto proprietà HotKeyFullScreen, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà HotKeyFullScreen
- Servizi Desktop remoto proprietà HotKeyFullScreen, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà HotKeyFullScreen
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyFullScreen
- IMsRdpClientAdvancedSettings.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.put_HotKeyFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9c53dd0c6dff9e47b87ea8c8697c20b3613a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963845"
---
# <a name="imsrdpclientadvancedsettingshotkeyfullscreen-property"></a><span data-ttu-id="ff136-120">Proprietà IMsRdpClientAdvancedSettings:: HotKeyFullScreen</span><span class="sxs-lookup"><span data-stu-id="ff136-120">IMsRdpClientAdvancedSettings::HotKeyFullScreen property</span></span>

<span data-ttu-id="ff136-121">Specifica il codice della chiave virtuale da aggiungere a CTRL + ALT per determinare la sostituzione del tasto di scelta rapida per passare alla modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="ff136-121">Specifies the virtual-key code to add to CTRL+ALT to determine the hotkey replacement for switching to full-screen mode.</span></span>

<span data-ttu-id="ff136-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="ff136-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff136-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ff136-123">Syntax</span></span>


```C++
HRESULT put_HotKeyFullScreen(
  [in]  LONG hotKeyFullScreen
);

HRESULT get_HotKeyFullScreen(
  [out] LONG *photKeyFullScreen
);
```



## <a name="property-value"></a><span data-ttu-id="ff136-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ff136-124">Property value</span></span>

<span data-ttu-id="ff136-125">Nuovo codice della chiave virtuale.</span><span class="sxs-lookup"><span data-stu-id="ff136-125">The new virtual-key code.</span></span> <span data-ttu-id="ff136-126">**VK \_ Annulla** è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="ff136-126">**VK\_CANCEL** is the default value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ff136-127">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ff136-127">Error codes</span></span>

<span data-ttu-id="ff136-128">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ff136-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff136-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="ff136-129">Remarks</span></span>

<span data-ttu-id="ff136-130">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ff136-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff136-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff136-131">Requirements</span></span>



| <span data-ttu-id="ff136-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff136-132">Requirement</span></span> | <span data-ttu-id="ff136-133">Valore</span><span class="sxs-lookup"><span data-stu-id="ff136-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff136-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff136-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ff136-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff136-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="ff136-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff136-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ff136-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff136-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="ff136-138">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ff136-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="ff136-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff136-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ff136-140">DLL</span><span class="sxs-lookup"><span data-stu-id="ff136-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff136-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff136-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ff136-142">IID</span><span class="sxs-lookup"><span data-stu-id="ff136-142">IID</span></span><br/>                      | <span data-ttu-id="ff136-143">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="ff136-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ff136-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ff136-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff136-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="ff136-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="ff136-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="ff136-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="ff136-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="ff136-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="ff136-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="ff136-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="ff136-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="ff136-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="ff136-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ff136-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="ff136-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ff136-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ff136-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="ff136-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





