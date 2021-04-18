---
title: Proprietà DisplayConnectionBar di IMsRdpClientAdvancedSettings
description: Specifica se utilizzare la barra di connessione. Il valore predefinito è VARIANT \_ true, che Abilita la proprietà.
ms.assetid: 251c0322-5589-423d-9694-004f847c173b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà DisplayConnectionBar
- Servizi Desktop remoto proprietà DisplayConnectionBar, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà DisplayConnectionBar
- Servizi Desktop remoto proprietà DisplayConnectionBar, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà DisplayConnectionBar
- Servizi Desktop remoto proprietà DisplayConnectionBar, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà DisplayConnectionBar
- Servizi Desktop remoto proprietà DisplayConnectionBar, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà DisplayConnectionBar
- Servizi Desktop remoto proprietà DisplayConnectionBar, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà DisplayConnectionBar
- Servizi Desktop remoto proprietà DisplayConnectionBar, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà DisplayConnectionBar
- Servizi Desktop remoto proprietà DisplayConnectionBar, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà DisplayConnectionBar
- Servizi Desktop remoto proprietà DisplayConnectionBar, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà DisplayConnectionBar
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DisplayConnectionBar
- IMsRdpClientAdvancedSettings.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings2.DisplayConnectionBar
- IMsRdpClientAdvancedSettings2.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings2.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings3.DisplayConnectionBar
- IMsRdpClientAdvancedSettings3.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings3.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings4.DisplayConnectionBar
- IMsRdpClientAdvancedSettings4.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings4.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings5.DisplayConnectionBar
- IMsRdpClientAdvancedSettings5.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings5.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings6.DisplayConnectionBar
- IMsRdpClientAdvancedSettings6.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings6.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings7.DisplayConnectionBar
- IMsRdpClientAdvancedSettings7.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings7.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings8.DisplayConnectionBar
- IMsRdpClientAdvancedSettings8.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings8.put_DisplayConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39dd85d0c8fd578931ed9ca8b85ac7a5ca01981e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301315"
---
# <a name="imsrdpclientadvancedsettingsdisplayconnectionbar-property"></a><span data-ttu-id="11488-121">IMsRdpClientAdvancedSettings::D Proprietà isplayConnectionBar</span><span class="sxs-lookup"><span data-stu-id="11488-121">IMsRdpClientAdvancedSettings::DisplayConnectionBar property</span></span>

<span data-ttu-id="11488-122">Specifica se utilizzare la barra di connessione.</span><span class="sxs-lookup"><span data-stu-id="11488-122">Specifies whether to use the connection bar.</span></span> <span data-ttu-id="11488-123">Il valore predefinito è **Variant \_ true**, che Abilita la proprietà.</span><span class="sxs-lookup"><span data-stu-id="11488-123">The default value is **VARIANT\_TRUE**, which enables the property.</span></span> <span data-ttu-id="11488-124">L'impostazione di questa proprietà su **Variant \_ false** in un ambiente di scripting sicuro restituisce **E \_ non riesce**.</span><span class="sxs-lookup"><span data-stu-id="11488-124">Setting this property to **VARIANT\_FALSE** in a safe scripting environment returns **E\_FAIL**.</span></span>

<span data-ttu-id="11488-125">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="11488-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="11488-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="11488-126">Syntax</span></span>


```C++
HRESULT put_DisplayConnectionBar(
  [in]  VARIANT_BOOL fDisplayConnectionBar
);

HRESULT get_DisplayConnectionBar(
  [out] VARIANT_BOOL *pfDisplayConnectionBar
);
```



## <a name="property-value"></a><span data-ttu-id="11488-127">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="11488-127">Property value</span></span>

<span data-ttu-id="11488-128">Impostare questo parametro su **Variant \_ false** per disabilitare la funzionalità o la **variante \_ true** per abilitare la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="11488-128">Set this parameter to **VARIANT\_FALSE** to disable the feature or **VARIANT\_TRUE** to enable the feature.</span></span> <span data-ttu-id="11488-129">Il valore predefinito è **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="11488-129">The default value is **VARIANT\_TRUE**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="11488-130">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="11488-130">Error codes</span></span>

<span data-ttu-id="11488-131">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="11488-131">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="11488-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="11488-132">Remarks</span></span>

<span data-ttu-id="11488-133">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="11488-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="11488-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11488-134">Requirements</span></span>



| <span data-ttu-id="11488-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="11488-135">Requirement</span></span> | <span data-ttu-id="11488-136">Valore</span><span class="sxs-lookup"><span data-stu-id="11488-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11488-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11488-137">Minimum supported client</span></span><br/> | <span data-ttu-id="11488-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11488-138">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="11488-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11488-139">Minimum supported server</span></span><br/> | <span data-ttu-id="11488-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11488-140">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="11488-141">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="11488-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="11488-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11488-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="11488-143">DLL</span><span class="sxs-lookup"><span data-stu-id="11488-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11488-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11488-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="11488-145">IID</span><span class="sxs-lookup"><span data-stu-id="11488-145">IID</span></span><br/>                      | <span data-ttu-id="11488-146">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="11488-146">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="11488-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11488-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11488-148">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="11488-148">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="11488-149">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="11488-149">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="11488-150">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="11488-150">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="11488-151">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="11488-151">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="11488-152">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="11488-152">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="11488-153">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="11488-153">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="11488-154">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="11488-154">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="11488-155">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="11488-155">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





