---
title: Proprietà DisableRdpdr di IMsTscAdvancedSettings
description: Specifica se il reindirizzamento della stampante e degli Appunti è abilitato.
ms.assetid: 63e0e024-4792-4efe-a6c5-d122f8adcb0a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà DisableRdpdr
- Servizi Desktop remoto proprietà DisableRdpdr, interfaccia IMsTscAdvancedSettings
- Interfaccia IMsTscAdvancedSettings Servizi Desktop remoto, proprietà DisableRdpdr
- Servizi Desktop remoto proprietà DisableRdpdr, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà DisableRdpdr
- Servizi Desktop remoto proprietà DisableRdpdr, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà DisableRdpdr
- Servizi Desktop remoto proprietà DisableRdpdr, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà DisableRdpdr
- Servizi Desktop remoto proprietà DisableRdpdr, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà DisableRdpdr
- Servizi Desktop remoto proprietà DisableRdpdr, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà DisableRdpdr
- Servizi Desktop remoto proprietà DisableRdpdr, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà DisableRdpdr
- Servizi Desktop remoto proprietà DisableRdpdr, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà DisableRdpdr
- Servizi Desktop remoto proprietà DisableRdpdr, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà DisableRdpdr
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.DisableRdpdr
- IMsTscAdvancedSettings.get_DisableRdpdr
- IMsTscAdvancedSettings.put_DisableRdpdr
- IMsRdpClientAdvancedSettings.DisableRdpdr
- IMsRdpClientAdvancedSettings.get_DisableRdpdr
- IMsRdpClientAdvancedSettings.put_DisableRdpdr
- IMsRdpClientAdvancedSettings2.DisableRdpdr
- IMsRdpClientAdvancedSettings2.get_DisableRdpdr
- IMsRdpClientAdvancedSettings2.put_DisableRdpdr
- IMsRdpClientAdvancedSettings3.DisableRdpdr
- IMsRdpClientAdvancedSettings3.get_DisableRdpdr
- IMsRdpClientAdvancedSettings3.put_DisableRdpdr
- IMsRdpClientAdvancedSettings4.DisableRdpdr
- IMsRdpClientAdvancedSettings4.get_DisableRdpdr
- IMsRdpClientAdvancedSettings4.put_DisableRdpdr
- IMsRdpClientAdvancedSettings5.DisableRdpdr
- IMsRdpClientAdvancedSettings5.get_DisableRdpdr
- IMsRdpClientAdvancedSettings5.put_DisableRdpdr
- IMsRdpClientAdvancedSettings6.DisableRdpdr
- IMsRdpClientAdvancedSettings6.get_DisableRdpdr
- IMsRdpClientAdvancedSettings6.put_DisableRdpdr
- IMsRdpClientAdvancedSettings7.DisableRdpdr
- IMsRdpClientAdvancedSettings7.get_DisableRdpdr
- IMsRdpClientAdvancedSettings7.put_DisableRdpdr
- IMsRdpClientAdvancedSettings8.DisableRdpdr
- IMsRdpClientAdvancedSettings8.get_DisableRdpdr
- IMsRdpClientAdvancedSettings8.put_DisableRdpdr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0747f37cd5e85c62946c9b8e3a1587f736dd8af9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301884"
---
# <a name="imstscadvancedsettingsdisablerdpdr-property"></a><span data-ttu-id="92a79-122">IMsTscAdvancedSettings::D Proprietà isableRdpdr</span><span class="sxs-lookup"><span data-stu-id="92a79-122">IMsTscAdvancedSettings::DisableRdpdr property</span></span>

<span data-ttu-id="92a79-123">Specifica se il reindirizzamento della stampante e degli Appunti è abilitato.</span><span class="sxs-lookup"><span data-stu-id="92a79-123">Specifies whether printer and clipboard redirection is enabled.</span></span>

<span data-ttu-id="92a79-124">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="92a79-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="92a79-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="92a79-125">Syntax</span></span>


```C++
HRESULT put_DisableRdpdr(
  [in]  BOOL DisableRdpdr
);

HRESULT get_DisableRdpdr(
  [out] BOOL *pDisableRdpdr
);
```



## <a name="property-value"></a><span data-ttu-id="92a79-126">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="92a79-126">Property value</span></span>

<span data-ttu-id="92a79-127">Impostare questo parametro su **true** per disabilitare il reindirizzamento o **false** per abilitare il reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="92a79-127">Set this parameter to **TRUE** to disable redirection or **FALSE** to enable redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="92a79-128">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="92a79-128">Error codes</span></span>

<span data-ttu-id="92a79-129">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="92a79-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="92a79-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="92a79-130">Remarks</span></span>

<span data-ttu-id="92a79-131">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="92a79-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="92a79-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92a79-132">Requirements</span></span>



| <span data-ttu-id="92a79-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="92a79-133">Requirement</span></span> | <span data-ttu-id="92a79-134">Valore</span><span class="sxs-lookup"><span data-stu-id="92a79-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="92a79-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92a79-135">Minimum supported client</span></span><br/> | <span data-ttu-id="92a79-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92a79-136">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="92a79-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92a79-137">Minimum supported server</span></span><br/> | <span data-ttu-id="92a79-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92a79-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="92a79-139">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="92a79-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="92a79-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92a79-140"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="92a79-141">DLL</span><span class="sxs-lookup"><span data-stu-id="92a79-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92a79-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92a79-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="92a79-143">IID</span><span class="sxs-lookup"><span data-stu-id="92a79-143">IID</span></span><br/>                      | <span data-ttu-id="92a79-144">IID \_ IMsTscAdvancedSettings è definito come 809945cc-4b3b-4A92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="92a79-144">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="92a79-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92a79-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92a79-146">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="92a79-146">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="92a79-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="92a79-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="92a79-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="92a79-148">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="92a79-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="92a79-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="92a79-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="92a79-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="92a79-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="92a79-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="92a79-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="92a79-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="92a79-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="92a79-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="92a79-154">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="92a79-154">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





