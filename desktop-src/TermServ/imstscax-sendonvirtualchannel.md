---
title: Metodo IMsTscAx SendOnVirtualChannel
description: Invia dati al server host sessione Desktop remoto (host sessione Desktop remoto) su un canale virtuale creato in precedenza tramite il metodo CreateVirtualChannels.
ms.assetid: 795ef508-bdf7-4897-84b1-931615262293
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SendOnVirtualChannel
- Metodo SendOnVirtualChannel Servizi Desktop remoto, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, metodo SendOnVirtualChannel
- Metodo SendOnVirtualChannel Servizi Desktop remoto, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, metodo SendOnVirtualChannel
- Metodo SendOnVirtualChannel Servizi Desktop remoto, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, metodo SendOnVirtualChannel
- Metodo SendOnVirtualChannel Servizi Desktop remoto, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, metodo SendOnVirtualChannel
- Metodo SendOnVirtualChannel Servizi Desktop remoto, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, metodo SendOnVirtualChannel
- Metodo SendOnVirtualChannel Servizi Desktop remoto, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, metodo SendOnVirtualChannel
- Metodo SendOnVirtualChannel Servizi Desktop remoto, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, metodo SendOnVirtualChannel
- Metodo SendOnVirtualChannel Servizi Desktop remoto, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, metodo SendOnVirtualChannel
- Metodo SendOnVirtualChannel Servizi Desktop remoto, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, metodo SendOnVirtualChannel
- Metodo SendOnVirtualChannel Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, metodo SendOnVirtualChannel
topic_type:
- apiref
api_name:
- IMsTscAx.SendOnVirtualChannel
- IMsRdpClient.SendOnVirtualChannel
- IMsRdpClient2.SendOnVirtualChannel
- IMsRdpClient3.SendOnVirtualChannel
- IMsRdpClient4.SendOnVirtualChannel
- IMsRdpClient5.SendOnVirtualChannel
- IMsRdpClient6.SendOnVirtualChannel
- IMsRdpClient7.SendOnVirtualChannel
- IMsRdpClient8.SendOnVirtualChannel
- IMsRdpClient9.SendOnVirtualChannel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1371ae17978601a3194f755dd364d9227b8fc28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475611"
---
# <a name="imstscaxsendonvirtualchannel-method"></a><span data-ttu-id="98eec-124">Metodo IMsTscAx:: SendOnVirtualChannel</span><span class="sxs-lookup"><span data-stu-id="98eec-124">IMsTscAx::SendOnVirtualChannel method</span></span>

<span data-ttu-id="98eec-125">Invia dati al server host sessione Desktop remoto (host sessione Desktop remoto) su un canale virtuale creato in precedenza tramite il metodo [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) .</span><span class="sxs-lookup"><span data-stu-id="98eec-125">Sends data to the Remote Desktop Session Host (RD Session Host) server over a virtual channel that was created previously by using the [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="98eec-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98eec-126">Syntax</span></span>


```C++
HRESULT SendOnVirtualChannel(
  [in] BSTR ChanName,
  [in] BSTR ChanData
);
```



## <a name="parameters"></a><span data-ttu-id="98eec-127">Parametri</span><span class="sxs-lookup"><span data-stu-id="98eec-127">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98eec-128">*Channame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="98eec-128">*ChanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98eec-129">Nome del canale virtuale specificato nella chiamata a [**CreateVirtualChannels**](imstscax-createvirtualchannels.md).</span><span class="sxs-lookup"><span data-stu-id="98eec-129">The virtual channel name that was specified in the call to [**CreateVirtualChannels**](imstscax-createvirtualchannels.md).</span></span>

</dd> <dt>

<span data-ttu-id="98eec-130">*ChanData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="98eec-130">*ChanData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98eec-131">Dati da inviare sul canale virtuale, in formato **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="98eec-131">The data to send over the virtual channel, in **BSTR** form.</span></span> <span data-ttu-id="98eec-132">Non esiste alcuna restrizione che questi dati devono essere stringhe con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="98eec-132">There is no restriction that this data must be null-terminated strings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98eec-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="98eec-133">Return value</span></span>

<span data-ttu-id="98eec-134">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="98eec-134">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="98eec-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="98eec-135">Remarks</span></span>

<span data-ttu-id="98eec-136">Per informazioni sulle restrizioni di denominazione dei canali virtuali, vedere [registrazione client del canale virtuale](virtual-channel-client-registration.md) .</span><span class="sxs-lookup"><span data-stu-id="98eec-136">Refer to [Virtual Channel Client Registration](virtual-channel-client-registration.md) for information about virtual channel naming restrictions.</span></span>

<span data-ttu-id="98eec-137">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="98eec-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="98eec-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98eec-138">Requirements</span></span>



| <span data-ttu-id="98eec-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="98eec-139">Requirement</span></span> | <span data-ttu-id="98eec-140">Valore</span><span class="sxs-lookup"><span data-stu-id="98eec-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98eec-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98eec-141">Minimum supported client</span></span><br/> | <span data-ttu-id="98eec-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98eec-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="98eec-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98eec-143">Minimum supported server</span></span><br/> | <span data-ttu-id="98eec-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98eec-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="98eec-145">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="98eec-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="98eec-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98eec-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="98eec-147">DLL</span><span class="sxs-lookup"><span data-stu-id="98eec-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98eec-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98eec-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="98eec-149">IID</span><span class="sxs-lookup"><span data-stu-id="98eec-149">IID</span></span><br/>                      | <span data-ttu-id="98eec-150">IID \_ IMsTscAx è definito come 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="98eec-150">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="98eec-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98eec-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98eec-152">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="98eec-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="98eec-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="98eec-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="98eec-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="98eec-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="98eec-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="98eec-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="98eec-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="98eec-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="98eec-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="98eec-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="98eec-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="98eec-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="98eec-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="98eec-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="98eec-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="98eec-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="98eec-161">**CreateVirtualChannels**</span><span class="sxs-lookup"><span data-stu-id="98eec-161">**CreateVirtualChannels**</span></span>](imstscax-createvirtualchannels.md)
</dt> <dt>

[<span data-ttu-id="98eec-162">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="98eec-162">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





