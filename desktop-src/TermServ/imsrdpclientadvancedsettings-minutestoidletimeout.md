---
title: Proprietà MinutesToIdleTimeout di IMsRdpClientAdvancedSettings
description: Specifica il periodo di tempo massimo, in minuti, durante il quale il client deve rimanere connesso senza l'input dell'utente. Se il tempo specificato scade, il controllo chiama il metodo IMsTscAxEvents OnIdleTimeoutNotification.
ms.assetid: 709238ea-45f8-4bdc-9bbe-019d54ca27bf
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà MinutesToIdleTimeout
- Servizi Desktop remoto proprietà MinutesToIdleTimeout, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà MinutesToIdleTimeout
- Servizi Desktop remoto proprietà MinutesToIdleTimeout, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà MinutesToIdleTimeout
- Servizi Desktop remoto proprietà MinutesToIdleTimeout, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà MinutesToIdleTimeout
- Servizi Desktop remoto proprietà MinutesToIdleTimeout, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà MinutesToIdleTimeout
- Servizi Desktop remoto proprietà MinutesToIdleTimeout, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà MinutesToIdleTimeout
- Servizi Desktop remoto proprietà MinutesToIdleTimeout, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà MinutesToIdleTimeout
- Servizi Desktop remoto proprietà MinutesToIdleTimeout, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà MinutesToIdleTimeout
- Servizi Desktop remoto proprietà MinutesToIdleTimeout, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà MinutesToIdleTimeout
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings2.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings2.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings2.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings3.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings3.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings3.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings4.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings4.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings4.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings5.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings5.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings5.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings6.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings6.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings6.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings7.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings7.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings7.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings8.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings8.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings8.put_MinutesToIdleTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b5e42258ed670ac0323723cafe7b2792f8c5bd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301311"
---
# <a name="imsrdpclientadvancedsettingsminutestoidletimeout-property"></a><span data-ttu-id="b978e-121">Proprietà IMsRdpClientAdvancedSettings:: MinutesToIdleTimeout</span><span class="sxs-lookup"><span data-stu-id="b978e-121">IMsRdpClientAdvancedSettings::MinutesToIdleTimeout property</span></span>

<span data-ttu-id="b978e-122">Specifica il periodo di tempo massimo, in minuti, durante il quale il client deve rimanere connesso senza l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b978e-122">Specifies the maximum length of time, in minutes, that the client should remain connected without user input.</span></span> <span data-ttu-id="b978e-123">Se il tempo specificato scade, il controllo chiama il metodo [**IMsTscAxEvents:: OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="b978e-123">If the specified time elapses, the control calls the [**IMsTscAxEvents::OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md) method.</span></span>

<span data-ttu-id="b978e-124">È possibile utilizzare questa proprietà in una situazione in cui è necessario disconnettere una sessione inattiva. ad esempio, in un ambiente chiosco multimediale.</span><span class="sxs-lookup"><span data-stu-id="b978e-124">You can use this property in a situation where you need to disconnect an idle session; for example, in a kiosk environment.</span></span>

<span data-ttu-id="b978e-125">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="b978e-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b978e-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b978e-126">Syntax</span></span>


```C++
HRESULT put_MinutesToIdleTimeout(
  [in]  LONG minutesToIdleTimeout
);

HRESULT get_MinutesToIdleTimeout(
  [out] LONG *pminutesToIdleTimeout
);
```



## <a name="property-value"></a><span data-ttu-id="b978e-127">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b978e-127">Property value</span></span>

<span data-ttu-id="b978e-128">Nuova ora, in minuti.</span><span class="sxs-lookup"><span data-stu-id="b978e-128">The new time, in minutes.</span></span> <span data-ttu-id="b978e-129">Il valore predefinito è zero, che disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="b978e-129">The default value is zero, which disables the feature.</span></span> <span data-ttu-id="b978e-130">Il valore massimo è 240, che rappresenta 4 ore.</span><span class="sxs-lookup"><span data-stu-id="b978e-130">The maximum value is 240, which represents 4 hours.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b978e-131">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="b978e-131">Error codes</span></span>

<span data-ttu-id="b978e-132">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b978e-132">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="b978e-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="b978e-133">Remarks</span></span>

<span data-ttu-id="b978e-134">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="b978e-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b978e-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b978e-135">Requirements</span></span>



| <span data-ttu-id="b978e-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="b978e-136">Requirement</span></span> | <span data-ttu-id="b978e-137">Valore</span><span class="sxs-lookup"><span data-stu-id="b978e-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b978e-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b978e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b978e-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b978e-139">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="b978e-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b978e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b978e-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b978e-141">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="b978e-142">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="b978e-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="b978e-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b978e-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="b978e-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b978e-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b978e-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b978e-145"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="b978e-146">IID</span><span class="sxs-lookup"><span data-stu-id="b978e-146">IID</span></span><br/>                      | <span data-ttu-id="b978e-147">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="b978e-147">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b978e-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b978e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b978e-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="b978e-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="b978e-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="b978e-150">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="b978e-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="b978e-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="b978e-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="b978e-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="b978e-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="b978e-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="b978e-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="b978e-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="b978e-155">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="b978e-155">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="b978e-156">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="b978e-156">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





