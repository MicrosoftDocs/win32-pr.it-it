---
title: Proprietà EnableMouse di IMsRdpClientAdvancedSettings
description: Questa proprietà non è supportata. | Proprietà EnableMouse di IMsRdpClientAdvancedSettings
ms.assetid: 4f60fdfc-e1b9-4ac2-98e4-49331b072883
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà EnableMouse
- Servizi Desktop remoto proprietà EnableMouse, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà EnableMouse
- Servizi Desktop remoto proprietà EnableMouse, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà EnableMouse
- Servizi Desktop remoto proprietà EnableMouse, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà EnableMouse
- Servizi Desktop remoto proprietà EnableMouse, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà EnableMouse
- Servizi Desktop remoto proprietà EnableMouse, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà EnableMouse
- Servizi Desktop remoto proprietà EnableMouse, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà EnableMouse
- Servizi Desktop remoto proprietà EnableMouse, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà EnableMouse
- Servizi Desktop remoto proprietà EnableMouse, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà EnableMouse
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.EnableMouse
- IMsRdpClientAdvancedSettings.get_EnableMouse
- IMsRdpClientAdvancedSettings.put_EnableMouse
- IMsRdpClientAdvancedSettings2.EnableMouse
- IMsRdpClientAdvancedSettings2.get_EnableMouse
- IMsRdpClientAdvancedSettings2.put_EnableMouse
- IMsRdpClientAdvancedSettings3.EnableMouse
- IMsRdpClientAdvancedSettings3.get_EnableMouse
- IMsRdpClientAdvancedSettings3.put_EnableMouse
- IMsRdpClientAdvancedSettings4.EnableMouse
- IMsRdpClientAdvancedSettings4.get_EnableMouse
- IMsRdpClientAdvancedSettings4.put_EnableMouse
- IMsRdpClientAdvancedSettings5.EnableMouse
- IMsRdpClientAdvancedSettings5.get_EnableMouse
- IMsRdpClientAdvancedSettings5.put_EnableMouse
- IMsRdpClientAdvancedSettings6.EnableMouse
- IMsRdpClientAdvancedSettings6.get_EnableMouse
- IMsRdpClientAdvancedSettings6.put_EnableMouse
- IMsRdpClientAdvancedSettings7.EnableMouse
- IMsRdpClientAdvancedSettings7.get_EnableMouse
- IMsRdpClientAdvancedSettings7.put_EnableMouse
- IMsRdpClientAdvancedSettings8.EnableMouse
- IMsRdpClientAdvancedSettings8.get_EnableMouse
- IMsRdpClientAdvancedSettings8.put_EnableMouse
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0495ba7b48e431efe5746f40b353b5c1ad701d6a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969040"
---
# <a name="imsrdpclientadvancedsettingsenablemouse-property"></a><span data-ttu-id="60e1a-121">Proprietà IMsRdpClientAdvancedSettings:: EnableMouse</span><span class="sxs-lookup"><span data-stu-id="60e1a-121">IMsRdpClientAdvancedSettings::EnableMouse property</span></span>

<span data-ttu-id="60e1a-122">Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="60e1a-122">This property is not supported.</span></span>

<span data-ttu-id="60e1a-123">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="60e1a-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="60e1a-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60e1a-124">Syntax</span></span>


```C++
HRESULT put_EnableMouse(
  [in]  LONG enableMouse
);

HRESULT get_EnableMouse(
  [out] LONG *penableMouse
);
```



## <a name="property-value"></a><span data-ttu-id="60e1a-125">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="60e1a-125">Property value</span></span>

<span data-ttu-id="60e1a-126">Impostare questo parametro su 0 per disabilitare la funzionalità o un valore diverso da zero per abilitare la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="60e1a-126">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="60e1a-127">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="60e1a-127">Error codes</span></span>

<span data-ttu-id="60e1a-128">Restituisce un valore **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="60e1a-128">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="60e1a-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="60e1a-129">Remarks</span></span>

<span data-ttu-id="60e1a-130">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="60e1a-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60e1a-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60e1a-131">Requirements</span></span>



| <span data-ttu-id="60e1a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="60e1a-132">Requirement</span></span> | <span data-ttu-id="60e1a-133">Valore</span><span class="sxs-lookup"><span data-stu-id="60e1a-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60e1a-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60e1a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="60e1a-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="60e1a-135">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="60e1a-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60e1a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="60e1a-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="60e1a-137">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="60e1a-138">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="60e1a-138">End of client support</span></span><br/>    | <span data-ttu-id="60e1a-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="60e1a-139">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="60e1a-140">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="60e1a-140">End of server support</span></span><br/>    | <span data-ttu-id="60e1a-141">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="60e1a-141">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="60e1a-142">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="60e1a-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="60e1a-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60e1a-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="60e1a-144">DLL</span><span class="sxs-lookup"><span data-stu-id="60e1a-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60e1a-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60e1a-145"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="60e1a-146">IID</span><span class="sxs-lookup"><span data-stu-id="60e1a-146">IID</span></span><br/>                      | <span data-ttu-id="60e1a-147">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="60e1a-147">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="60e1a-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60e1a-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60e1a-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="60e1a-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="60e1a-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="60e1a-150">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="60e1a-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="60e1a-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="60e1a-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="60e1a-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="60e1a-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="60e1a-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="60e1a-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="60e1a-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="60e1a-155">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="60e1a-155">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="60e1a-156">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="60e1a-156">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





