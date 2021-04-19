---
title: Proprietà DedicatedTerminal di IMsRdpClientAdvancedSettings
description: Questa proprietà non è supportata. | Proprietà DedicatedTerminal di IMsRdpClientAdvancedSettings
ms.assetid: 40d54c88-dcac-4e7d-b389-a65caeb6960e
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà DedicatedTerminal
- Servizi Desktop remoto proprietà DedicatedTerminal, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà DedicatedTerminal
- Servizi Desktop remoto proprietà DedicatedTerminal, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà DedicatedTerminal
- Servizi Desktop remoto proprietà DedicatedTerminal, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà DedicatedTerminal
- Servizi Desktop remoto proprietà DedicatedTerminal, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà DedicatedTerminal
- Servizi Desktop remoto proprietà DedicatedTerminal, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà DedicatedTerminal
- Servizi Desktop remoto proprietà DedicatedTerminal, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà DedicatedTerminal
- Servizi Desktop remoto proprietà DedicatedTerminal, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà DedicatedTerminal
- Servizi Desktop remoto proprietà DedicatedTerminal, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà DedicatedTerminal
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DedicatedTerminal
- IMsRdpClientAdvancedSettings.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings2.DedicatedTerminal
- IMsRdpClientAdvancedSettings2.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings2.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings3.DedicatedTerminal
- IMsRdpClientAdvancedSettings3.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings3.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings4.DedicatedTerminal
- IMsRdpClientAdvancedSettings4.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings4.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings5.DedicatedTerminal
- IMsRdpClientAdvancedSettings5.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings5.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings6.DedicatedTerminal
- IMsRdpClientAdvancedSettings6.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings6.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings7.DedicatedTerminal
- IMsRdpClientAdvancedSettings7.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings7.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings8.DedicatedTerminal
- IMsRdpClientAdvancedSettings8.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings8.put_DedicatedTerminal
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee005439b38e21c5ed05d035545cc5600993cd5c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321638"
---
# <a name="imsrdpclientadvancedsettingsdedicatedterminal-property"></a><span data-ttu-id="85f5e-121">IMsRdpClientAdvancedSettings::D Proprietà edicatedTerminal</span><span class="sxs-lookup"><span data-stu-id="85f5e-121">IMsRdpClientAdvancedSettings::DedicatedTerminal property</span></span>

<span data-ttu-id="85f5e-122">Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="85f5e-122">This property is not supported.</span></span>

<span data-ttu-id="85f5e-123">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="85f5e-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="85f5e-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85f5e-124">Syntax</span></span>


```C++
HRESULT put_DedicatedTerminal(
  [in]  LONG dedicatedTerminal
);

HRESULT get_DedicatedTerminal(
  [out] LONG *pdedicatedTerminal
);
```



## <a name="property-value"></a><span data-ttu-id="85f5e-125">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="85f5e-125">Property value</span></span>

<span data-ttu-id="85f5e-126">Impostare questo parametro su 0 per disabilitare la funzionalità o un valore diverso da zero per abilitare la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="85f5e-126">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="85f5e-127">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="85f5e-127">Error codes</span></span>

<span data-ttu-id="85f5e-128">Restituisce un valore **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="85f5e-128">Returns **S\_FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="85f5e-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85f5e-129">Requirements</span></span>



| <span data-ttu-id="85f5e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="85f5e-130">Requirement</span></span> | <span data-ttu-id="85f5e-131">Valore</span><span class="sxs-lookup"><span data-stu-id="85f5e-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85f5e-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85f5e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="85f5e-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="85f5e-133">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="85f5e-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85f5e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="85f5e-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="85f5e-135">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="85f5e-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="85f5e-136">End of client support</span></span><br/>    | <span data-ttu-id="85f5e-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="85f5e-137">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="85f5e-138">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="85f5e-138">End of server support</span></span><br/>    | <span data-ttu-id="85f5e-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="85f5e-139">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="85f5e-140">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="85f5e-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="85f5e-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85f5e-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="85f5e-142">DLL</span><span class="sxs-lookup"><span data-stu-id="85f5e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85f5e-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85f5e-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="85f5e-144">IID</span><span class="sxs-lookup"><span data-stu-id="85f5e-144">IID</span></span><br/>                      | <span data-ttu-id="85f5e-145">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="85f5e-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="85f5e-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85f5e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85f5e-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="85f5e-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="85f5e-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="85f5e-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="85f5e-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="85f5e-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="85f5e-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="85f5e-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="85f5e-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="85f5e-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="85f5e-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="85f5e-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="85f5e-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="85f5e-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="85f5e-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="85f5e-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





