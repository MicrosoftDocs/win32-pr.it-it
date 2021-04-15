---
title: Proprietà ClearTextPassword di IMsRdpClientAdvancedSettings
description: Specifica la password con cui connettersi. Per ulteriori informazioni, vedere l'interfaccia IMsTscNonScriptable.
ms.assetid: 9bb12dd6-f74c-488d-b6e5-4f96346610a1
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà ClearTextPassword
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.ClearTextPassword
- IMsRdpClientAdvancedSettings.put_ClearTextPassword
- IMsRdpClientAdvancedSettings2.ClearTextPassword
- IMsRdpClientAdvancedSettings2.put_ClearTextPassword
- IMsRdpClientAdvancedSettings3.ClearTextPassword
- IMsRdpClientAdvancedSettings3.put_ClearTextPassword
- IMsRdpClientAdvancedSettings4.ClearTextPassword
- IMsRdpClientAdvancedSettings4.put_ClearTextPassword
- IMsRdpClientAdvancedSettings5.ClearTextPassword
- IMsRdpClientAdvancedSettings5.put_ClearTextPassword
- IMsRdpClientAdvancedSettings6.ClearTextPassword
- IMsRdpClientAdvancedSettings6.put_ClearTextPassword
- IMsRdpClientAdvancedSettings7.ClearTextPassword
- IMsRdpClientAdvancedSettings7.put_ClearTextPassword
- IMsRdpClientAdvancedSettings8.ClearTextPassword
- IMsRdpClientAdvancedSettings8.put_ClearTextPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6943913193b2ecc9ed6ab31728d0274fb9ddd231
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476462"
---
# <a name="imsrdpclientadvancedsettingscleartextpassword-property"></a><span data-ttu-id="30386-121">Proprietà IMsRdpClientAdvancedSettings:: ClearTextPassword</span><span class="sxs-lookup"><span data-stu-id="30386-121">IMsRdpClientAdvancedSettings::ClearTextPassword property</span></span>

<span data-ttu-id="30386-122">Specifica la password con cui connettersi.</span><span class="sxs-lookup"><span data-stu-id="30386-122">Specifies the password with which to connect.</span></span> <span data-ttu-id="30386-123">Per ulteriori informazioni, vedere l'interfaccia [**IMsTscNonScriptable**](imstscnonscriptable-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="30386-123">For more information, see the [**IMsTscNonScriptable**](imstscnonscriptable-interface.md) interface.</span></span>

> [!Caution]  
> <span data-ttu-id="30386-124">Anche se l'accesso tramite script a password in testo non crittografato è disponibile tramite questa proprietà, è comunque compito dello sviluppatore esercitare ogni attenzione e mantenere la sicurezza quando si passano le password nelle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="30386-124">Even though scriptable access to plaintext passwords is available through this property, it is still the responsibility of the developer to exercise every caution and maintain security when passing passwords in their applications.</span></span>

 

<span data-ttu-id="30386-125">Questa proprietà è di sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="30386-125">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="30386-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30386-126">Syntax</span></span>


```C++
HRESULT put_ClearTextPassword(
  [in] BSTR clearTextPassword
);
```



## <a name="property-value"></a><span data-ttu-id="30386-127">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="30386-127">Property value</span></span>

<span data-ttu-id="30386-128">Nuova password.</span><span class="sxs-lookup"><span data-stu-id="30386-128">The new password.</span></span>

## <a name="error-codes"></a><span data-ttu-id="30386-129">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="30386-129">Error codes</span></span>

<span data-ttu-id="30386-130">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="30386-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="30386-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="30386-131">Remarks</span></span>

<span data-ttu-id="30386-132">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="30386-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30386-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30386-133">Requirements</span></span>



| <span data-ttu-id="30386-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="30386-134">Requirement</span></span> | <span data-ttu-id="30386-135">Valore</span><span class="sxs-lookup"><span data-stu-id="30386-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30386-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30386-136">Minimum supported client</span></span><br/> | <span data-ttu-id="30386-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30386-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="30386-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30386-138">Minimum supported server</span></span><br/> | <span data-ttu-id="30386-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30386-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="30386-140">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="30386-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="30386-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30386-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="30386-142">DLL</span><span class="sxs-lookup"><span data-stu-id="30386-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30386-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30386-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="30386-144">IID</span><span class="sxs-lookup"><span data-stu-id="30386-144">IID</span></span><br/>                      | <span data-ttu-id="30386-145">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="30386-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="30386-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30386-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30386-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="30386-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="30386-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="30386-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="30386-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="30386-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="30386-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="30386-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="30386-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="30386-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="30386-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="30386-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="30386-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="30386-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="30386-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="30386-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





