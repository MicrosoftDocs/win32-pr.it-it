---
title: Metodo di connessione IMsTscAx
description: Avvia una connessione utilizzando le proprietà attualmente impostate nel controllo.
ms.assetid: 9bcbdc13-6c66-4737-82a4-98329f173743
ms.tgt_platform: multiple
keywords:
- Metodo Connect Servizi Desktop remoto
- Metodo Connect Servizi Desktop remoto, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, metodo Connect
- Metodo Connect Servizi Desktop remoto, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, metodo Connect
- Metodo Connect Servizi Desktop remoto, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, metodo Connect
- Metodo Connect Servizi Desktop remoto, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, metodo Connect
- Metodo Connect Servizi Desktop remoto, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, metodo Connect
- Metodo Connect Servizi Desktop remoto, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, metodo Connect
- Metodo Connect Servizi Desktop remoto, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, metodo Connect
- Metodo Connect Servizi Desktop remoto, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, metodo Connect
- Metodo Connect Servizi Desktop remoto, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, metodo Connect
- Metodo Connect Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, metodo Connect
topic_type:
- apiref
api_name:
- IMsTscAx.Connect
- IMsRdpClient.Connect
- IMsRdpClient2.Connect
- IMsRdpClient3.Connect
- IMsRdpClient4.Connect
- IMsRdpClient5.Connect
- IMsRdpClient6.Connect
- IMsRdpClient7.Connect
- IMsRdpClient8.Connect
- IMsRdpClient9.Connect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c267b24c3dd27dd875d895674d98e1350f757c82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963965"
---
# <a name="imstscaxconnect-method"></a><span data-ttu-id="f5b7a-124">Metodo IMsTscAx:: Connect</span><span class="sxs-lookup"><span data-stu-id="f5b7a-124">IMsTscAx::Connect method</span></span>

<span data-ttu-id="f5b7a-125">Avvia una connessione utilizzando le proprietà attualmente impostate nel controllo.</span><span class="sxs-lookup"><span data-stu-id="f5b7a-125">Initiates a connection using the properties currently set on the control.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5b7a-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5b7a-126">Syntax</span></span>


```C++
HRESULT Connect();
```



## <a name="parameters"></a><span data-ttu-id="f5b7a-127">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5b7a-127">Parameters</span></span>

<span data-ttu-id="f5b7a-128">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f5b7a-128">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f5b7a-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5b7a-129">Return value</span></span>

<span data-ttu-id="f5b7a-130">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="f5b7a-130">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5b7a-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5b7a-131">Remarks</span></span>

<span data-ttu-id="f5b7a-132">L'unica proprietà obbligatoria è il nome del server.</span><span class="sxs-lookup"><span data-stu-id="f5b7a-132">The only required property is the server name.</span></span> <span data-ttu-id="f5b7a-133">Fare riferimento alla proprietà [**Server**](imstscax-server.md) .</span><span class="sxs-lookup"><span data-stu-id="f5b7a-133">Refer to the [**Server**](imstscax-server.md) property.</span></span>

<span data-ttu-id="f5b7a-134">Il controllo si connette in modo asincrono, quindi un ritorno da una chiamata Connect indica solo che la connessione è stata avviata correttamente, non che è stata completata.</span><span class="sxs-lookup"><span data-stu-id="f5b7a-134">The control connects asynchronously, so a return from a Connect call indicates only that the connection has been initiated successfully, not that it has been completed.</span></span> <span data-ttu-id="f5b7a-135">È necessario rispondere agli eventi sull'interfaccia [**IMsTscAxEvents**](imstscaxevents-interface.md) per determinare quando il controllo è stato connesso correttamente o è stato disconnesso.</span><span class="sxs-lookup"><span data-stu-id="f5b7a-135">You should respond to events on the [**IMsTscAxEvents**](imstscaxevents-interface.md) interface to determine when the control has successfully connected (or has been disconnected.)</span></span>

<span data-ttu-id="f5b7a-136">Questo metodo restituisce **E ha \_ esito negativo** se viene chiamato quando il controllo è già connesso o nello stato di connessione.</span><span class="sxs-lookup"><span data-stu-id="f5b7a-136">This method returns **E\_FAIL** if it is called while the control is already connected or in the connecting state.</span></span>

<span data-ttu-id="f5b7a-137">Una volta chiamata la **connessione** , la maggior parte delle proprietà del controllo non può più essere impostata finché il controllo non torna allo stato disconnesso.</span><span class="sxs-lookup"><span data-stu-id="f5b7a-137">After **Connect** has been called, most of the control properties can no longer be set until the control returns to the disconnected state.</span></span>

<span data-ttu-id="f5b7a-138">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f5b7a-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5b7a-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5b7a-139">Requirements</span></span>



| <span data-ttu-id="f5b7a-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5b7a-140">Requirement</span></span> | <span data-ttu-id="f5b7a-141">Valore</span><span class="sxs-lookup"><span data-stu-id="f5b7a-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b7a-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5b7a-142">Minimum supported client</span></span><br/> | <span data-ttu-id="f5b7a-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5b7a-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f5b7a-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5b7a-144">Minimum supported server</span></span><br/> | <span data-ttu-id="f5b7a-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5b7a-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f5b7a-146">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f5b7a-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="f5b7a-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5b7a-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f5b7a-148">DLL</span><span class="sxs-lookup"><span data-stu-id="f5b7a-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5b7a-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5b7a-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f5b7a-150">IID</span><span class="sxs-lookup"><span data-stu-id="f5b7a-150">IID</span></span><br/>                      | <span data-ttu-id="f5b7a-151">IID \_ IMsTscAx è definito come 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="f5b7a-151">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="f5b7a-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5b7a-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5b7a-153">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="f5b7a-153">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="f5b7a-154">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="f5b7a-154">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="f5b7a-155">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="f5b7a-155">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="f5b7a-156">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="f5b7a-156">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="f5b7a-157">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="f5b7a-157">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="f5b7a-158">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="f5b7a-158">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="f5b7a-159">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="f5b7a-159">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="f5b7a-160">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="f5b7a-160">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="f5b7a-161">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="f5b7a-161">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="f5b7a-162">**Disconnetti**</span><span class="sxs-lookup"><span data-stu-id="f5b7a-162">**Disconnect**</span></span>](imstscax-disconnect.md)
</dt> <dt>

[<span data-ttu-id="f5b7a-163">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="f5b7a-163">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





