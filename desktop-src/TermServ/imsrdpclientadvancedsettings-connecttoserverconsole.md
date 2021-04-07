---
title: Proprietà ConnectToServerConsole di IMsRdpClientAdvancedSettings
description: Questa proprietà non è supportata. Le chiamate a ConnectToServerConsole restituiscono sempre S \_ false.
ms.assetid: 58f79085-4364-408f-8bf1-97a82ad68f4b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà ConnectToServerConsole
- Servizi Desktop remoto proprietà ConnectToServerConsole, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà ConnectToServerConsole
- Servizi Desktop remoto proprietà ConnectToServerConsole, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà ConnectToServerConsole
- Servizi Desktop remoto proprietà ConnectToServerConsole, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà ConnectToServerConsole
- Servizi Desktop remoto proprietà ConnectToServerConsole, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà ConnectToServerConsole
- Servizi Desktop remoto proprietà ConnectToServerConsole, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà ConnectToServerConsole
- Servizi Desktop remoto proprietà ConnectToServerConsole, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà ConnectToServerConsole
- Servizi Desktop remoto proprietà ConnectToServerConsole, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà ConnectToServerConsole
- Servizi Desktop remoto proprietà ConnectToServerConsole, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà ConnectToServerConsole
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.ConnectToServerConsole
- IMsRdpClientAdvancedSettings.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings2.ConnectToServerConsole
- IMsRdpClientAdvancedSettings2.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings2.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings3.ConnectToServerConsole
- IMsRdpClientAdvancedSettings3.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings3.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings4.ConnectToServerConsole
- IMsRdpClientAdvancedSettings4.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings4.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings5.ConnectToServerConsole
- IMsRdpClientAdvancedSettings5.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings5.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings6.ConnectToServerConsole
- IMsRdpClientAdvancedSettings6.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings6.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings7.ConnectToServerConsole
- IMsRdpClientAdvancedSettings7.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings7.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings8.ConnectToServerConsole
- IMsRdpClientAdvancedSettings8.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings8.put_ConnectToServerConsole
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e3385b25a9dbe3e77085ae011b85e9be21b224
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964142"
---
# <a name="imsrdpclientadvancedsettingsconnecttoserverconsole-property"></a><span data-ttu-id="6a09e-121">Proprietà IMsRdpClientAdvancedSettings:: ConnectToServerConsole</span><span class="sxs-lookup"><span data-stu-id="6a09e-121">IMsRdpClientAdvancedSettings::ConnectToServerConsole property</span></span>

<span data-ttu-id="6a09e-122">Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="6a09e-122">This property is not supported.</span></span> <span data-ttu-id="6a09e-123">Le chiamate a **ConnectToServerConsole** restituiscono sempre **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="6a09e-123">Calls to **ConnectToServerConsole** always return **S\_FALSE**.</span></span>

<span data-ttu-id="6a09e-124">Utilizzare la proprietà [**ConnectToAdministerServer**](imsrdpclientadvancedsettings6-connecttoadministerserver.md) per connettersi alla sessione utilizzata a scopo amministrativo.</span><span class="sxs-lookup"><span data-stu-id="6a09e-124">Use the [**ConnectToAdministerServer**](imsrdpclientadvancedsettings6-connecttoadministerserver.md) property to connect to the session that is used for administrative purposes.</span></span>

<span data-ttu-id="6a09e-125">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="6a09e-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a09e-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a09e-126">Syntax</span></span>


```C++
HRESULT put_ConnectToServerConsole(
  [in]  VARIANT_BOOL connectToServerConsole
);

HRESULT get_ConnectToServerConsole(
  [out] VARIANT_BOOL *pconnectToServerConsole
);
```



## <a name="property-value"></a><span data-ttu-id="6a09e-127">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="6a09e-127">Property value</span></span>

<span data-ttu-id="6a09e-128">Impostare questo parametro su **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="6a09e-128">Set this parameter to **VARIANT\_FALSE**.</span></span> <span data-ttu-id="6a09e-129">**Variante \_ TRUE** non è supportato.</span><span class="sxs-lookup"><span data-stu-id="6a09e-129">**VARIANT\_TRUE** is not supported.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6a09e-130">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="6a09e-130">Error codes</span></span>

<span data-ttu-id="6a09e-131">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="6a09e-131">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a09e-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a09e-132">Remarks</span></span>

<span data-ttu-id="6a09e-133">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6a09e-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a09e-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a09e-134">Requirements</span></span>



| <span data-ttu-id="6a09e-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a09e-135">Requirement</span></span> | <span data-ttu-id="6a09e-136">Valore</span><span class="sxs-lookup"><span data-stu-id="6a09e-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a09e-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a09e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6a09e-138">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6a09e-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="6a09e-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a09e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6a09e-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6a09e-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="6a09e-141">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="6a09e-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="6a09e-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a09e-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="6a09e-143">DLL</span><span class="sxs-lookup"><span data-stu-id="6a09e-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a09e-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a09e-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="6a09e-145">IID</span><span class="sxs-lookup"><span data-stu-id="6a09e-145">IID</span></span><br/>                      | <span data-ttu-id="6a09e-146">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="6a09e-146">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6a09e-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a09e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a09e-148">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="6a09e-148">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="6a09e-149">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="6a09e-149">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="6a09e-150">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="6a09e-150">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="6a09e-151">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="6a09e-151">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="6a09e-152">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="6a09e-152">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="6a09e-153">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="6a09e-153">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="6a09e-154">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="6a09e-154">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="6a09e-155">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="6a09e-155">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





