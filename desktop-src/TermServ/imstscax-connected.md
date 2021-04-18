---
title: Proprietà connessa IMsTscAx (Tsvirtualchannels. h)
description: Recupera lo stato di connessione del controllo corrente.
ms.assetid: f6f65ef6-d321-4362-b192-1ea5ffd2b712
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto di proprietà connesse
- Servizi Desktop remoto di proprietà connesse, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, proprietà connessa
- Servizi Desktop remoto di proprietà connesse, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà connessa
- Servizi Desktop remoto di proprietà connesse, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà connessa
- Servizi Desktop remoto di proprietà connesse, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà connessa
- Servizi Desktop remoto di proprietà connesse, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà connessa
- Servizi Desktop remoto di proprietà connesse, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà connessa
- Servizi Desktop remoto di proprietà connesse, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà connessa
- Servizi Desktop remoto di proprietà connesse, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà connessa
- Servizi Desktop remoto di proprietà connesse, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà connessa
- Servizi Desktop remoto di proprietà connesse, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà connessa
topic_type:
- apiref
api_name:
- IMsTscAx.Connected
- IMsTscAx.get_Connected
- IMsRdpClient.Connected
- IMsRdpClient.get_Connected
- IMsRdpClient2.Connected
- IMsRdpClient2.get_Connected
- IMsRdpClient3.Connected
- IMsRdpClient3.get_Connected
- IMsRdpClient4.Connected
- IMsRdpClient4.get_Connected
- IMsRdpClient5.Connected
- IMsRdpClient5.get_Connected
- IMsRdpClient6.Connected
- IMsRdpClient6.get_Connected
- IMsRdpClient7.Connected
- IMsRdpClient7.get_Connected
- IMsRdpClient8.Connected
- IMsRdpClient8.get_Connected
- IMsRdpClient9.Connected
- IMsRdpClient9.get_Connected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 883ba670ab9a6b5d4e4a065c35f263734929ba02
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302740"
---
# <a name="imstscaxconnected-property"></a><span data-ttu-id="b7b5f-124">Proprietà IMsTscAx:: Connected</span><span class="sxs-lookup"><span data-stu-id="b7b5f-124">IMsTscAx::Connected property</span></span>

<span data-ttu-id="b7b5f-125">Recupera lo stato di connessione del controllo corrente.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-125">Retrieves the connection state of the current control.</span></span>

<span data-ttu-id="b7b5f-126">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7b5f-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7b5f-127">Syntax</span></span>


```C++
HRESULT get_Connected(
  [out] short *pIsConnected
);
```



## <a name="property-value"></a><span data-ttu-id="b7b5f-128">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b7b5f-128">Property value</span></span>

<span data-ttu-id="b7b5f-129">Indica lo stato di connessione del controllo.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-129">Indicates the connection state of the control.</span></span> <span data-ttu-id="b7b5f-130">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-130">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="b7b5f-131">0</span><span class="sxs-lookup"><span data-stu-id="b7b5f-131">0</span></span>
</dt> <dd>

<span data-ttu-id="b7b5f-132">Il controllo non è connesso.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-132">The control is not connected.</span></span>

</dd> <dt>

<span data-ttu-id="b7b5f-133">1</span><span class="sxs-lookup"><span data-stu-id="b7b5f-133">1</span></span>
</dt> <dd>

<span data-ttu-id="b7b5f-134">Il controllo è connesso.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-134">The control is connected.</span></span>

</dd> <dt>

<span data-ttu-id="b7b5f-135">2</span><span class="sxs-lookup"><span data-stu-id="b7b5f-135">2</span></span>
</dt> <dd>

<span data-ttu-id="b7b5f-136">Il controllo sta stabilendo una connessione.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-136">The control is establishing a connection.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="b7b5f-137">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="b7b5f-137">Error codes</span></span>

<span data-ttu-id="b7b5f-138">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="b7b5f-138">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7b5f-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="b7b5f-139">Remarks</span></span>

<span data-ttu-id="b7b5f-140">Il modo migliore per determinare lo stato di connessione del controllo consiste nel rispondere agli eventi di connessione in [**IMsTscAxEvents**](imstscaxevents-interface.md).</span><span class="sxs-lookup"><span data-stu-id="b7b5f-140">The preferred way to determine the control's connection state is to respond to the connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md).</span></span>

<span data-ttu-id="b7b5f-141">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="b7b5f-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7b5f-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7b5f-142">Requirements</span></span>



| <span data-ttu-id="b7b5f-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7b5f-143">Requirement</span></span> | <span data-ttu-id="b7b5f-144">Valore</span><span class="sxs-lookup"><span data-stu-id="b7b5f-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7b5f-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7b5f-145">Minimum supported client</span></span><br/> | <span data-ttu-id="b7b5f-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7b5f-146">Windows Vista</span></span><br/>                                                                       |
| <span data-ttu-id="b7b5f-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7b5f-147">Minimum supported server</span></span><br/> | <span data-ttu-id="b7b5f-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7b5f-148">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="b7b5f-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7b5f-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7b5f-150"><dt>Tsvirtualchannels. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7b5f-150"><dt>Tsvirtualchannels.h</dt></span></span> </dl> |
| <span data-ttu-id="b7b5f-151">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="b7b5f-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="b7b5f-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7b5f-152"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="b7b5f-153">DLL</span><span class="sxs-lookup"><span data-stu-id="b7b5f-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7b5f-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7b5f-154"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="b7b5f-155">IID</span><span class="sxs-lookup"><span data-stu-id="b7b5f-155">IID</span></span><br/>                      | <span data-ttu-id="b7b5f-156">IID \_ IMsTscAx è definito come 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="b7b5f-156">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="b7b5f-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7b5f-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7b5f-158">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="b7b5f-158">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="b7b5f-159">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="b7b5f-159">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="b7b5f-160">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="b7b5f-160">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="b7b5f-161">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="b7b5f-161">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="b7b5f-162">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="b7b5f-162">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="b7b5f-163">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="b7b5f-163">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="b7b5f-164">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="b7b5f-164">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="b7b5f-165">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="b7b5f-165">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="b7b5f-166">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="b7b5f-166">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="b7b5f-167">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="b7b5f-167">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





