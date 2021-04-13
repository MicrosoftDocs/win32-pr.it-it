---
title: Proprietà LoadBalanceInfo di IMsRdpClientAdvancedSettings
description: Specifica il cookie di bilanciamento del carico che verrà inserito nel pacchetto della richiesta di connessione X. 224 nella sequenza di connessione del protocollo server host sessione Desktop remoto (host sessione Desktop remoto).
ms.assetid: 25f12a2e-00a2-42a8-afd3-81efcd94da94
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà LoadBalanceInfo
- Servizi Desktop remoto proprietà LoadBalanceInfo, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà LoadBalanceInfo
- Servizi Desktop remoto proprietà LoadBalanceInfo, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà LoadBalanceInfo
- Servizi Desktop remoto proprietà LoadBalanceInfo, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà LoadBalanceInfo
- Servizi Desktop remoto proprietà LoadBalanceInfo, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà LoadBalanceInfo
- Servizi Desktop remoto proprietà LoadBalanceInfo, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà LoadBalanceInfo
- Servizi Desktop remoto proprietà LoadBalanceInfo, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà LoadBalanceInfo
- Servizi Desktop remoto proprietà LoadBalanceInfo, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà LoadBalanceInfo
- Servizi Desktop remoto proprietà LoadBalanceInfo, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà LoadBalanceInfo
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.LoadBalanceInfo
- IMsRdpClientAdvancedSettings.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.put_LoadBalanceInfo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a12112eb2a18d38993e905f8d36175f1ab15f58a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400449"
---
# <a name="imsrdpclientadvancedsettingsloadbalanceinfo-property"></a><span data-ttu-id="f9cb4-120">Proprietà IMsRdpClientAdvancedSettings:: LoadBalanceInfo</span><span class="sxs-lookup"><span data-stu-id="f9cb4-120">IMsRdpClientAdvancedSettings::LoadBalanceInfo property</span></span>

<span data-ttu-id="f9cb4-121">Specifica il cookie di bilanciamento del carico che verrà inserito nel pacchetto della richiesta di connessione X. 224 nella sequenza di connessione del protocollo server host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="f9cb4-121">Specifies the load balancing cookie that will be placed in the X.224 Connection Request packet in the Remote Desktop Session Host (RD Session Host) server protocol connection sequence.</span></span>

<span data-ttu-id="f9cb4-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9cb4-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9cb4-123">Syntax</span></span>


```C++
HRESULT put_LoadBalanceInfo(
  [in]  BSTR newLBInfo
);

HRESULT get_LoadBalanceInfo(
  [out] BSTR *pLBInfo
);
```



## <a name="property-value"></a><span data-ttu-id="f9cb4-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f9cb4-124">Property value</span></span>

<span data-ttu-id="f9cb4-125">Puntatore al nuovo cookie.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-125">Pointer to the new cookie.</span></span> <span data-ttu-id="f9cb4-126">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-126">For more information, see the remarks section.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f9cb4-127">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="f9cb4-127">Error codes</span></span>

<span data-ttu-id="f9cb4-128">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9cb4-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9cb4-129">Remarks</span></span>

<span data-ttu-id="f9cb4-130">Le informazioni sul bilanciamento del carico vengono utilizzate dai router di bilanciamento del carico per scegliere il server migliore per il client quando si utilizzano farm di server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-130">The load balancing information is used by load balancing routers to choose the best server for the client when using farms of RD Session Host servers.</span></span> <span data-ttu-id="f9cb4-131">Il server Host sessione Desktop remoto non utilizza queste informazioni e lo eliminerà.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-131">The RD Session Host server itself does not use this information and will discard it.</span></span>

<span data-ttu-id="f9cb4-132">Il cookie utilizza la sintassi seguente, con distinzione tra maiuscole e minuscole:</span><span class="sxs-lookup"><span data-stu-id="f9cb4-132">The cookie uses the following, case-sensitive, syntax:</span></span>

<span data-ttu-id="f9cb4-133">**Cookie: MSTS =**_IpAddressAndPortNumber_*_\\ r \\ n_*</span><span class="sxs-lookup"><span data-stu-id="f9cb4-133">**Cookie: msts=**_IpAddressAndPortNumber_*_\\r\\n_*</span></span>

<span data-ttu-id="f9cb4-134">Dove *IpAddressAndPortNumber* è l'indirizzo IP e il numero di porta, in ordine byte di rete.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-134">Where *IpAddressAndPortNumber* is the IP address and port number, in network byte order.</span></span>

<span data-ttu-id="f9cb4-135">Ad esempio, il cookie usato per accedere all'indirizzo IP di 172.31.249.216, il numero di porta 3389 è il seguente:</span><span class="sxs-lookup"><span data-stu-id="f9cb4-135">For example, the cookie used to access the IP address of 172.31.249.216, port number 3389 is as follows:</span></span>

<span data-ttu-id="f9cb4-136">**Cookie: MSTS = 3640205228.15629.0000 \\ r \\ n**</span><span class="sxs-lookup"><span data-stu-id="f9cb4-136">**Cookie: msts=3640205228.15629.0000\\r\\n**</span></span>

<span data-ttu-id="f9cb4-137">I quattro zeri finali sono facoltativi e sono riservati.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-137">The final four zeros are optional and are reserved.</span></span> <span data-ttu-id="f9cb4-138">Il separatore decimale finale è obbligatorio, così come il ritorno a capo e il avanzamento riga finali.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-138">The final decimal point is required, as are the trailing carriage return and linefeed.</span></span> <span data-ttu-id="f9cb4-139">La lunghezza della stringa, in caratteri, deve essere un multiplo pari a 2, quindi aggiungere uno spazio se necessario.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-139">The length of the string, in characters, must be an even multiple of 2, so add a space if necessary.</span></span>

<span data-ttu-id="f9cb4-140">Se non viene fornito alcun cookie, il valore predefinito è **cookie: mstshash =**_username_*_\\ r \\ n_*.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-140">If no cookie is supplied, the default is **Cookie: mstshash=**_UserName_*_\\r\\n_*.</span></span>

<span data-ttu-id="f9cb4-141">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f9cb4-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9cb4-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9cb4-142">Requirements</span></span>



| <span data-ttu-id="f9cb4-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9cb4-143">Requirement</span></span> | <span data-ttu-id="f9cb4-144">Valore</span><span class="sxs-lookup"><span data-stu-id="f9cb4-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9cb4-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9cb4-145">Minimum supported client</span></span><br/> | <span data-ttu-id="f9cb4-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9cb4-146">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="f9cb4-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9cb4-147">Minimum supported server</span></span><br/> | <span data-ttu-id="f9cb4-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9cb4-148">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="f9cb4-149">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f9cb4-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="f9cb4-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9cb4-150"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f9cb4-151">DLL</span><span class="sxs-lookup"><span data-stu-id="f9cb4-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9cb4-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9cb4-152"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f9cb4-153">IID</span><span class="sxs-lookup"><span data-stu-id="f9cb4-153">IID</span></span><br/>                      | <span data-ttu-id="f9cb4-154">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="f9cb4-154">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9cb4-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9cb4-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9cb4-156">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="f9cb4-156">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="f9cb4-157">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="f9cb4-157">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="f9cb4-158">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="f9cb4-158">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="f9cb4-159">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="f9cb4-159">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="f9cb4-160">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="f9cb4-160">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="f9cb4-161">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="f9cb4-161">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="f9cb4-162">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="f9cb4-162">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="f9cb4-163">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="f9cb4-163">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





