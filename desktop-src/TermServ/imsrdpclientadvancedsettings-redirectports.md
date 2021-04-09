---
title: Proprietà RedirectPorts di IMsRdpClientAdvancedSettings
description: Specifica se è consentito il reindirizzamento delle porte locali (ad esempio, COM e LPT).
ms.assetid: 85e1e40d-8da7-4333-ae96-2bfa44479267
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà RedirectPorts
- Servizi Desktop remoto proprietà RedirectPorts, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà RedirectPorts
- Servizi Desktop remoto proprietà RedirectPorts, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà RedirectPorts
- Servizi Desktop remoto proprietà RedirectPorts, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà RedirectPorts
- Servizi Desktop remoto proprietà RedirectPorts, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà RedirectPorts
- Servizi Desktop remoto proprietà RedirectPorts, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà RedirectPorts
- Servizi Desktop remoto proprietà RedirectPorts, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà RedirectPorts
- Servizi Desktop remoto proprietà RedirectPorts, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà RedirectPorts
- Servizi Desktop remoto proprietà RedirectPorts, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà RedirectPorts
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectPorts
- IMsRdpClientAdvancedSettings.get_RedirectPorts
- IMsRdpClientAdvancedSettings.put_RedirectPorts
- IMsRdpClientAdvancedSettings2.RedirectPorts
- IMsRdpClientAdvancedSettings2.get_RedirectPorts
- IMsRdpClientAdvancedSettings2.put_RedirectPorts
- IMsRdpClientAdvancedSettings3.RedirectPorts
- IMsRdpClientAdvancedSettings3.get_RedirectPorts
- IMsRdpClientAdvancedSettings3.put_RedirectPorts
- IMsRdpClientAdvancedSettings4.RedirectPorts
- IMsRdpClientAdvancedSettings4.get_RedirectPorts
- IMsRdpClientAdvancedSettings4.put_RedirectPorts
- IMsRdpClientAdvancedSettings5.RedirectPorts
- IMsRdpClientAdvancedSettings5.get_RedirectPorts
- IMsRdpClientAdvancedSettings5.put_RedirectPorts
- IMsRdpClientAdvancedSettings6.RedirectPorts
- IMsRdpClientAdvancedSettings6.get_RedirectPorts
- IMsRdpClientAdvancedSettings6.put_RedirectPorts
- IMsRdpClientAdvancedSettings7.RedirectPorts
- IMsRdpClientAdvancedSettings7.get_RedirectPorts
- IMsRdpClientAdvancedSettings7.put_RedirectPorts
- IMsRdpClientAdvancedSettings8.RedirectPorts
- IMsRdpClientAdvancedSettings8.get_RedirectPorts
- IMsRdpClientAdvancedSettings8.put_RedirectPorts
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 714b26081bb4caadface283553b1dd3ebd91192d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963775"
---
# <a name="imsrdpclientadvancedsettingsredirectports-property"></a><span data-ttu-id="579ca-120">Proprietà IMsRdpClientAdvancedSettings:: RedirectPorts</span><span class="sxs-lookup"><span data-stu-id="579ca-120">IMsRdpClientAdvancedSettings::RedirectPorts property</span></span>

<span data-ttu-id="579ca-121">Specifica se è consentito il reindirizzamento delle porte locali (ad esempio, COM e LPT).</span><span class="sxs-lookup"><span data-stu-id="579ca-121">Specifies if redirection of local ports (for example, COM and LPT) is allowed.</span></span>

<span data-ttu-id="579ca-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="579ca-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="579ca-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="579ca-123">Syntax</span></span>


```C++
HRESULT put_RedirectPorts(
  [in]  VARIANT_BOOL redirectPorts
);

HRESULT get_RedirectPorts(
  [out] VARIANT_BOOL *predirectPorts
);
```



## <a name="property-value"></a><span data-ttu-id="579ca-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="579ca-124">Property value</span></span>

<span data-ttu-id="579ca-125">Impostare questo parametro su **Variant \_ true** per consentire il reindirizzamento o la **variante \_ false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="579ca-125">Set this parameter to **VARIANT\_TRUE** to allow redirection or **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="579ca-126">**Variante \_ TRUE** chiede all'utente di confermare la concessione del reindirizzamento al momento della connessione, per motivi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="579ca-126">**VARIANT\_TRUE** prompts the user to confirm allowing redirection at connection time, for security purposes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="579ca-127">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="579ca-127">Error codes</span></span>

<span data-ttu-id="579ca-128">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="579ca-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="579ca-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="579ca-129">Remarks</span></span>

<span data-ttu-id="579ca-130">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="579ca-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="579ca-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="579ca-131">Requirements</span></span>



| <span data-ttu-id="579ca-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="579ca-132">Requirement</span></span> | <span data-ttu-id="579ca-133">Valore</span><span class="sxs-lookup"><span data-stu-id="579ca-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="579ca-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="579ca-134">Minimum supported client</span></span><br/> | <span data-ttu-id="579ca-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="579ca-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="579ca-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="579ca-136">Minimum supported server</span></span><br/> | <span data-ttu-id="579ca-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="579ca-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="579ca-138">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="579ca-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="579ca-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="579ca-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="579ca-140">DLL</span><span class="sxs-lookup"><span data-stu-id="579ca-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="579ca-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="579ca-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="579ca-142">IID</span><span class="sxs-lookup"><span data-stu-id="579ca-142">IID</span></span><br/>                      | <span data-ttu-id="579ca-143">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="579ca-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="579ca-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="579ca-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="579ca-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="579ca-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="579ca-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="579ca-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="579ca-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="579ca-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="579ca-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="579ca-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="579ca-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="579ca-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="579ca-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="579ca-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="579ca-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="579ca-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="579ca-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="579ca-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





