---
title: Proprietà PluginDlls di IMsTscAdvancedSettings
description: Specifica i nomi delle dll client del canale virtuale da caricare.
ms.assetid: 4b248fb8-200a-4ce0-8c8e-ce1692a80d88
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà PluginDlls
- Servizi Desktop remoto proprietà PluginDlls, interfaccia IMsTscAdvancedSettings
- Interfaccia IMsTscAdvancedSettings Servizi Desktop remoto, proprietà PluginDlls
- Servizi Desktop remoto proprietà PluginDlls, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà PluginDlls
- Servizi Desktop remoto proprietà PluginDlls, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà PluginDlls
- Servizi Desktop remoto proprietà PluginDlls, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà PluginDlls
- Servizi Desktop remoto proprietà PluginDlls, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà PluginDlls
- Servizi Desktop remoto proprietà PluginDlls, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà PluginDlls
- Servizi Desktop remoto proprietà PluginDlls, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà PluginDlls
- Servizi Desktop remoto proprietà PluginDlls, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà PluginDlls
- Servizi Desktop remoto proprietà PluginDlls, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà PluginDlls
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.PluginDlls
- IMsTscAdvancedSettings.put_PluginDlls
- IMsRdpClientAdvancedSettings.PluginDlls
- IMsRdpClientAdvancedSettings.put_PluginDlls
- IMsRdpClientAdvancedSettings2.PluginDlls
- IMsRdpClientAdvancedSettings2.put_PluginDlls
- IMsRdpClientAdvancedSettings3.PluginDlls
- IMsRdpClientAdvancedSettings3.put_PluginDlls
- IMsRdpClientAdvancedSettings4.PluginDlls
- IMsRdpClientAdvancedSettings4.put_PluginDlls
- IMsRdpClientAdvancedSettings5.PluginDlls
- IMsRdpClientAdvancedSettings5.put_PluginDlls
- IMsRdpClientAdvancedSettings6.PluginDlls
- IMsRdpClientAdvancedSettings6.put_PluginDlls
- IMsRdpClientAdvancedSettings7.PluginDlls
- IMsRdpClientAdvancedSettings7.put_PluginDlls
- IMsRdpClientAdvancedSettings8.PluginDlls
- IMsRdpClientAdvancedSettings8.put_PluginDlls
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3ef2e518145ae34533477bcbefb92e15d9c8d94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476744"
---
# <a name="imstscadvancedsettingsplugindlls-property"></a><span data-ttu-id="17736-122">IMsTscAdvancedSettings::P proprietà luginDlls</span><span class="sxs-lookup"><span data-stu-id="17736-122">IMsTscAdvancedSettings::PluginDlls property</span></span>

<span data-ttu-id="17736-123">Specifica i nomi delle dll client del canale virtuale da caricare.</span><span class="sxs-lookup"><span data-stu-id="17736-123">Specifies the names of virtual channel client DLLs to be loaded.</span></span> <span data-ttu-id="17736-124">Le dll client del canale virtuale sono anche denominate DLL plug-in.</span><span class="sxs-lookup"><span data-stu-id="17736-124">Virtual channel client DLLs are also referred to as Plug-in DLLs.</span></span>

<span data-ttu-id="17736-125">Questa proprietà è di sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="17736-125">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="17736-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17736-126">Syntax</span></span>


```C++
HRESULT put_PluginDlls(
  [in] BSTR PluginDlls
);
```



## <a name="property-value"></a><span data-ttu-id="17736-127">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="17736-127">Property value</span></span>

<span data-ttu-id="17736-128">Elenco delimitato da virgole dei nomi delle dll client del canale virtuale da caricare.</span><span class="sxs-lookup"><span data-stu-id="17736-128">Comma-separated list of the names of the virtual channel client DLLs to be loaded.</span></span> <span data-ttu-id="17736-129">I nomi delle DLL devono contenere solo caratteri alfanumerici.</span><span class="sxs-lookup"><span data-stu-id="17736-129">The DLL names must contain only alphanumeric characters.</span></span> <span data-ttu-id="17736-130">Per ulteriori informazioni sul formato di questi nomi, vedere [registrazione del plug-in DVC](dvc-plug-in-registration.md).</span><span class="sxs-lookup"><span data-stu-id="17736-130">For more information about the format of these names, see [DVC plug-in registration](dvc-plug-in-registration.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="17736-131">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="17736-131">Error codes</span></span>

<span data-ttu-id="17736-132">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="17736-132">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="17736-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="17736-133">Remarks</span></span>

<span data-ttu-id="17736-134">Per motivi di sicurezza, se il controllo è ospitato in una pagina Web, la proprietà **PluginDlls** accetta solo un elenco denominato di dll client di canale virtuale.</span><span class="sxs-lookup"><span data-stu-id="17736-134">For security reasons, if the control is hosted in a webpage the **PluginDlls** property only accepts a named list of virtual channel client DLLs.</span></span> <span data-ttu-id="17736-135">Il controllo restituisce un errore se viene specificato un file system o un percorso UNC.</span><span class="sxs-lookup"><span data-stu-id="17736-135">The control returns an error if a file system or UNC path is specified.</span></span>

<span data-ttu-id="17736-136">Le dll client del canale virtuale a cui si accede da una pagina Web devono essere installate nella directory "% WinDir% \\ system32" perché il controllo ActiveX Desktop remoto accede solo ai file dll in tale percorso.</span><span class="sxs-lookup"><span data-stu-id="17736-136">Virtual channel client DLLs that will be accessed from a webpage must be installed in the "%WinDir%\\system32" directory because the Remote Desktop ActiveX control only accesses DLL files in that location.</span></span> <span data-ttu-id="17736-137">Se il controllo non è ospitato in una pagina Web, questa restrizione di sicurezza non esiste e i percorsi completi possono essere usati per accedere e caricare le dll client dei canali virtuali presenti in qualsiasi punto del file system.</span><span class="sxs-lookup"><span data-stu-id="17736-137">If the control is not hosted in a webpage, this security restriction does not exist and full paths may be used to access and load virtual channel client DLLs located anywhere on the file system.</span></span>

<span data-ttu-id="17736-138">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="17736-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="17736-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17736-139">Requirements</span></span>



| <span data-ttu-id="17736-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="17736-140">Requirement</span></span> | <span data-ttu-id="17736-141">Valore</span><span class="sxs-lookup"><span data-stu-id="17736-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="17736-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17736-142">Minimum supported client</span></span><br/> | <span data-ttu-id="17736-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17736-143">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="17736-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17736-144">Minimum supported server</span></span><br/> | <span data-ttu-id="17736-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17736-145">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="17736-146">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="17736-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="17736-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17736-147"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="17736-148">DLL</span><span class="sxs-lookup"><span data-stu-id="17736-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17736-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17736-149"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="17736-150">IID</span><span class="sxs-lookup"><span data-stu-id="17736-150">IID</span></span><br/>                      | <span data-ttu-id="17736-151">IID \_ IMsTscAdvancedSettings è definito come 809945cc-4b3b-4A92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="17736-151">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="17736-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17736-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17736-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="17736-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="17736-154">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="17736-154">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="17736-155">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="17736-155">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="17736-156">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="17736-156">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="17736-157">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="17736-157">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="17736-158">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="17736-158">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="17736-159">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="17736-159">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="17736-160">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="17736-160">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="17736-161">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="17736-161">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





