---
title: Metodo IMsRdpClient SetVirtualChannelOptions
description: Imposta le opzioni del canale virtuale per il controllo ActiveX Desktop remoto.
ms.assetid: c74c3917-5766-4d5b-8458-b051eb91cb28
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, metodo SetVirtualChannelOptions
topic_type:
- apiref
api_name:
- IMsRdpClient.SetVirtualChannelOptions
- IMsRdpClient2.SetVirtualChannelOptions
- IMsRdpClient3.SetVirtualChannelOptions
- IMsRdpClient4.SetVirtualChannelOptions
- IMsRdpClient5.SetVirtualChannelOptions
- IMsRdpClient6.SetVirtualChannelOptions
- IMsRdpClient7.SetVirtualChannelOptions
- IMsRdpClient8.SetVirtualChannelOptions
- IMsRdpClient9.SetVirtualChannelOptions
- IMsRdpClient10.SetVirtualChannelOptions
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10e727fd3486b9d1b31fb3a421ea6ff268949790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400396"
---
# <a name="imsrdpclientsetvirtualchanneloptions-method"></a><span data-ttu-id="b5cc0-124">Metodo IMsRdpClient:: SetVirtualChannelOptions</span><span class="sxs-lookup"><span data-stu-id="b5cc0-124">IMsRdpClient::SetVirtualChannelOptions method</span></span>

<span data-ttu-id="b5cc0-125">Imposta le opzioni del canale virtuale per il controllo ActiveX Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="b5cc0-125">Sets the virtual channel options for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="b5cc0-126">Chiamare questo metodo dopo avere chiamato il metodo [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) , ma prima di stabilire una connessione con il metodo [**Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="b5cc0-126">Call this method after calling the [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method, but before establishing a connection with the [**Connect**](imstscax-connect.md) method.</span></span> <span data-ttu-id="b5cc0-127">Questo metodo consente di impostare opzioni aggiuntive nei canali virtuali creati con **CreateVirtualChannels**.</span><span class="sxs-lookup"><span data-stu-id="b5cc0-127">This method sets additional options on virtual channels that have been created with **CreateVirtualChannels**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5cc0-128">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5cc0-128">Syntax</span></span>


```C++
HRESULT SetVirtualChannelOptions(
  [in] BSTR ChanName,
  [in] LONG chanOptions
);
```



## <a name="parameters"></a><span data-ttu-id="b5cc0-129">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5cc0-129">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5cc0-130">*Channame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5cc0-130">*ChanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5cc0-131">Nome del canale virtuale specificato nella chiamata al metodo [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) .</span><span class="sxs-lookup"><span data-stu-id="b5cc0-131">The name of the virtual channel that was specified in the call to the [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="b5cc0-132">*chanOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5cc0-132">*chanOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5cc0-133">Opzioni da impostare per il canale virtuale specificato dal parametro *channame* .</span><span class="sxs-lookup"><span data-stu-id="b5cc0-133">The options to set for the virtual channel specified by the *ChanName* parameter.</span></span> <span data-ttu-id="b5cc0-134">Per una descrizione delle possibili opzioni, vedere [**Channel \_ def**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).</span><span class="sxs-lookup"><span data-stu-id="b5cc0-134">For a description of possible options, see [**CHANNEL\_DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).</span></span> <span data-ttu-id="b5cc0-135">Per ulteriori informazioni, vedere la sezione Osservazioni successiva.</span><span class="sxs-lookup"><span data-stu-id="b5cc0-135">For more information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5cc0-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5cc0-136">Return value</span></span>

<span data-ttu-id="b5cc0-137">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="b5cc0-137">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5cc0-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5cc0-138">Remarks</span></span>

<span data-ttu-id="b5cc0-139">Un esempio di utilizzo di questo metodo consiste nel dichiarare il canale come controllo remoto persistente impostando il flag **\_ \_ \_ \_ permanente controllo remoto opzioni canale** .</span><span class="sxs-lookup"><span data-stu-id="b5cc0-139">An example of using this method would be to declare the channel as remote control persistent by setting the **CHANNEL\_OPTION\_REMOTE\_CONTROL\_PERSISTENT** flag.</span></span> <span data-ttu-id="b5cc0-140">Ciò significa che il canale non verrà chiuso quando un controllo remoto si connette o si disconnette dalla sessione connessa al client.</span><span class="sxs-lookup"><span data-stu-id="b5cc0-140">This means that the channel would not be closed when a remote control connects to or disconnects from the session connected to the client.</span></span> <span data-ttu-id="b5cc0-141">Per ulteriori informazioni, vedere la pagina relativa ai [canali virtuali persistenti del controllo remoto](remote-control-persistent-virtual-channels.md).</span><span class="sxs-lookup"><span data-stu-id="b5cc0-141">For more information, see [Remote Control Persistent Virtual Channels](remote-control-persistent-virtual-channels.md).</span></span>

<span data-ttu-id="b5cc0-142">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="b5cc0-142">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5cc0-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5cc0-143">Requirements</span></span>



| <span data-ttu-id="b5cc0-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5cc0-144">Requirement</span></span> | <span data-ttu-id="b5cc0-145">Valore</span><span class="sxs-lookup"><span data-stu-id="b5cc0-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5cc0-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5cc0-146">Minimum supported client</span></span><br/> | <span data-ttu-id="b5cc0-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5cc0-147">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b5cc0-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5cc0-148">Minimum supported server</span></span><br/> | <span data-ttu-id="b5cc0-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5cc0-149">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b5cc0-150">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="b5cc0-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="b5cc0-151"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5cc0-151"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b5cc0-152">DLL</span><span class="sxs-lookup"><span data-stu-id="b5cc0-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5cc0-153"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5cc0-153"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b5cc0-154">IID</span><span class="sxs-lookup"><span data-stu-id="b5cc0-154">IID</span></span><br/>                      | <span data-ttu-id="b5cc0-155">IID \_ IMsRdpClient è definito come 92b4a539-7115-4B7C-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="b5cc0-155">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="b5cc0-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5cc0-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5cc0-157">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="b5cc0-157">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="b5cc0-158">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="b5cc0-158">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="b5cc0-159">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="b5cc0-159">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="b5cc0-160">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="b5cc0-160">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="b5cc0-161">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="b5cc0-161">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="b5cc0-162">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="b5cc0-162">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="b5cc0-163">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="b5cc0-163">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="b5cc0-164">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="b5cc0-164">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="b5cc0-165">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="b5cc0-165">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="b5cc0-166">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="b5cc0-166">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="b5cc0-167">**\_def canale**</span><span class="sxs-lookup"><span data-stu-id="b5cc0-167">**CHANNEL\_DEF**</span></span>](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[<span data-ttu-id="b5cc0-168">**CreateVirtualChannels**</span><span class="sxs-lookup"><span data-stu-id="b5cc0-168">**CreateVirtualChannels**</span></span>](imstscax-createvirtualchannels.md)
</dt> <dt>

[<span data-ttu-id="b5cc0-169">**GetVirtualChannelOptions**</span><span class="sxs-lookup"><span data-stu-id="b5cc0-169">**GetVirtualChannelOptions**</span></span>](imsrdpclient-getvirtualchanneloptions.md)
</dt> </dl>

 

 





