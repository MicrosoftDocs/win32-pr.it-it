---
title: Proprietà allowBackgroundInput di IMsTscAdvancedSettings
description: Specifica se la modalità di input in background è abilitata.
ms.assetid: 2b57ebe9-3aad-400c-bcfb-d01c759b453d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà allowBackgroundInput
- Servizi Desktop remoto proprietà allowBackgroundInput, interfaccia IMsTscAdvancedSettings
- Interfaccia IMsTscAdvancedSettings Servizi Desktop remoto, proprietà allowBackgroundInput
- Servizi Desktop remoto proprietà allowBackgroundInput, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà allowBackgroundInput
- Servizi Desktop remoto proprietà allowBackgroundInput, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà allowBackgroundInput
- Servizi Desktop remoto proprietà allowBackgroundInput, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà allowBackgroundInput
- Servizi Desktop remoto proprietà allowBackgroundInput, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà allowBackgroundInput
- Servizi Desktop remoto proprietà allowBackgroundInput, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà allowBackgroundInput
- Servizi Desktop remoto proprietà allowBackgroundInput, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà allowBackgroundInput
- Servizi Desktop remoto proprietà allowBackgroundInput, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà allowBackgroundInput
- Servizi Desktop remoto proprietà allowBackgroundInput, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà allowBackgroundInput
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.allowBackgroundInput
- IMsTscAdvancedSettings.get_allowBackgroundInput
- IMsTscAdvancedSettings.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings.allowBackgroundInput
- IMsRdpClientAdvancedSettings.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings2.allowBackgroundInput
- IMsRdpClientAdvancedSettings2.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings2.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings3.allowBackgroundInput
- IMsRdpClientAdvancedSettings3.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings3.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings4.allowBackgroundInput
- IMsRdpClientAdvancedSettings4.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings4.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings5.allowBackgroundInput
- IMsRdpClientAdvancedSettings5.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings5.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings6.allowBackgroundInput
- IMsRdpClientAdvancedSettings6.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings6.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings7.allowBackgroundInput
- IMsRdpClientAdvancedSettings7.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings7.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings8.allowBackgroundInput
- IMsRdpClientAdvancedSettings8.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings8.put_allowBackgroundInput
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 938725ea1aa3d774d5993be695ac8568963897fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400918"
---
# <a name="imstscadvancedsettingsallowbackgroundinput-property"></a><span data-ttu-id="b4141-122">Proprietà IMsTscAdvancedSettings:: allowBackgroundInput</span><span class="sxs-lookup"><span data-stu-id="b4141-122">IMsTscAdvancedSettings::allowBackgroundInput property</span></span>

<span data-ttu-id="b4141-123">Specifica se la modalità di input in background è abilitata.</span><span class="sxs-lookup"><span data-stu-id="b4141-123">Specifies whether background input mode is enabled.</span></span> <span data-ttu-id="b4141-124">Quando l'input in background è abilitato, il client può accettare l'input quando il client non ha lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="b4141-124">When background input is enabled the client can accept input when the client does not have focus.</span></span>

<span data-ttu-id="b4141-125">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="b4141-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4141-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4141-126">Syntax</span></span>


```C++
HRESULT put_allowBackgroundInput(
  [in]  LONG allowBackgroundInput
);

HRESULT get_allowBackgroundInput(
  [out] LONG *pallowBackgroundInput
);
```



## <a name="property-value"></a><span data-ttu-id="b4141-127">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b4141-127">Property value</span></span>

<span data-ttu-id="b4141-128">Impostare questo parametro su 0 per disabilitare la modalità di input in background o un valore diverso da zero per abilitare la modalità di input in background.</span><span class="sxs-lookup"><span data-stu-id="b4141-128">Set this parameter to 0 to disable background input mode or a nonzero value to enable background input mode.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b4141-129">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="b4141-129">Error codes</span></span>

<span data-ttu-id="b4141-130">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b4141-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4141-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="b4141-131">Remarks</span></span>

<span data-ttu-id="b4141-132">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="b4141-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4141-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4141-133">Requirements</span></span>



| <span data-ttu-id="b4141-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4141-134">Requirement</span></span> | <span data-ttu-id="b4141-135">Valore</span><span class="sxs-lookup"><span data-stu-id="b4141-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4141-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4141-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b4141-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b4141-137">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="b4141-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4141-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b4141-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4141-139">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="b4141-140">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="b4141-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="b4141-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4141-141"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="b4141-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b4141-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4141-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4141-143"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="b4141-144">IID</span><span class="sxs-lookup"><span data-stu-id="b4141-144">IID</span></span><br/>                      | <span data-ttu-id="b4141-145">IID \_ IMsTscAdvancedSettings è definito come 809945cc-4b3b-4A92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="b4141-145">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b4141-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4141-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4141-147">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="b4141-147">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="b4141-148">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="b4141-148">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="b4141-149">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="b4141-149">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="b4141-150">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="b4141-150">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="b4141-151">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="b4141-151">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="b4141-152">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="b4141-152">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="b4141-153">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="b4141-153">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="b4141-154">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="b4141-154">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="b4141-155">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="b4141-155">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





