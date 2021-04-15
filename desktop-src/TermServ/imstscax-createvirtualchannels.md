---
title: Metodo IMsTscAx CreateVirtualChannels
description: Crea un oggetto canale virtuale sul lato client per ogni nome di canale virtuale specificato.
ms.assetid: 3afd2f1c-abd5-4f85-93fb-6d1173f09b07
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo CreateVirtualChannels
- Metodo CreateVirtualChannels Servizi Desktop remoto, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, metodo CreateVirtualChannels
- Metodo CreateVirtualChannels Servizi Desktop remoto, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, metodo CreateVirtualChannels
- Metodo CreateVirtualChannels Servizi Desktop remoto, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, metodo CreateVirtualChannels
- Metodo CreateVirtualChannels Servizi Desktop remoto, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, metodo CreateVirtualChannels
- Metodo CreateVirtualChannels Servizi Desktop remoto, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, metodo CreateVirtualChannels
- Metodo CreateVirtualChannels Servizi Desktop remoto, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, metodo CreateVirtualChannels
- Metodo CreateVirtualChannels Servizi Desktop remoto, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, metodo CreateVirtualChannels
- Metodo CreateVirtualChannels Servizi Desktop remoto, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, metodo CreateVirtualChannels
- Metodo CreateVirtualChannels Servizi Desktop remoto, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, metodo CreateVirtualChannels
- Metodo CreateVirtualChannels Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, metodo CreateVirtualChannels
topic_type:
- apiref
api_name:
- IMsTscAx.CreateVirtualChannels
- IMsRdpClient.CreateVirtualChannels
- IMsRdpClient2.CreateVirtualChannels
- IMsRdpClient3.CreateVirtualChannels
- IMsRdpClient4.CreateVirtualChannels
- IMsRdpClient5.CreateVirtualChannels
- IMsRdpClient6.CreateVirtualChannels
- IMsRdpClient7.CreateVirtualChannels
- IMsRdpClient8.CreateVirtualChannels
- IMsRdpClient9.CreateVirtualChannels
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d59c185763ddd3685e5e566f88e26a6aa6211b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477734"
---
# <a name="imstscaxcreatevirtualchannels-method"></a><span data-ttu-id="c4637-124">Metodo IMsTscAx:: CreateVirtualChannels</span><span class="sxs-lookup"><span data-stu-id="c4637-124">IMsTscAx::CreateVirtualChannels method</span></span>

<span data-ttu-id="c4637-125">Crea un oggetto canale virtuale sul lato client per ogni nome di canale virtuale specificato.</span><span class="sxs-lookup"><span data-stu-id="c4637-125">Creates a client-side virtual channel object for each specified virtual channel name.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4637-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4637-126">Syntax</span></span>


```C++
HRESULT CreateVirtualChannels(
  [in] BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="c4637-127">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4637-127">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4637-128">*newVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4637-128">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4637-129">Elenco delimitato da virgole di nomi di canale virtuali validi.</span><span class="sxs-lookup"><span data-stu-id="c4637-129">A comma-separated list of valid virtual channel names.</span></span> <span data-ttu-id="c4637-130">La lunghezza di ogni nome in questo elenco può essere costituita da un minimo di uno e un massimo di sette caratteri alfabetici.</span><span class="sxs-lookup"><span data-stu-id="c4637-130">The length of each name in this list can be a minimum of one and a maximum of seven alphabetical characters.</span></span> <span data-ttu-id="c4637-131">La lunghezza dell'intera stringa può essere un minimo di uno e un massimo di 300 caratteri alfabetici.</span><span class="sxs-lookup"><span data-stu-id="c4637-131">The length of the entire string can be a minimum of one and a maximum of 300 alphabetical characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4637-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c4637-132">Return value</span></span>

<span data-ttu-id="c4637-133">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c4637-133">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="c4637-134">Restituisce **E \_ INVALIDARG** se il parametro passato non soddisfa i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="c4637-134">Returns **E\_INVALIDARG** if the parameter that is passed does not meet the criteria that is specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4637-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4637-135">Remarks</span></span>

<span data-ttu-id="c4637-136">Chiamare questo metodo prima di chiamare il metodo [**Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="c4637-136">Call this method before calling the [**Connect**](imstscax-connect.md) method.</span></span>

<span data-ttu-id="c4637-137">Per informazioni sulle restrizioni di denominazione dei canali virtuali, vedere [registrazione client del canale virtuale](virtual-channel-client-registration.md) .</span><span class="sxs-lookup"><span data-stu-id="c4637-137">Refer to [Virtual Channel Client Registration](virtual-channel-client-registration.md) for information about virtual channel naming restrictions.</span></span>

<span data-ttu-id="c4637-138">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c4637-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4637-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4637-139">Requirements</span></span>



| <span data-ttu-id="c4637-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4637-140">Requirement</span></span> | <span data-ttu-id="c4637-141">Valore</span><span class="sxs-lookup"><span data-stu-id="c4637-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4637-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4637-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c4637-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4637-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c4637-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4637-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c4637-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4637-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c4637-146">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c4637-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="c4637-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4637-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c4637-148">DLL</span><span class="sxs-lookup"><span data-stu-id="c4637-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4637-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4637-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c4637-150">IID</span><span class="sxs-lookup"><span data-stu-id="c4637-150">IID</span></span><br/>                      | <span data-ttu-id="c4637-151">IID \_ IMsTscAx è definito come 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="c4637-151">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="c4637-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4637-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4637-153">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="c4637-153">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="c4637-154">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="c4637-154">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="c4637-155">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="c4637-155">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="c4637-156">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="c4637-156">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="c4637-157">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="c4637-157">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="c4637-158">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="c4637-158">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="c4637-159">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="c4637-159">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="c4637-160">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="c4637-160">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="c4637-161">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="c4637-161">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="c4637-162">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="c4637-162">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





