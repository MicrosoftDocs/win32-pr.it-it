---
title: Proprietà AdvancedSettings di IMsTscAx
description: Recupera un puntatore all'interfaccia IMsTscAdvancedSettings.
ms.assetid: 1c0e2216-0c65-48ad-b0f6-3a766c8fa44e
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà AdvancedSettings
- Servizi Desktop remoto proprietà AdvancedSettings, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, proprietà AdvancedSettings
- Servizi Desktop remoto proprietà AdvancedSettings, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà AdvancedSettings
- Servizi Desktop remoto proprietà AdvancedSettings, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà AdvancedSettings
- Servizi Desktop remoto proprietà AdvancedSettings, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà AdvancedSettings
- Servizi Desktop remoto proprietà AdvancedSettings, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà AdvancedSettings
- Servizi Desktop remoto proprietà AdvancedSettings, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà AdvancedSettings
- Servizi Desktop remoto proprietà AdvancedSettings, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà AdvancedSettings
- Servizi Desktop remoto proprietà AdvancedSettings, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà AdvancedSettings
- Servizi Desktop remoto proprietà AdvancedSettings, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà AdvancedSettings
- Servizi Desktop remoto proprietà AdvancedSettings, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà AdvancedSettings
topic_type:
- apiref
api_name:
- IMsTscAx.AdvancedSettings
- IMsTscAx.get_AdvancedSettings
- IMsRdpClient.AdvancedSettings
- IMsRdpClient.get_AdvancedSettings
- IMsRdpClient2.AdvancedSettings
- IMsRdpClient2.get_AdvancedSettings
- IMsRdpClient3.AdvancedSettings
- IMsRdpClient3.get_AdvancedSettings
- IMsRdpClient4.AdvancedSettings
- IMsRdpClient4.get_AdvancedSettings
- IMsRdpClient5.AdvancedSettings
- IMsRdpClient5.get_AdvancedSettings
- IMsRdpClient6.AdvancedSettings
- IMsRdpClient6.get_AdvancedSettings
- IMsRdpClient7.AdvancedSettings
- IMsRdpClient7.get_AdvancedSettings
- IMsRdpClient8.AdvancedSettings
- IMsRdpClient8.get_AdvancedSettings
- IMsRdpClient9.AdvancedSettings
- IMsRdpClient9.get_AdvancedSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98bb6b1d581704a0638a47310004777f020ce9bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964212"
---
# <a name="imstscaxadvancedsettings-property"></a><span data-ttu-id="01efd-124">Proprietà IMsTscAx:: AdvancedSettings</span><span class="sxs-lookup"><span data-stu-id="01efd-124">IMsTscAx::AdvancedSettings property</span></span>

<span data-ttu-id="01efd-125">Recupera un puntatore all'interfaccia [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="01efd-125">Retrieves an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span>

<span data-ttu-id="01efd-126">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="01efd-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="01efd-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01efd-127">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings(
  [out] IMsTscAdvancedSettings **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="01efd-128">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="01efd-128">Property value</span></span>

<span data-ttu-id="01efd-129">Puntatore di interfaccia [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="01efd-129">An [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="01efd-130">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="01efd-130">Error codes</span></span>

<span data-ttu-id="01efd-131">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="01efd-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="01efd-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="01efd-132">Remarks</span></span>

<span data-ttu-id="01efd-133">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="01efd-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="01efd-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01efd-134">Requirements</span></span>



| <span data-ttu-id="01efd-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="01efd-135">Requirement</span></span> | <span data-ttu-id="01efd-136">Valore</span><span class="sxs-lookup"><span data-stu-id="01efd-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="01efd-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01efd-137">Minimum supported client</span></span><br/> | <span data-ttu-id="01efd-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01efd-138">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="01efd-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01efd-139">Minimum supported server</span></span><br/> | <span data-ttu-id="01efd-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01efd-140">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="01efd-141">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="01efd-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="01efd-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01efd-142"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="01efd-143">DLL</span><span class="sxs-lookup"><span data-stu-id="01efd-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01efd-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01efd-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="01efd-145">IID</span><span class="sxs-lookup"><span data-stu-id="01efd-145">IID</span></span><br/>                      | <span data-ttu-id="01efd-146">IID \_ IMsTscAx è definito come 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="01efd-146">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="01efd-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01efd-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01efd-148">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="01efd-148">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="01efd-149">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="01efd-149">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="01efd-150">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="01efd-150">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="01efd-151">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="01efd-151">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="01efd-152">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="01efd-152">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="01efd-153">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="01efd-153">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="01efd-154">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="01efd-154">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="01efd-155">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="01efd-155">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="01efd-156">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="01efd-156">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="01efd-157">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="01efd-157">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





