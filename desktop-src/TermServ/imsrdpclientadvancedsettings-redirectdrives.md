---
title: Proprietà RedirectDrives di IMsRdpClientAdvancedSettings
description: Specifica se è consentito il reindirizzamento delle unità disco.
ms.assetid: 5ed4cd28-4a1f-4d3b-9f9d-bf44a8483209
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà RedirectDrives
- Servizi Desktop remoto proprietà RedirectDrives, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà RedirectDrives
- Servizi Desktop remoto proprietà RedirectDrives, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà RedirectDrives
- Servizi Desktop remoto proprietà RedirectDrives, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà RedirectDrives
- Servizi Desktop remoto proprietà RedirectDrives, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà RedirectDrives
- Servizi Desktop remoto proprietà RedirectDrives, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà RedirectDrives
- Servizi Desktop remoto proprietà RedirectDrives, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà RedirectDrives
- Servizi Desktop remoto proprietà RedirectDrives, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà RedirectDrives
- Servizi Desktop remoto proprietà RedirectDrives, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà RedirectDrives
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectDrives
- IMsRdpClientAdvancedSettings.get_RedirectDrives
- IMsRdpClientAdvancedSettings.put_RedirectDrives
- IMsRdpClientAdvancedSettings2.RedirectDrives
- IMsRdpClientAdvancedSettings2.get_RedirectDrives
- IMsRdpClientAdvancedSettings2.put_RedirectDrives
- IMsRdpClientAdvancedSettings3.RedirectDrives
- IMsRdpClientAdvancedSettings3.get_RedirectDrives
- IMsRdpClientAdvancedSettings3.put_RedirectDrives
- IMsRdpClientAdvancedSettings4.RedirectDrives
- IMsRdpClientAdvancedSettings4.get_RedirectDrives
- IMsRdpClientAdvancedSettings4.put_RedirectDrives
- IMsRdpClientAdvancedSettings5.RedirectDrives
- IMsRdpClientAdvancedSettings5.get_RedirectDrives
- IMsRdpClientAdvancedSettings5.put_RedirectDrives
- IMsRdpClientAdvancedSettings6.RedirectDrives
- IMsRdpClientAdvancedSettings6.get_RedirectDrives
- IMsRdpClientAdvancedSettings6.put_RedirectDrives
- IMsRdpClientAdvancedSettings7.RedirectDrives
- IMsRdpClientAdvancedSettings7.get_RedirectDrives
- IMsRdpClientAdvancedSettings7.put_RedirectDrives
- IMsRdpClientAdvancedSettings8.RedirectDrives
- IMsRdpClientAdvancedSettings8.get_RedirectDrives
- IMsRdpClientAdvancedSettings8.put_RedirectDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c83d24ae4ea4dae2760c1e468f4fa8b326a94c38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743655"
---
# <a name="imsrdpclientadvancedsettingsredirectdrives-property"></a><span data-ttu-id="0ba59-120">Proprietà IMsRdpClientAdvancedSettings:: RedirectDrives</span><span class="sxs-lookup"><span data-stu-id="0ba59-120">IMsRdpClientAdvancedSettings::RedirectDrives property</span></span>

<span data-ttu-id="0ba59-121">Specifica se è consentito il reindirizzamento delle unità disco.</span><span class="sxs-lookup"><span data-stu-id="0ba59-121">Specifies if redirection of disk drives is allowed.</span></span>

<span data-ttu-id="0ba59-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="0ba59-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ba59-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ba59-123">Syntax</span></span>


```C++
HRESULT put_RedirectDrives(
  [in]  VARIANT_BOOL redirectDrives
);

HRESULT get_RedirectDrives(
  [out] VARIANT_BOOL *predirectDrives
);
```



## <a name="property-value"></a><span data-ttu-id="0ba59-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0ba59-124">Property value</span></span>

<span data-ttu-id="0ba59-125">Impostare questo parametro su **Variant \_ true** per consentire il reindirizzamento o la **variante \_ false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0ba59-125">Set this parameter to **VARIANT\_TRUE** to allow redirection or **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="0ba59-126">**Variante \_ TRUE** chiede all'utente di confermare la concessione del reindirizzamento al momento della connessione, per motivi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="0ba59-126">**VARIANT\_TRUE** prompts the user to confirm allowing redirection at connection time, for security purposes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0ba59-127">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="0ba59-127">Error codes</span></span>

<span data-ttu-id="0ba59-128">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0ba59-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ba59-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ba59-129">Remarks</span></span>

<span data-ttu-id="0ba59-130">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0ba59-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ba59-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ba59-131">Requirements</span></span>



| <span data-ttu-id="0ba59-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ba59-132">Requirement</span></span> | <span data-ttu-id="0ba59-133">Valore</span><span class="sxs-lookup"><span data-stu-id="0ba59-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ba59-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ba59-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0ba59-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0ba59-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="0ba59-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ba59-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0ba59-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ba59-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="0ba59-138">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="0ba59-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="0ba59-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ba59-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="0ba59-140">DLL</span><span class="sxs-lookup"><span data-stu-id="0ba59-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ba59-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ba59-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="0ba59-142">IID</span><span class="sxs-lookup"><span data-stu-id="0ba59-142">IID</span></span><br/>                      | <span data-ttu-id="0ba59-143">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="0ba59-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0ba59-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ba59-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ba59-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="0ba59-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="0ba59-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="0ba59-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="0ba59-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="0ba59-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="0ba59-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="0ba59-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="0ba59-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="0ba59-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="0ba59-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="0ba59-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="0ba59-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="0ba59-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="0ba59-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="0ba59-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





