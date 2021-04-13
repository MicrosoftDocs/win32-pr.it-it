---
title: Proprietà singleConnectionTimeout di IMsRdpClientAdvancedSettings
description: Specifica il periodo di tempo massimo, in secondi, durante il quale il controllo client attende una connessione a un indirizzo IP.
ms.assetid: 57fb2397-8229-4446-88fd-e75cb96c7ac5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà singleConnectionTimeout
- Servizi Desktop remoto proprietà singleConnectionTimeout, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà singleConnectionTimeout
- Servizi Desktop remoto proprietà singleConnectionTimeout, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà singleConnectionTimeout
- Servizi Desktop remoto proprietà singleConnectionTimeout, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà singleConnectionTimeout
- Servizi Desktop remoto proprietà singleConnectionTimeout, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà singleConnectionTimeout
- Servizi Desktop remoto proprietà singleConnectionTimeout, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà singleConnectionTimeout
- Servizi Desktop remoto proprietà singleConnectionTimeout, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà singleConnectionTimeout
- Servizi Desktop remoto proprietà singleConnectionTimeout, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà singleConnectionTimeout
- Servizi Desktop remoto proprietà singleConnectionTimeout, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà singleConnectionTimeout
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.singleConnectionTimeout
- IMsRdpClientAdvancedSettings.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings2.singleConnectionTimeout
- IMsRdpClientAdvancedSettings2.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings2.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings3.singleConnectionTimeout
- IMsRdpClientAdvancedSettings3.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings3.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings4.singleConnectionTimeout
- IMsRdpClientAdvancedSettings4.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings4.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings5.singleConnectionTimeout
- IMsRdpClientAdvancedSettings5.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings5.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings6.singleConnectionTimeout
- IMsRdpClientAdvancedSettings6.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings6.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings7.singleConnectionTimeout
- IMsRdpClientAdvancedSettings7.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings7.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings8.singleConnectionTimeout
- IMsRdpClientAdvancedSettings8.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings8.put_singleConnectionTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a0d2eb34235c874b4408e5e4c6f0a349a1ab93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400241"
---
# <a name="imsrdpclientadvancedsettingssingleconnectiontimeout-property"></a><span data-ttu-id="fd65b-120">Proprietà IMsRdpClientAdvancedSettings:: singleConnectionTimeout</span><span class="sxs-lookup"><span data-stu-id="fd65b-120">IMsRdpClientAdvancedSettings::singleConnectionTimeout property</span></span>

<span data-ttu-id="fd65b-121">Specifica il periodo di tempo massimo, in secondi, durante il quale il controllo client attende una connessione a un indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="fd65b-121">Specifies the maximum length of time, in seconds, that the client control waits for a connection to an IP address.</span></span>

<span data-ttu-id="fd65b-122">Durante la connessione, il controllo può tentare di connettersi a più indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="fd65b-122">During connection, the control may attempt to connect to multiple IP addresses.</span></span>

<span data-ttu-id="fd65b-123">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="fd65b-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd65b-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd65b-124">Syntax</span></span>


```C++
HRESULT put_singleConnectionTimeout(
  [in]  LONG singleConnectionTimeout
);

HRESULT get_singleConnectionTimeout(
  [out] LONG *psingleConnectionTimeout
);
```



## <a name="property-value"></a><span data-ttu-id="fd65b-125">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="fd65b-125">Property value</span></span>

<span data-ttu-id="fd65b-126">Nuova ora, in secondi.</span><span class="sxs-lookup"><span data-stu-id="fd65b-126">The new time, in seconds.</span></span> <span data-ttu-id="fd65b-127">Il valore massimo è 600.</span><span class="sxs-lookup"><span data-stu-id="fd65b-127">The maximum value is 600.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fd65b-128">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="fd65b-128">Error codes</span></span>

<span data-ttu-id="fd65b-129">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="fd65b-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd65b-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd65b-130">Remarks</span></span>

<span data-ttu-id="fd65b-131">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="fd65b-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd65b-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd65b-132">Requirements</span></span>



| <span data-ttu-id="fd65b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd65b-133">Requirement</span></span> | <span data-ttu-id="fd65b-134">Valore</span><span class="sxs-lookup"><span data-stu-id="fd65b-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd65b-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd65b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="fd65b-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd65b-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="fd65b-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd65b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="fd65b-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd65b-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="fd65b-139">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="fd65b-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="fd65b-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd65b-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="fd65b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="fd65b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd65b-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd65b-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="fd65b-143">IID</span><span class="sxs-lookup"><span data-stu-id="fd65b-143">IID</span></span><br/>                      | <span data-ttu-id="fd65b-144">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="fd65b-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fd65b-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd65b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd65b-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="fd65b-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="fd65b-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="fd65b-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="fd65b-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="fd65b-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="fd65b-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="fd65b-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="fd65b-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="fd65b-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="fd65b-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="fd65b-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="fd65b-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="fd65b-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="fd65b-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="fd65b-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="fd65b-154">**overallConnectionTimeout**</span><span class="sxs-lookup"><span data-stu-id="fd65b-154">**overallConnectionTimeout**</span></span>](imsrdpclientadvancedsettings-overallconnectiontimeout.md)
</dt> </dl>

 

 





