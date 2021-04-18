---
title: Proprietà overallConnectionTimeout di IMsRdpClientAdvancedSettings
description: Specifica il periodo di tempo totale, in secondi, durante il quale il controllo client attende il completamento di una connessione.
ms.assetid: 02fb24e1-b5e4-4d8e-a1c2-a9bd62a69bed
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà overallConnectionTimeout
- Servizi Desktop remoto proprietà overallConnectionTimeout, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà overallConnectionTimeout
- Servizi Desktop remoto proprietà overallConnectionTimeout, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà overallConnectionTimeout
- Servizi Desktop remoto proprietà overallConnectionTimeout, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà overallConnectionTimeout
- Servizi Desktop remoto proprietà overallConnectionTimeout, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà overallConnectionTimeout
- Servizi Desktop remoto proprietà overallConnectionTimeout, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà overallConnectionTimeout
- Servizi Desktop remoto proprietà overallConnectionTimeout, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà overallConnectionTimeout
- Servizi Desktop remoto proprietà overallConnectionTimeout, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà overallConnectionTimeout
- Servizi Desktop remoto proprietà overallConnectionTimeout, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà overallConnectionTimeout
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.overallConnectionTimeout
- IMsRdpClientAdvancedSettings.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings2.overallConnectionTimeout
- IMsRdpClientAdvancedSettings2.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings2.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings3.overallConnectionTimeout
- IMsRdpClientAdvancedSettings3.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings3.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings4.overallConnectionTimeout
- IMsRdpClientAdvancedSettings4.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings4.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings5.overallConnectionTimeout
- IMsRdpClientAdvancedSettings5.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings5.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings6.overallConnectionTimeout
- IMsRdpClientAdvancedSettings6.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings6.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings7.overallConnectionTimeout
- IMsRdpClientAdvancedSettings7.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings7.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings8.overallConnectionTimeout
- IMsRdpClientAdvancedSettings8.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings8.put_overallConnectionTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50de6687d3d5cbccb3f7fdab94eca5ba4f2331c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301308"
---
# <a name="imsrdpclientadvancedsettingsoverallconnectiontimeout-property"></a><span data-ttu-id="56bfe-120">Proprietà IMsRdpClientAdvancedSettings:: overallConnectionTimeout</span><span class="sxs-lookup"><span data-stu-id="56bfe-120">IMsRdpClientAdvancedSettings::overallConnectionTimeout property</span></span>

<span data-ttu-id="56bfe-121">Specifica il periodo di tempo totale, in secondi, durante il quale il controllo client attende il completamento di una connessione.</span><span class="sxs-lookup"><span data-stu-id="56bfe-121">Specifies the total length of time, in seconds, that the client control waits for a connection to complete.</span></span>

<span data-ttu-id="56bfe-122">Se il tempo specificato scade prima del completamento della connessione, il controllo si disconnette e chiama il metodo [**IMsTscAxEvents:: disconnected**](imstscaxevents-ondisconnected.md) .</span><span class="sxs-lookup"><span data-stu-id="56bfe-122">If the specified time elapses before connection completes, the control disconnects and calls the [**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md) method.</span></span>

<span data-ttu-id="56bfe-123">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="56bfe-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="56bfe-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56bfe-124">Syntax</span></span>


```C++
HRESULT put_overallConnectionTimeout(
  [in]  LONG overallConnectionTimeout
);

HRESULT get_overallConnectionTimeout(
  [out] LONG *poverallConnectionTimeout
);
```



## <a name="property-value"></a><span data-ttu-id="56bfe-125">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="56bfe-125">Property value</span></span>

<span data-ttu-id="56bfe-126">Nuova ora, in secondi.</span><span class="sxs-lookup"><span data-stu-id="56bfe-126">The new time, in seconds.</span></span> <span data-ttu-id="56bfe-127">Il valore massimo è 600, che rappresenta 10 minuti.</span><span class="sxs-lookup"><span data-stu-id="56bfe-127">The maximum value is 600, which represents 10 minutes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="56bfe-128">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="56bfe-128">Error codes</span></span>

<span data-ttu-id="56bfe-129">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="56bfe-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="56bfe-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="56bfe-130">Remarks</span></span>

<span data-ttu-id="56bfe-131">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="56bfe-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="56bfe-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56bfe-132">Requirements</span></span>



| <span data-ttu-id="56bfe-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="56bfe-133">Requirement</span></span> | <span data-ttu-id="56bfe-134">Valore</span><span class="sxs-lookup"><span data-stu-id="56bfe-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56bfe-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56bfe-135">Minimum supported client</span></span><br/> | <span data-ttu-id="56bfe-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56bfe-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="56bfe-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56bfe-137">Minimum supported server</span></span><br/> | <span data-ttu-id="56bfe-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56bfe-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="56bfe-139">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="56bfe-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="56bfe-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56bfe-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="56bfe-141">DLL</span><span class="sxs-lookup"><span data-stu-id="56bfe-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56bfe-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56bfe-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="56bfe-143">IID</span><span class="sxs-lookup"><span data-stu-id="56bfe-143">IID</span></span><br/>                      | <span data-ttu-id="56bfe-144">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="56bfe-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="56bfe-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56bfe-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56bfe-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="56bfe-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="56bfe-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="56bfe-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="56bfe-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="56bfe-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="56bfe-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="56bfe-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="56bfe-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="56bfe-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="56bfe-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="56bfe-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="56bfe-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="56bfe-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="56bfe-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="56bfe-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="56bfe-154">**singleConnectionTimeout**</span><span class="sxs-lookup"><span data-stu-id="56bfe-154">**singleConnectionTimeout**</span></span>](imsrdpclientadvancedsettings-singleconnectiontimeout.md)
</dt> </dl>

 

 





