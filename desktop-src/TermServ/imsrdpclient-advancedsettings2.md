---
title: Proprietà AdvancedSettings2 di IMsRdpClient
description: Recupera un puntatore all'interfaccia IMsRdpClientAdvancedSettings. L'interfaccia può essere utilizzata per impostare impostazioni avanzate per il controllo client.
ms.assetid: 207b625c-fc2b-41ad-9339-9f3c3b8eeab7
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà AdvancedSettings2
- Servizi Desktop remoto proprietà AdvancedSettings2, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà AdvancedSettings2
- Servizi Desktop remoto proprietà AdvancedSettings2, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà AdvancedSettings2
- Servizi Desktop remoto proprietà AdvancedSettings2, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà AdvancedSettings2
- Servizi Desktop remoto proprietà AdvancedSettings2, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà AdvancedSettings2
- Servizi Desktop remoto proprietà AdvancedSettings2, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà AdvancedSettings2
- Servizi Desktop remoto proprietà AdvancedSettings2, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà AdvancedSettings2
- Servizi Desktop remoto proprietà AdvancedSettings2, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà AdvancedSettings2
- Servizi Desktop remoto proprietà AdvancedSettings2, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà AdvancedSettings2
- Servizi Desktop remoto proprietà AdvancedSettings2, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà AdvancedSettings2
- Servizi Desktop remoto proprietà AdvancedSettings2, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, proprietà AdvancedSettings2
topic_type:
- apiref
api_name:
- IMsRdpClient.AdvancedSettings2
- IMsRdpClient.get_AdvancedSettings2
- IMsRdpClient2.AdvancedSettings2
- IMsRdpClient2.get_AdvancedSettings2
- IMsRdpClient3.AdvancedSettings2
- IMsRdpClient3.get_AdvancedSettings2
- IMsRdpClient4.AdvancedSettings2
- IMsRdpClient4.get_AdvancedSettings2
- IMsRdpClient5.AdvancedSettings2
- IMsRdpClient5.get_AdvancedSettings2
- IMsRdpClient6.AdvancedSettings2
- IMsRdpClient6.get_AdvancedSettings2
- IMsRdpClient7.AdvancedSettings2
- IMsRdpClient7.get_AdvancedSettings2
- IMsRdpClient8.AdvancedSettings2
- IMsRdpClient8.get_AdvancedSettings2
- IMsRdpClient9.AdvancedSettings2
- IMsRdpClient9.get_AdvancedSettings2
- IMsRdpClient10.AdvancedSettings2
- IMsRdpClient10.get_AdvancedSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683d56d5e9501114b1e60635ca406b4509d2032b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302470"
---
# <a name="imsrdpclientadvancedsettings2-property"></a><span data-ttu-id="78fe1-125">Proprietà IMsRdpClient:: AdvancedSettings2</span><span class="sxs-lookup"><span data-stu-id="78fe1-125">IMsRdpClient::AdvancedSettings2 property</span></span>

<span data-ttu-id="78fe1-126">Recupera un puntatore all'interfaccia [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="78fe1-126">Retrieves a pointer to the [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) interface.</span></span> <span data-ttu-id="78fe1-127">L'interfaccia può essere utilizzata per impostare impostazioni avanzate per il controllo client.</span><span class="sxs-lookup"><span data-stu-id="78fe1-127">The interface can be used to set advanced settings for the client control.</span></span>

<span data-ttu-id="78fe1-128">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="78fe1-128">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="78fe1-129">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78fe1-129">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings2(
  [out] IMsRdpClientAdvancedSettings **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="78fe1-130">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="78fe1-130">Property value</span></span>

<span data-ttu-id="78fe1-131">Puntatore all'interfaccia [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="78fe1-131">Pointer to the [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) interface.</span></span> <span data-ttu-id="78fe1-132">L'interfaccia può essere utilizzata per impostare impostazioni avanzate per il controllo client.</span><span class="sxs-lookup"><span data-stu-id="78fe1-132">The interface can be used to set advanced settings for the client control.</span></span>

## <a name="error-codes"></a><span data-ttu-id="78fe1-133">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="78fe1-133">Error codes</span></span>

<span data-ttu-id="78fe1-134">Se il metodo ha esito positivo, viene restituito **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="78fe1-134">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="78fe1-135">Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="78fe1-135">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="78fe1-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="78fe1-136">Remarks</span></span>

<span data-ttu-id="78fe1-137">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="78fe1-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="78fe1-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78fe1-138">Requirements</span></span>



| <span data-ttu-id="78fe1-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="78fe1-139">Requirement</span></span> | <span data-ttu-id="78fe1-140">Valore</span><span class="sxs-lookup"><span data-stu-id="78fe1-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78fe1-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78fe1-141">Minimum supported client</span></span><br/> | <span data-ttu-id="78fe1-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78fe1-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="78fe1-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78fe1-143">Minimum supported server</span></span><br/> | <span data-ttu-id="78fe1-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78fe1-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="78fe1-145">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="78fe1-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="78fe1-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78fe1-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="78fe1-147">DLL</span><span class="sxs-lookup"><span data-stu-id="78fe1-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78fe1-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78fe1-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="78fe1-149">IID</span><span class="sxs-lookup"><span data-stu-id="78fe1-149">IID</span></span><br/>                      | <span data-ttu-id="78fe1-150">IID \_ IMsRdpClient è definito come 92b4a539-7115-4B7C-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="78fe1-150">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="78fe1-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78fe1-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78fe1-152">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="78fe1-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="78fe1-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="78fe1-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="78fe1-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="78fe1-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="78fe1-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="78fe1-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="78fe1-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="78fe1-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="78fe1-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="78fe1-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="78fe1-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="78fe1-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="78fe1-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="78fe1-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="78fe1-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="78fe1-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="78fe1-161">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="78fe1-161">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





