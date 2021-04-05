---
title: Proprietà maxEventCount di IMsRdpClientAdvancedSettings
description: Questa proprietà non è supportata. | Proprietà maxEventCount di IMsRdpClientAdvancedSettings
ms.assetid: d7b5951d-8cc3-48b4-af1b-1f547afbc6ae
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà maxEventCount
- Servizi Desktop remoto proprietà maxEventCount, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà maxEventCount
- Servizi Desktop remoto proprietà maxEventCount, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà maxEventCount
- Servizi Desktop remoto proprietà maxEventCount, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà maxEventCount
- Servizi Desktop remoto proprietà maxEventCount, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà maxEventCount
- Servizi Desktop remoto proprietà maxEventCount, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà maxEventCount
- Servizi Desktop remoto proprietà maxEventCount, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà maxEventCount
- Servizi Desktop remoto proprietà maxEventCount, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà maxEventCount
- Servizi Desktop remoto proprietà maxEventCount, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà maxEventCount
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.maxEventCount
- IMsRdpClientAdvancedSettings.get_maxEventCount
- IMsRdpClientAdvancedSettings.put_maxEventCount
- IMsRdpClientAdvancedSettings2.maxEventCount
- IMsRdpClientAdvancedSettings2.get_maxEventCount
- IMsRdpClientAdvancedSettings2.put_maxEventCount
- IMsRdpClientAdvancedSettings3.maxEventCount
- IMsRdpClientAdvancedSettings3.get_maxEventCount
- IMsRdpClientAdvancedSettings3.put_maxEventCount
- IMsRdpClientAdvancedSettings4.maxEventCount
- IMsRdpClientAdvancedSettings4.get_maxEventCount
- IMsRdpClientAdvancedSettings4.put_maxEventCount
- IMsRdpClientAdvancedSettings5.maxEventCount
- IMsRdpClientAdvancedSettings5.get_maxEventCount
- IMsRdpClientAdvancedSettings5.put_maxEventCount
- IMsRdpClientAdvancedSettings6.maxEventCount
- IMsRdpClientAdvancedSettings6.get_maxEventCount
- IMsRdpClientAdvancedSettings6.put_maxEventCount
- IMsRdpClientAdvancedSettings7.maxEventCount
- IMsRdpClientAdvancedSettings7.get_maxEventCount
- IMsRdpClientAdvancedSettings7.put_maxEventCount
- IMsRdpClientAdvancedSettings8.maxEventCount
- IMsRdpClientAdvancedSettings8.get_maxEventCount
- IMsRdpClientAdvancedSettings8.put_maxEventCount
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb305d4a81b3c4dd9eb53dceab5a4e685c57c060
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886116"
---
# <a name="imsrdpclientadvancedsettingsmaxeventcount-property"></a><span data-ttu-id="a7548-121">Proprietà IMsRdpClientAdvancedSettings:: maxEventCount</span><span class="sxs-lookup"><span data-stu-id="a7548-121">IMsRdpClientAdvancedSettings::maxEventCount property</span></span>

<span data-ttu-id="a7548-122">Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="a7548-122">This property is not supported.</span></span>

<span data-ttu-id="a7548-123">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a7548-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7548-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7548-124">Syntax</span></span>


```C++
HRESULT put_maxEventCount(
  [in]  LONG maxEventCount
);

HRESULT get_maxEventCount(
  [out] LONG pmaxEventCount
);
```



## <a name="property-value"></a><span data-ttu-id="a7548-125">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a7548-125">Property value</span></span>

<span data-ttu-id="a7548-126">Il nuovo conteggio degli eventi.</span><span class="sxs-lookup"><span data-stu-id="a7548-126">The new event count.</span></span> <span data-ttu-id="a7548-127">Il valore predefinito è 100.</span><span class="sxs-lookup"><span data-stu-id="a7548-127">The default is 100.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a7548-128">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="a7548-128">Error codes</span></span>

<span data-ttu-id="a7548-129">Restituisce un valore **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="a7548-129">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7548-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="a7548-130">Remarks</span></span>

<span data-ttu-id="a7548-131">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a7548-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a7548-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7548-132">Requirements</span></span>



| <span data-ttu-id="a7548-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7548-133">Requirement</span></span> | <span data-ttu-id="a7548-134">Valore</span><span class="sxs-lookup"><span data-stu-id="a7548-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7548-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7548-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a7548-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a7548-136">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="a7548-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7548-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a7548-138">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a7548-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="a7548-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a7548-139">End of client support</span></span><br/>    | <span data-ttu-id="a7548-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a7548-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="a7548-141">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="a7548-141">End of server support</span></span><br/>    | <span data-ttu-id="a7548-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a7548-142">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="a7548-143">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a7548-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="a7548-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7548-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="a7548-145">DLL</span><span class="sxs-lookup"><span data-stu-id="a7548-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7548-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7548-146"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="a7548-147">IID</span><span class="sxs-lookup"><span data-stu-id="a7548-147">IID</span></span><br/>                      | <span data-ttu-id="a7548-148">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="a7548-148">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a7548-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7548-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7548-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="a7548-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="a7548-151">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="a7548-151">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="a7548-152">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="a7548-152">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="a7548-153">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="a7548-153">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="a7548-154">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="a7548-154">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="a7548-155">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="a7548-155">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="a7548-156">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="a7548-156">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="a7548-157">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="a7548-157">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





