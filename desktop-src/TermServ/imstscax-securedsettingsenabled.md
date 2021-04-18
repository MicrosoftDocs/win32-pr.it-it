---
title: Proprietà SecuredSettingsEnabled di IMsTscAx
description: Indica se l'interfaccia IMsTscSecuredSettings è disponibile. Ovvero se la pagina Web contenente il controllo si trova attualmente in una delle aree di sicurezza URL Internet Explorer consentite.
ms.assetid: 0747eab0-9d62-4c10-b02d-fc65ca2f752e
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà SecuredSettingsEnabled
- Servizi Desktop remoto proprietà SecuredSettingsEnabled, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, proprietà SecuredSettingsEnabled
- Servizi Desktop remoto proprietà SecuredSettingsEnabled, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà SecuredSettingsEnabled
- Servizi Desktop remoto proprietà SecuredSettingsEnabled, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà SecuredSettingsEnabled
- Servizi Desktop remoto proprietà SecuredSettingsEnabled, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà SecuredSettingsEnabled
- Servizi Desktop remoto proprietà SecuredSettingsEnabled, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà SecuredSettingsEnabled
- Servizi Desktop remoto proprietà SecuredSettingsEnabled, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà SecuredSettingsEnabled
- Servizi Desktop remoto proprietà SecuredSettingsEnabled, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà SecuredSettingsEnabled
- Servizi Desktop remoto proprietà SecuredSettingsEnabled, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà SecuredSettingsEnabled
- Servizi Desktop remoto proprietà SecuredSettingsEnabled, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà SecuredSettingsEnabled
- Servizi Desktop remoto proprietà SecuredSettingsEnabled, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà SecuredSettingsEnabled
topic_type:
- apiref
api_name:
- IMsTscAx.SecuredSettingsEnabled
- IMsTscAx.get_SecuredSettingsEnabled
- IMsRdpClient.SecuredSettingsEnabled
- IMsRdpClient.get_SecuredSettingsEnabled
- IMsRdpClient2.SecuredSettingsEnabled
- IMsRdpClient2.get_SecuredSettingsEnabled
- IMsRdpClient3.SecuredSettingsEnabled
- IMsRdpClient3.get_SecuredSettingsEnabled
- IMsRdpClient4.SecuredSettingsEnabled
- IMsRdpClient4.get_SecuredSettingsEnabled
- IMsRdpClient5.SecuredSettingsEnabled
- IMsRdpClient5.get_SecuredSettingsEnabled
- IMsRdpClient6.SecuredSettingsEnabled
- IMsRdpClient6.get_SecuredSettingsEnabled
- IMsRdpClient7.SecuredSettingsEnabled
- IMsRdpClient7.get_SecuredSettingsEnabled
- IMsRdpClient8.SecuredSettingsEnabled
- IMsRdpClient8.get_SecuredSettingsEnabled
- IMsRdpClient9.SecuredSettingsEnabled
- IMsRdpClient9.get_SecuredSettingsEnabled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0601ac64ab0ca55f3d92ec460861a4347f70b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302460"
---
# <a name="imstscaxsecuredsettingsenabled-property"></a><span data-ttu-id="35f82-125">Proprietà IMsTscAx:: SecuredSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="35f82-125">IMsTscAx::SecuredSettingsEnabled property</span></span>

<span data-ttu-id="35f82-126">Indica se l'interfaccia [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) è disponibile.</span><span class="sxs-lookup"><span data-stu-id="35f82-126">Indicates whether the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface is available.</span></span> <span data-ttu-id="35f82-127">Ovvero se la pagina Web contenente il controllo si trova attualmente in una delle aree di sicurezza URL Internet Explorer consentite.</span><span class="sxs-lookup"><span data-stu-id="35f82-127">That is, whether the webpage containing the control is currently in one of the allowed Internet Explorer URL security zones.</span></span>

<span data-ttu-id="35f82-128">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="35f82-128">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="35f82-129">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35f82-129">Syntax</span></span>


```C++
HRESULT get_SecuredSettingsEnabled(
  [out] BOOL *pSecuredSettingsEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="35f82-130">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="35f82-130">Property value</span></span>

<span data-ttu-id="35f82-131">Il valore di questo parametro è **true** se l'interfaccia è disponibile e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="35f82-131">The value of this parameter is **TRUE** if the interface is available, and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="35f82-132">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="35f82-132">Error codes</span></span>

<span data-ttu-id="35f82-133">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="35f82-133">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="35f82-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="35f82-134">Remarks</span></span>

<span data-ttu-id="35f82-135">Utilizzare questo metodo per eseguire una query per verificare se l'interfaccia [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) è disponibile prima di recuperare la proprietà [**SecuredSettings**](imstscax-securedsettings.md) .</span><span class="sxs-lookup"><span data-stu-id="35f82-135">Use this method to query whether the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface is available before retrieving the [**SecuredSettings**](imstscax-securedsettings.md) property.</span></span>

<span data-ttu-id="35f82-136">Per un elenco di aree di sicurezza con URL limitati, vedere la pagina [relativa a come fornire la sicurezza del client RDP](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="35f82-136">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for a list of restricted URL security zones.</span></span>

<span data-ttu-id="35f82-137">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="35f82-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35f82-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35f82-138">Requirements</span></span>



| <span data-ttu-id="35f82-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="35f82-139">Requirement</span></span> | <span data-ttu-id="35f82-140">Valore</span><span class="sxs-lookup"><span data-stu-id="35f82-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35f82-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35f82-141">Minimum supported client</span></span><br/> | <span data-ttu-id="35f82-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35f82-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="35f82-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35f82-143">Minimum supported server</span></span><br/> | <span data-ttu-id="35f82-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35f82-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="35f82-145">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="35f82-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="35f82-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35f82-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="35f82-147">DLL</span><span class="sxs-lookup"><span data-stu-id="35f82-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35f82-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35f82-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="35f82-149">IID</span><span class="sxs-lookup"><span data-stu-id="35f82-149">IID</span></span><br/>                      | <span data-ttu-id="35f82-150">IID \_ IMsTscAx è definito come 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="35f82-150">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="35f82-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35f82-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35f82-152">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="35f82-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="35f82-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="35f82-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="35f82-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="35f82-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="35f82-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="35f82-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="35f82-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="35f82-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="35f82-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="35f82-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="35f82-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="35f82-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="35f82-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="35f82-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="35f82-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="35f82-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="35f82-161">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="35f82-161">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="35f82-162">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="35f82-162">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





