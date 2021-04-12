---
title: Proprietà SecuredSettings di IMsTscAx
description: Recupera un puntatore all'interfaccia IMsTscSecuredSettings.
ms.assetid: 64d4059b-e617-449d-a733-c19c1d281132
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà SecuredSettings
- Servizi Desktop remoto proprietà SecuredSettings, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, proprietà SecuredSettings
- Servizi Desktop remoto proprietà SecuredSettings, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà SecuredSettings
- Servizi Desktop remoto proprietà SecuredSettings, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà SecuredSettings
- Servizi Desktop remoto proprietà SecuredSettings, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà SecuredSettings
- Servizi Desktop remoto proprietà SecuredSettings, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà SecuredSettings
- Servizi Desktop remoto proprietà SecuredSettings, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà SecuredSettings
- Servizi Desktop remoto proprietà SecuredSettings, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà SecuredSettings
- Servizi Desktop remoto proprietà SecuredSettings, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà SecuredSettings
- Servizi Desktop remoto proprietà SecuredSettings, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà SecuredSettings
- Servizi Desktop remoto proprietà SecuredSettings, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà SecuredSettings
topic_type:
- apiref
api_name:
- IMsTscAx.SecuredSettings
- IMsTscAx.get_SecuredSettings
- IMsRdpClient.SecuredSettings
- IMsRdpClient.get_SecuredSettings
- IMsRdpClient2.SecuredSettings
- IMsRdpClient2.get_SecuredSettings
- IMsRdpClient3.SecuredSettings
- IMsRdpClient3.get_SecuredSettings
- IMsRdpClient4.SecuredSettings
- IMsRdpClient4.get_SecuredSettings
- IMsRdpClient5.SecuredSettings
- IMsRdpClient5.get_SecuredSettings
- IMsRdpClient6.SecuredSettings
- IMsRdpClient6.get_SecuredSettings
- IMsRdpClient7.SecuredSettings
- IMsRdpClient7.get_SecuredSettings
- IMsRdpClient8.SecuredSettings
- IMsRdpClient8.get_SecuredSettings
- IMsRdpClient9.SecuredSettings
- IMsRdpClient9.get_SecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6610448d822fe75082c225686dc6d809229a325f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119774"
---
# <a name="imstscaxsecuredsettings-property"></a><span data-ttu-id="efb63-124">Proprietà IMsTscAx:: SecuredSettings</span><span class="sxs-lookup"><span data-stu-id="efb63-124">IMsTscAx::SecuredSettings property</span></span>

<span data-ttu-id="efb63-125">Recupera un puntatore all'interfaccia [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="efb63-125">Retrieves an [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface pointer.</span></span>

<span data-ttu-id="efb63-126">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="efb63-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="efb63-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="efb63-127">Syntax</span></span>


```C++
HRESULT get_SecuredSettings(
  [out] IMsTscSecuredSettings **ppSecuredSettings
);
```



## <a name="property-value"></a><span data-ttu-id="efb63-128">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="efb63-128">Property value</span></span>

<span data-ttu-id="efb63-129">Puntatore di interfaccia [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="efb63-129">An [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="efb63-130">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="efb63-130">Error codes</span></span>

<span data-ttu-id="efb63-131">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="efb63-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="efb63-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="efb63-132">Remarks</span></span>

<span data-ttu-id="efb63-133">Se il controllo è ospitato in una pagina Web e l'area di sicurezza dell'URL di Internet Explorer corrente non consente il recupero dell'indirizzo di interfaccia, questo metodo restituisce **E ha \_ esito negativo**.</span><span class="sxs-lookup"><span data-stu-id="efb63-133">If the control is hosted in a webpage and the current Internet Explorer URL security zone does not permit the retrieval of the interface address, this method returns **E\_FAIL**.</span></span>

<span data-ttu-id="efb63-134">Per le restrizioni sulla disponibilità dell'interfaccia [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) , vedere [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) .</span><span class="sxs-lookup"><span data-stu-id="efb63-134">Refer to [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) for restrictions on the availability of the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface.</span></span>

<span data-ttu-id="efb63-135">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="efb63-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="efb63-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="efb63-136">Requirements</span></span>



| <span data-ttu-id="efb63-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="efb63-137">Requirement</span></span> | <span data-ttu-id="efb63-138">Valore</span><span class="sxs-lookup"><span data-stu-id="efb63-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="efb63-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efb63-139">Minimum supported client</span></span><br/> | <span data-ttu-id="efb63-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="efb63-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="efb63-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efb63-141">Minimum supported server</span></span><br/> | <span data-ttu-id="efb63-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="efb63-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="efb63-143">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="efb63-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="efb63-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efb63-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="efb63-145">DLL</span><span class="sxs-lookup"><span data-stu-id="efb63-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efb63-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efb63-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="efb63-147">IID</span><span class="sxs-lookup"><span data-stu-id="efb63-147">IID</span></span><br/>                      | <span data-ttu-id="efb63-148">IID \_ IMsTscAx è definito come 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="efb63-148">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="efb63-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="efb63-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efb63-150">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="efb63-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="efb63-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="efb63-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="efb63-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="efb63-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="efb63-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="efb63-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="efb63-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="efb63-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="efb63-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="efb63-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="efb63-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="efb63-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="efb63-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="efb63-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="efb63-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="efb63-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="efb63-159">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="efb63-159">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="efb63-160">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="efb63-160">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





