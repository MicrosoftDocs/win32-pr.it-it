---
title: Proprietà RDPPort di IMsRdpClientAdvancedSettings
description: Specifica la porta di connessione.
ms.assetid: 15be7ef8-8ed2-46e0-8cc5-d5cf1642b79e
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà RDPPort
- Servizi Desktop remoto proprietà RDPPort, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà RDPPort
- Servizi Desktop remoto proprietà RDPPort, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà RDPPort
- Servizi Desktop remoto proprietà RDPPort, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà RDPPort
- Servizi Desktop remoto proprietà RDPPort, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà RDPPort
- Servizi Desktop remoto proprietà RDPPort, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà RDPPort
- Servizi Desktop remoto proprietà RDPPort, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà RDPPort
- Servizi Desktop remoto proprietà RDPPort, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà RDPPort
- Servizi Desktop remoto proprietà RDPPort, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà RDPPort
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RDPPort
- IMsRdpClientAdvancedSettings.get_RDPPort
- IMsRdpClientAdvancedSettings.put_RDPPort
- IMsRdpClientAdvancedSettings2.RDPPort
- IMsRdpClientAdvancedSettings2.get_RDPPort
- IMsRdpClientAdvancedSettings2.put_RDPPort
- IMsRdpClientAdvancedSettings3.RDPPort
- IMsRdpClientAdvancedSettings3.get_RDPPort
- IMsRdpClientAdvancedSettings3.put_RDPPort
- IMsRdpClientAdvancedSettings4.RDPPort
- IMsRdpClientAdvancedSettings4.get_RDPPort
- IMsRdpClientAdvancedSettings4.put_RDPPort
- IMsRdpClientAdvancedSettings5.RDPPort
- IMsRdpClientAdvancedSettings5.get_RDPPort
- IMsRdpClientAdvancedSettings5.put_RDPPort
- IMsRdpClientAdvancedSettings6.RDPPort
- IMsRdpClientAdvancedSettings6.get_RDPPort
- IMsRdpClientAdvancedSettings6.put_RDPPort
- IMsRdpClientAdvancedSettings7.RDPPort
- IMsRdpClientAdvancedSettings7.get_RDPPort
- IMsRdpClientAdvancedSettings7.put_RDPPort
- IMsRdpClientAdvancedSettings8.RDPPort
- IMsRdpClientAdvancedSettings8.get_RDPPort
- IMsRdpClientAdvancedSettings8.put_RDPPort
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c8eafb3521d6338a0a2d469c813ff7ffa447a20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121434"
---
# <a name="imsrdpclientadvancedsettingsrdpport-property"></a><span data-ttu-id="4874b-120">Proprietà IMsRdpClientAdvancedSettings:: RDPPort</span><span class="sxs-lookup"><span data-stu-id="4874b-120">IMsRdpClientAdvancedSettings::RDPPort property</span></span>

<span data-ttu-id="4874b-121">Specifica la porta di connessione.</span><span class="sxs-lookup"><span data-stu-id="4874b-121">Specifies the connection port.</span></span>

<span data-ttu-id="4874b-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="4874b-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4874b-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4874b-123">Syntax</span></span>


```C++
HRESULT put_RDPPort(
  [in]  LONG rdpPort
);

HRESULT get_RDPPort(
  [out] LONG *prdpPort
);
```



## <a name="property-value"></a><span data-ttu-id="4874b-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4874b-124">Property value</span></span>

<span data-ttu-id="4874b-125">Nuova porta.</span><span class="sxs-lookup"><span data-stu-id="4874b-125">The new port.</span></span> <span data-ttu-id="4874b-126">Il valore predefinito è 3389.</span><span class="sxs-lookup"><span data-stu-id="4874b-126">The default value is 3389.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4874b-127">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="4874b-127">Error codes</span></span>

<span data-ttu-id="4874b-128">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4874b-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="4874b-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="4874b-129">Remarks</span></span>

<span data-ttu-id="4874b-130">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="4874b-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4874b-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4874b-131">Requirements</span></span>



| <span data-ttu-id="4874b-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="4874b-132">Requirement</span></span> | <span data-ttu-id="4874b-133">Valore</span><span class="sxs-lookup"><span data-stu-id="4874b-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4874b-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4874b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4874b-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4874b-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="4874b-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4874b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4874b-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4874b-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="4874b-138">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="4874b-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="4874b-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4874b-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="4874b-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4874b-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4874b-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4874b-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="4874b-142">IID</span><span class="sxs-lookup"><span data-stu-id="4874b-142">IID</span></span><br/>                      | <span data-ttu-id="4874b-143">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="4874b-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4874b-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4874b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4874b-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="4874b-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="4874b-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="4874b-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="4874b-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="4874b-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="4874b-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="4874b-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="4874b-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="4874b-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="4874b-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="4874b-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="4874b-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="4874b-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="4874b-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="4874b-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





