---
title: Proprietà AdvancedSettings3 di IMsRdpClient2
description: Recupera un puntatore all'interfaccia IMsRdpClientAdvancedSettings2. L'interfaccia può essere utilizzata per impostare impostazioni avanzate per il controllo client.
ms.assetid: 69353bfa-973e-4c6a-8f7e-1b9514be2539
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà AdvancedSettings3
- Servizi Desktop remoto proprietà AdvancedSettings3, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà AdvancedSettings3
- Servizi Desktop remoto proprietà AdvancedSettings3, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà AdvancedSettings3
- Servizi Desktop remoto proprietà AdvancedSettings3, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà AdvancedSettings3
- Servizi Desktop remoto proprietà AdvancedSettings3, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà AdvancedSettings3
- Servizi Desktop remoto proprietà AdvancedSettings3, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà AdvancedSettings3
- Servizi Desktop remoto proprietà AdvancedSettings3, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà AdvancedSettings3
- Servizi Desktop remoto proprietà AdvancedSettings3, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà AdvancedSettings3
- Servizi Desktop remoto proprietà AdvancedSettings3, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà AdvancedSettings3
- Servizi Desktop remoto proprietà AdvancedSettings3, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, proprietà AdvancedSettings3
topic_type:
- apiref
api_name:
- IMsRdpClient2.AdvancedSettings3
- IMsRdpClient2.get_AdvancedSettings3
- IMsRdpClient3.AdvancedSettings3
- IMsRdpClient3.get_AdvancedSettings3
- IMsRdpClient4.AdvancedSettings3
- IMsRdpClient4.get_AdvancedSettings3
- IMsRdpClient5.AdvancedSettings3
- IMsRdpClient5.get_AdvancedSettings3
- IMsRdpClient6.AdvancedSettings3
- IMsRdpClient6.get_AdvancedSettings3
- IMsRdpClient7.AdvancedSettings3
- IMsRdpClient7.get_AdvancedSettings3
- IMsRdpClient8.AdvancedSettings3
- IMsRdpClient8.get_AdvancedSettings3
- IMsRdpClient9.AdvancedSettings3
- IMsRdpClient9.get_AdvancedSettings3
- IMsRdpClient10.AdvancedSettings3
- IMsRdpClient10.get_AdvancedSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf16d56eaff321d313e3a27eb6dd774ef67e13ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340813"
---
# <a name="imsrdpclient2advancedsettings3-property"></a><span data-ttu-id="f3a1c-123">Proprietà IMsRdpClient2:: AdvancedSettings3</span><span class="sxs-lookup"><span data-stu-id="f3a1c-123">IMsRdpClient2::AdvancedSettings3 property</span></span>

<span data-ttu-id="f3a1c-124">Recupera un puntatore all'interfaccia [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="f3a1c-124">Retrieves a pointer to the [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) interface.</span></span> <span data-ttu-id="f3a1c-125">L'interfaccia può essere utilizzata per impostare impostazioni avanzate per il controllo client.</span><span class="sxs-lookup"><span data-stu-id="f3a1c-125">The interface can be used to set advanced settings for the client control.</span></span>

<span data-ttu-id="f3a1c-126">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="f3a1c-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3a1c-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3a1c-127">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings3(
  [out] IMsRdpClientAdvancedSettings2 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="f3a1c-128">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f3a1c-128">Property value</span></span>

<span data-ttu-id="f3a1c-129">Recupera un puntatore all'interfaccia [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="f3a1c-129">Retrieves a pointer to the [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) interface.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f3a1c-130">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="f3a1c-130">Error codes</span></span>

<span data-ttu-id="f3a1c-131">Se il metodo ha esito positivo, viene restituito **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="f3a1c-131">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="f3a1c-132">Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="f3a1c-132">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3a1c-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3a1c-133">Remarks</span></span>

<span data-ttu-id="f3a1c-134">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f3a1c-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3a1c-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3a1c-135">Requirements</span></span>



| <span data-ttu-id="f3a1c-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3a1c-136">Requirement</span></span> | <span data-ttu-id="f3a1c-137">Valore</span><span class="sxs-lookup"><span data-stu-id="f3a1c-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3a1c-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3a1c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f3a1c-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f3a1c-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f3a1c-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3a1c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f3a1c-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3a1c-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f3a1c-142">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f3a1c-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="f3a1c-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3a1c-143"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f3a1c-144">DLL</span><span class="sxs-lookup"><span data-stu-id="f3a1c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3a1c-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3a1c-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f3a1c-146">IID</span><span class="sxs-lookup"><span data-stu-id="f3a1c-146">IID</span></span><br/>                      | <span data-ttu-id="f3a1c-147">IID \_ IMsRdpClient2 è definito come e7e17dc4-3b71-4ba7-A8E6-281ffadca28f</span><span class="sxs-lookup"><span data-stu-id="f3a1c-147">IID\_IMsRdpClient2 is defined as e7e17dc4-3b71-4ba7-a8e6-281ffadca28f</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f3a1c-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3a1c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3a1c-149">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="f3a1c-149">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="f3a1c-150">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="f3a1c-150">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="f3a1c-151">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="f3a1c-151">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="f3a1c-152">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="f3a1c-152">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="f3a1c-153">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="f3a1c-153">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="f3a1c-154">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="f3a1c-154">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="f3a1c-155">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="f3a1c-155">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="f3a1c-156">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="f3a1c-156">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="f3a1c-157">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="f3a1c-157">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





