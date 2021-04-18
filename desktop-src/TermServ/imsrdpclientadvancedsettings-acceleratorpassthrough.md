---
title: Proprietà AcceleratorPassthrough di IMsRdpClientAdvancedSettings
description: Specifica se i tasti di scelta rapida devono essere passati al server.
ms.assetid: ad0053bc-e3a9-4cd5-a409-fab3e24ffffa
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà AcceleratorPassthrough
- Servizi Desktop remoto proprietà AcceleratorPassthrough, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà AcceleratorPassthrough
- Servizi Desktop remoto proprietà AcceleratorPassthrough, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà AcceleratorPassthrough
- Servizi Desktop remoto proprietà AcceleratorPassthrough, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà AcceleratorPassthrough
- Servizi Desktop remoto proprietà AcceleratorPassthrough, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà AcceleratorPassthrough
- Servizi Desktop remoto proprietà AcceleratorPassthrough, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà AcceleratorPassthrough
- Servizi Desktop remoto proprietà AcceleratorPassthrough, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà AcceleratorPassthrough
- Servizi Desktop remoto proprietà AcceleratorPassthrough, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà AcceleratorPassthrough
- Servizi Desktop remoto proprietà AcceleratorPassthrough, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà AcceleratorPassthrough
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings2.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings2.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings2.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings3.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings3.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings3.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings4.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings4.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings4.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings5.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings5.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings5.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings6.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings6.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings6.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings7.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings7.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings7.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings8.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings8.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings8.put_AcceleratorPassthrough
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c252c5c0477f331b66cf65b93ed2cab844fb88e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301319"
---
# <a name="imsrdpclientadvancedsettingsacceleratorpassthrough-property"></a><span data-ttu-id="85d87-120">Proprietà IMsRdpClientAdvancedSettings:: AcceleratorPassthrough</span><span class="sxs-lookup"><span data-stu-id="85d87-120">IMsRdpClientAdvancedSettings::AcceleratorPassthrough property</span></span>

<span data-ttu-id="85d87-121">Specifica se i tasti di scelta rapida devono essere passati al server.</span><span class="sxs-lookup"><span data-stu-id="85d87-121">Specifies if keyboard accelerators should be passed to the server.</span></span>

<span data-ttu-id="85d87-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="85d87-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="85d87-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85d87-123">Syntax</span></span>


```C++
HRESULT put_AcceleratorPassthrough(
  [in]  LONG acceleratorPassthrough
);

HRESULT get_AcceleratorPassthrough(
  [out] LONG *pacceleratorPassthrough
);
```



## <a name="property-value"></a><span data-ttu-id="85d87-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="85d87-124">Property value</span></span>

<span data-ttu-id="85d87-125">Impostare questo parametro su 0 per disabilitare la funzionalità o un valore diverso da zero per abilitare la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="85d87-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span> <span data-ttu-id="85d87-126">Il valore predefinito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="85d87-126">The default is a nonzero value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="85d87-127">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="85d87-127">Error codes</span></span>

<span data-ttu-id="85d87-128">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="85d87-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="85d87-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="85d87-129">Remarks</span></span>

<span data-ttu-id="85d87-130">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="85d87-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="85d87-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85d87-131">Requirements</span></span>



| <span data-ttu-id="85d87-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="85d87-132">Requirement</span></span> | <span data-ttu-id="85d87-133">Valore</span><span class="sxs-lookup"><span data-stu-id="85d87-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85d87-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85d87-134">Minimum supported client</span></span><br/> | <span data-ttu-id="85d87-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="85d87-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="85d87-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85d87-136">Minimum supported server</span></span><br/> | <span data-ttu-id="85d87-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85d87-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="85d87-138">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="85d87-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="85d87-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85d87-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="85d87-140">DLL</span><span class="sxs-lookup"><span data-stu-id="85d87-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85d87-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85d87-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="85d87-142">IID</span><span class="sxs-lookup"><span data-stu-id="85d87-142">IID</span></span><br/>                      | <span data-ttu-id="85d87-143">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="85d87-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="85d87-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85d87-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85d87-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="85d87-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="85d87-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="85d87-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="85d87-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="85d87-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="85d87-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="85d87-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="85d87-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="85d87-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="85d87-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="85d87-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="85d87-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="85d87-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="85d87-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="85d87-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





