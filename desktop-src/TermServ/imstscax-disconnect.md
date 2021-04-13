---
title: Metodo di disconnessione IMsTscAx
description: Disconnette la connessione attiva.
ms.assetid: 9fcffd45-b293-4650-be8f-1b0d01d592a2
ms.tgt_platform: multiple
keywords:
- Disconnetti metodo Servizi Desktop remoto
- Metodo Disconnect Servizi Desktop remoto, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, metodo Disconnect
- Metodo Disconnect Servizi Desktop remoto, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, metodo Disconnect
- Metodo Disconnect Servizi Desktop remoto, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, metodo Disconnect
- Metodo Disconnect Servizi Desktop remoto, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, metodo Disconnect
- Metodo Disconnect Servizi Desktop remoto, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, metodo Disconnect
- Metodo Disconnect Servizi Desktop remoto, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, metodo Disconnect
- Metodo Disconnect Servizi Desktop remoto, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, metodo Disconnect
- Metodo Disconnect Servizi Desktop remoto, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, metodo Disconnect
- Metodo Disconnect Servizi Desktop remoto, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, metodo Disconnect
- Metodo Disconnect Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, metodo Disconnect
topic_type:
- apiref
api_name:
- IMsTscAx.Disconnect
- IMsRdpClient.Disconnect
- IMsRdpClient2.Disconnect
- IMsRdpClient3.Disconnect
- IMsRdpClient4.Disconnect
- IMsRdpClient5.Disconnect
- IMsRdpClient6.Disconnect
- IMsRdpClient7.Disconnect
- IMsRdpClient8.Disconnect
- IMsRdpClient9.Disconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4f1545a8244209c0b4fa8267fcc8ce2a41e090
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518178"
---
# <a name="imstscaxdisconnect-method"></a><span data-ttu-id="1c570-124">IMsTscAx::D metodo di connessione</span><span class="sxs-lookup"><span data-stu-id="1c570-124">IMsTscAx::Disconnect method</span></span>

<span data-ttu-id="1c570-125">Disconnette la connessione attiva.</span><span class="sxs-lookup"><span data-stu-id="1c570-125">Disconnects the active connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c570-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c570-126">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="1c570-127">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c570-127">Parameters</span></span>

<span data-ttu-id="1c570-128">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="1c570-128">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1c570-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c570-129">Return value</span></span>

<span data-ttu-id="1c570-130">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="1c570-130">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c570-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c570-131">Remarks</span></span>

<span data-ttu-id="1c570-132">Questo metodo restituisce un valore di errore errore se viene chiamato quando il controllo non è connesso.</span><span class="sxs-lookup"><span data-stu-id="1c570-132">This method returns a failure error value if it is called when the control is not connected.</span></span>

<span data-ttu-id="1c570-133">È anche possibile disconnettere il controllo chiudendo la finestra principale.</span><span class="sxs-lookup"><span data-stu-id="1c570-133">It is also possible to disconnect the control by closing its main window.</span></span> <span data-ttu-id="1c570-134">Se, ad esempio, il controllo è ospitato in una pagina Web, non è necessario chiamare questo metodo prima di uscire dalla pagina; la chiusura del controllo attiva una disconnessione.</span><span class="sxs-lookup"><span data-stu-id="1c570-134">For example, if the control is hosted in a webpage, it is not necessary to call this method before leaving the page; the closing of the control triggers a disconnection.</span></span>

<span data-ttu-id="1c570-135">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="1c570-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c570-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c570-136">Requirements</span></span>



| <span data-ttu-id="1c570-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c570-137">Requirement</span></span> | <span data-ttu-id="1c570-138">Valore</span><span class="sxs-lookup"><span data-stu-id="1c570-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c570-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c570-139">Minimum supported client</span></span><br/> | <span data-ttu-id="1c570-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c570-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1c570-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c570-141">Minimum supported server</span></span><br/> | <span data-ttu-id="1c570-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c570-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1c570-143">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="1c570-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="1c570-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c570-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1c570-145">DLL</span><span class="sxs-lookup"><span data-stu-id="1c570-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c570-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c570-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1c570-147">IID</span><span class="sxs-lookup"><span data-stu-id="1c570-147">IID</span></span><br/>                      | <span data-ttu-id="1c570-148">IID \_ IMsTscAx è definito come 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="1c570-148">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="1c570-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c570-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c570-150">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="1c570-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="1c570-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="1c570-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="1c570-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="1c570-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="1c570-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="1c570-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="1c570-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="1c570-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="1c570-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="1c570-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="1c570-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="1c570-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="1c570-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="1c570-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="1c570-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="1c570-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="1c570-159">**Connettersi**</span><span class="sxs-lookup"><span data-stu-id="1c570-159">**Connect**</span></span>](imstscax-connect.md)
</dt> <dt>

[<span data-ttu-id="1c570-160">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="1c570-160">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





