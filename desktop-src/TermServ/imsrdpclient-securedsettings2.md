---
title: Proprietà SecuredSettings2 di IMsRdpClient
description: Recupera un puntatore all'interfaccia IMsRdpClientSecuredSettings. Questa interfaccia può essere utilizzata per impostare impostazioni protette per il controllo client.
ms.assetid: f570a3f6-70ae-45fd-ba20-75c9f4d2f5ca
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà SecuredSettings2
- Servizi Desktop remoto proprietà SecuredSettings2, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà SecuredSettings2
- Servizi Desktop remoto proprietà SecuredSettings2, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà SecuredSettings2
- Servizi Desktop remoto proprietà SecuredSettings2, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà SecuredSettings2
- Servizi Desktop remoto proprietà SecuredSettings2, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà SecuredSettings2
- Servizi Desktop remoto proprietà SecuredSettings2, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà SecuredSettings2
- Servizi Desktop remoto proprietà SecuredSettings2, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà SecuredSettings2
- Servizi Desktop remoto proprietà SecuredSettings2, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà SecuredSettings2
- Servizi Desktop remoto proprietà SecuredSettings2, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà SecuredSettings2
- Servizi Desktop remoto proprietà SecuredSettings2, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà SecuredSettings2
- Servizi Desktop remoto proprietà SecuredSettings2, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, proprietà SecuredSettings2
topic_type:
- apiref
api_name:
- IMsRdpClient.SecuredSettings2
- IMsRdpClient.get_SecuredSettings2
- IMsRdpClient2.SecuredSettings2
- IMsRdpClient2.get_SecuredSettings2
- IMsRdpClient3.SecuredSettings2
- IMsRdpClient3.get_SecuredSettings2
- IMsRdpClient4.SecuredSettings2
- IMsRdpClient4.get_SecuredSettings2
- IMsRdpClient5.SecuredSettings2
- IMsRdpClient5.get_SecuredSettings2
- IMsRdpClient6.SecuredSettings2
- IMsRdpClient6.get_SecuredSettings2
- IMsRdpClient7.SecuredSettings2
- IMsRdpClient7.get_SecuredSettings2
- IMsRdpClient8.SecuredSettings2
- IMsRdpClient8.get_SecuredSettings2
- IMsRdpClient9.SecuredSettings2
- IMsRdpClient9.get_SecuredSettings2
- IMsRdpClient10.SecuredSettings2
- IMsRdpClient10.get_SecuredSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39e26d9d7a7b2ac776166c251e5a2ab9923297f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517367"
---
# <a name="imsrdpclientsecuredsettings2-property"></a><span data-ttu-id="ab20e-125">Proprietà IMsRdpClient:: SecuredSettings2</span><span class="sxs-lookup"><span data-stu-id="ab20e-125">IMsRdpClient::SecuredSettings2 property</span></span>

<span data-ttu-id="ab20e-126">Recupera un puntatore all'interfaccia [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="ab20e-126">Retrieves a pointer to the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface.</span></span> <span data-ttu-id="ab20e-127">Questa interfaccia può essere utilizzata per impostare impostazioni protette per il controllo client.</span><span class="sxs-lookup"><span data-stu-id="ab20e-127">This interface can be used to set secured settings for the client control.</span></span>

<span data-ttu-id="ab20e-128">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="ab20e-128">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab20e-129">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab20e-129">Syntax</span></span>


```C++
HRESULT get_SecuredSettings2(
  [out] IMsRdpClientSecuredSettings **ppSecuredSettings
);
```



## <a name="property-value"></a><span data-ttu-id="ab20e-130">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ab20e-130">Property value</span></span>

<span data-ttu-id="ab20e-131">Puntatore di interfaccia [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="ab20e-131">An [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ab20e-132">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ab20e-132">Error codes</span></span>

<span data-ttu-id="ab20e-133">Se il metodo ha esito positivo, viene restituito **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="ab20e-133">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="ab20e-134">Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="ab20e-134">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab20e-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab20e-135">Remarks</span></span>

<span data-ttu-id="ab20e-136">Per ulteriori informazioni, vedere l'interfaccia [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) e [fornire la sicurezza del client RDP](providing-for-rdp-client-security.md).</span><span class="sxs-lookup"><span data-stu-id="ab20e-136">For more information, see the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface, and [Providing for RDP Client Security](providing-for-rdp-client-security.md).</span></span>

<span data-ttu-id="ab20e-137">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ab20e-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab20e-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab20e-138">Requirements</span></span>



| <span data-ttu-id="ab20e-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab20e-139">Requirement</span></span> | <span data-ttu-id="ab20e-140">Valore</span><span class="sxs-lookup"><span data-stu-id="ab20e-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab20e-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab20e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="ab20e-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ab20e-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ab20e-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab20e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="ab20e-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab20e-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ab20e-145">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ab20e-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="ab20e-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab20e-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ab20e-147">DLL</span><span class="sxs-lookup"><span data-stu-id="ab20e-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab20e-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab20e-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ab20e-149">IID</span><span class="sxs-lookup"><span data-stu-id="ab20e-149">IID</span></span><br/>                      | <span data-ttu-id="ab20e-150">IID \_ IMsRdpClient è definito come 92b4a539-7115-4B7C-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="ab20e-150">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="ab20e-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab20e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab20e-152">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="ab20e-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="ab20e-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="ab20e-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="ab20e-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="ab20e-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="ab20e-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="ab20e-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="ab20e-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="ab20e-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="ab20e-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="ab20e-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="ab20e-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="ab20e-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="ab20e-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="ab20e-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="ab20e-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="ab20e-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="ab20e-161">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="ab20e-161">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





