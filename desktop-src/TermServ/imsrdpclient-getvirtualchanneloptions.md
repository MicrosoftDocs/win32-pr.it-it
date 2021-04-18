---
title: Metodo IMsRdpClient GetVirtualChannelOptions
description: Recupera le opzioni impostate per un canale virtuale.
ms.assetid: d2ec9fb2-c0dc-49f1-a86b-d7abca13a322
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetVirtualChannelOptions
- Metodo GetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, metodo GetVirtualChannelOptions
- Metodo GetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, metodo GetVirtualChannelOptions
- Metodo GetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, metodo GetVirtualChannelOptions
- Metodo GetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, metodo GetVirtualChannelOptions
- Metodo GetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, metodo GetVirtualChannelOptions
- Metodo GetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, metodo GetVirtualChannelOptions
- Metodo GetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, metodo GetVirtualChannelOptions
- Metodo GetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, metodo GetVirtualChannelOptions
- Metodo GetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, metodo GetVirtualChannelOptions
- Metodo GetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, metodo GetVirtualChannelOptions
topic_type:
- apiref
api_name:
- IMsRdpClient.GetVirtualChannelOptions
- IMsRdpClient2.GetVirtualChannelOptions
- IMsRdpClient3.GetVirtualChannelOptions
- IMsRdpClient4.GetVirtualChannelOptions
- IMsRdpClient5.GetVirtualChannelOptions
- IMsRdpClient6.GetVirtualChannelOptions
- IMsRdpClient7.GetVirtualChannelOptions
- IMsRdpClient8.GetVirtualChannelOptions
- IMsRdpClient9.GetVirtualChannelOptions
- IMsRdpClient10.GetVirtualChannelOptions
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71548002ebc67dae8dc1a49e8144da3de608afb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302467"
---
# <a name="imsrdpclientgetvirtualchanneloptions-method"></a><span data-ttu-id="aeb08-124">Metodo IMsRdpClient:: GetVirtualChannelOptions</span><span class="sxs-lookup"><span data-stu-id="aeb08-124">IMsRdpClient::GetVirtualChannelOptions method</span></span>

<span data-ttu-id="aeb08-125">Recupera le opzioni impostate per un canale virtuale.</span><span class="sxs-lookup"><span data-stu-id="aeb08-125">Retrieves the options set for a virtual channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="aeb08-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aeb08-126">Syntax</span></span>


```C++
HRESULT GetVirtualChannelOptions(
  [in]  BSTR ChanName,
  [out] LONG *pChanOptions
);
```



## <a name="parameters"></a><span data-ttu-id="aeb08-127">Parametri</span><span class="sxs-lookup"><span data-stu-id="aeb08-127">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aeb08-128">*Channame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aeb08-128">*ChanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aeb08-129">Nome di un canale virtuale specificato nella chiamata al metodo [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) .</span><span class="sxs-lookup"><span data-stu-id="aeb08-129">The name of a virtual channel that was specified in the call to [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="aeb08-130">*pChanOptions* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="aeb08-130">*pChanOptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aeb08-131">Opzioni impostate per il canale virtuale specificato dal parametro *channame* .</span><span class="sxs-lookup"><span data-stu-id="aeb08-131">The options set for the virtual channel specified by the *ChanName* parameter.</span></span> <span data-ttu-id="aeb08-132">Per una descrizione delle possibili opzioni, vedere [**Channel \_ def**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).</span><span class="sxs-lookup"><span data-stu-id="aeb08-132">For a description of possible options, see [**CHANNEL\_DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aeb08-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aeb08-133">Return value</span></span>

<span data-ttu-id="aeb08-134">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="aeb08-134">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="aeb08-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="aeb08-135">Remarks</span></span>

<span data-ttu-id="aeb08-136">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="aeb08-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aeb08-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aeb08-137">Requirements</span></span>



| <span data-ttu-id="aeb08-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="aeb08-138">Requirement</span></span> | <span data-ttu-id="aeb08-139">Valore</span><span class="sxs-lookup"><span data-stu-id="aeb08-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aeb08-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aeb08-140">Minimum supported client</span></span><br/> | <span data-ttu-id="aeb08-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aeb08-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="aeb08-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aeb08-142">Minimum supported server</span></span><br/> | <span data-ttu-id="aeb08-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aeb08-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="aeb08-144">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="aeb08-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="aeb08-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aeb08-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="aeb08-146">DLL</span><span class="sxs-lookup"><span data-stu-id="aeb08-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aeb08-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aeb08-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="aeb08-148">IID</span><span class="sxs-lookup"><span data-stu-id="aeb08-148">IID</span></span><br/>                      | <span data-ttu-id="aeb08-149">IID \_ IMsRdpClient è definito come 92b4a539-7115-4B7C-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="aeb08-149">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="aeb08-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aeb08-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeb08-151">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="aeb08-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="aeb08-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="aeb08-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="aeb08-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="aeb08-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="aeb08-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="aeb08-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="aeb08-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="aeb08-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="aeb08-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="aeb08-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="aeb08-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="aeb08-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="aeb08-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="aeb08-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="aeb08-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="aeb08-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="aeb08-160">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="aeb08-160">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="aeb08-161">**\_def canale**</span><span class="sxs-lookup"><span data-stu-id="aeb08-161">**CHANNEL\_DEF**</span></span>](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[<span data-ttu-id="aeb08-162">**CreateVirtualChannels**</span><span class="sxs-lookup"><span data-stu-id="aeb08-162">**CreateVirtualChannels**</span></span>](imstscax-createvirtualchannels.md)
</dt> <dt>

[<span data-ttu-id="aeb08-163">**SetVirtualChannelOptions**</span><span class="sxs-lookup"><span data-stu-id="aeb08-163">**SetVirtualChannelOptions**</span></span>](imsrdpclient-setvirtualchanneloptions.md)
</dt> </dl>

 

 





