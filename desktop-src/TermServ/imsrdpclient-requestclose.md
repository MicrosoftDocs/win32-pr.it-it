---
title: Metodo IMsRdpClient RequestClose
description: Richiede un arresto normale del controllo ActiveX Desktop remoto.
ms.assetid: 0b930a00-f134-4da2-a752-8fd131a22043
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del Metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, Metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, Metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, Metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, Metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, Metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, Metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, Metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, Metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, Metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, Metodo RequestClose
topic_type:
- apiref
api_name:
- IMsRdpClient.RequestClose
- IMsRdpClient2.RequestClose
- IMsRdpClient3.RequestClose
- IMsRdpClient4.RequestClose
- IMsRdpClient5.RequestClose
- IMsRdpClient6.RequestClose
- IMsRdpClient7.RequestClose
- IMsRdpClient8.RequestClose
- IMsRdpClient9.RequestClose
- IMsRdpClient10.RequestClose
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1679b08680b962cdbff57e9bbbd1c392607d8709
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740575"
---
# <a name="imsrdpclientrequestclose-method"></a><span data-ttu-id="a8f7b-124">Metodo IMsRdpClient:: RequestClose</span><span class="sxs-lookup"><span data-stu-id="a8f7b-124">IMsRdpClient::RequestClose method</span></span>

<span data-ttu-id="a8f7b-125">Richiede un arresto normale del controllo ActiveX Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="a8f7b-125">Requests a graceful shutdown of the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="a8f7b-126">Un arresto normale può includere la chiusura della sessione di Servizi Desktop remoto dell'utente, ma non l'arresto del server di host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="a8f7b-126">A graceful shutdown can include ending the user's Remote Desktop Services session but it does not shut down the Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8f7b-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a8f7b-127">Syntax</span></span>


```C++
HRESULT RequestClose(
  [out] ControlCloseStatus *pCloseStatus
);
```



## <a name="parameters"></a><span data-ttu-id="a8f7b-128">Parametri</span><span class="sxs-lookup"><span data-stu-id="a8f7b-128">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8f7b-129">*pCloseStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a8f7b-129">*pCloseStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8f7b-130">Valore dell'enumerazione [**ControlCloseStatus**](controlclosestatus.md) che indica se l'applicazione può chiudere immediatamente il controllo.</span><span class="sxs-lookup"><span data-stu-id="a8f7b-130">Value from the [**ControlCloseStatus**](controlclosestatus.md) enumeration that indicates whether the application can close the control immediately.</span></span> <span data-ttu-id="a8f7b-131">Di seguito è riportato un elenco di valori possibili.</span><span class="sxs-lookup"><span data-stu-id="a8f7b-131">Following is a list of possible values.</span></span>

<dt>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>

<span data-ttu-id="a8f7b-132"><span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed** (0x0000)</span><span class="sxs-lookup"><span data-stu-id="a8f7b-132"><span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed** (0x0000)</span></span>


</dt> <dd>

<span data-ttu-id="a8f7b-133">L'applicazione contenitore può procedere immediatamente alla chiusura del controllo.</span><span class="sxs-lookup"><span data-stu-id="a8f7b-133">The container application can proceed to close the control immediately.</span></span> <span data-ttu-id="a8f7b-134">Questo valore può anche indicare che la connessione è già stata terminata.</span><span class="sxs-lookup"><span data-stu-id="a8f7b-134">This value can also indicate that the connection has already terminated.</span></span>

</dd> <dt>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>

<span data-ttu-id="a8f7b-135"><span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="a8f7b-135"><span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents** (0x0001)</span></span>


</dt> <dd>

<span data-ttu-id="a8f7b-136">Il controllo non deve essere chiuso immediatamente dall'applicazione contenitore; l'applicazione deve attendere che uno degli eventi descritti nella sezione Osservazioni seguente venga eseguito prima della chiusura.</span><span class="sxs-lookup"><span data-stu-id="a8f7b-136">The container application should not close the control immediately; the application should wait for one of the events described in the following Remarks section to occur before closing.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8f7b-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a8f7b-137">Return value</span></span>

<span data-ttu-id="a8f7b-138">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="a8f7b-138">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8f7b-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8f7b-139">Remarks</span></span>

<span data-ttu-id="a8f7b-140">Se il parametro *pCloseStatus* è uguale a **controlCloseWaitForEvents**, l'applicazione deve attendere che si verifichi uno degli eventi seguenti prima che l'applicazione chiuda il controllo:</span><span class="sxs-lookup"><span data-stu-id="a8f7b-140">If the *pCloseStatus* parameter is equal to **controlCloseWaitForEvents**, the application should wait for one of the following events to occur before the application closes the control:</span></span>

-   <span data-ttu-id="a8f7b-141">[**IMsTscAxEvents:: disconnected**](imstscaxevents-ondisconnected.md).</span><span class="sxs-lookup"><span data-stu-id="a8f7b-141">[**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md).</span></span> <span data-ttu-id="a8f7b-142">Se l'utente non è connesso alla sessione di Servizi Desktop remoto, l'applicazione può chiamare la funzione [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) per eliminare definitivamente tutte le finestre e quindi chiudere il controllo.</span><span class="sxs-lookup"><span data-stu-id="a8f7b-142">If the user is not logged on to the Remote Desktop Services session, the application can call the [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) function to destroy all windows and then close the control.</span></span>
-   <span data-ttu-id="a8f7b-143">[**IMsTscAxEvents:: OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span><span class="sxs-lookup"><span data-stu-id="a8f7b-143">[**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span></span> <span data-ttu-id="a8f7b-144">Se l'utente è connesso alla sessione di Servizi Desktop remoto, il controllo genera un evento **OnConfirmClose** .</span><span class="sxs-lookup"><span data-stu-id="a8f7b-144">If the user is logged on to the Remote Desktop Services session, the control fires an **OnConfirmClose** event.</span></span> <span data-ttu-id="a8f7b-145">Questo evento consente all'applicazione di richiedere all'utente se chiudere la connessione.</span><span class="sxs-lookup"><span data-stu-id="a8f7b-145">This event allows the application to prompt the user about whether to close the connection.</span></span> <span data-ttu-id="a8f7b-146">Se l'utente risponde Sì al prompt, l'applicazione contenitore può chiamare [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) per eliminare tutte le finestre e chiudere il controllo.</span><span class="sxs-lookup"><span data-stu-id="a8f7b-146">If the user replies yes to the prompt, the container application can call [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) to destroy all windows, and close the control.</span></span>

<span data-ttu-id="a8f7b-147">**RequestClose** consente a un'applicazione contenitore di richiedere all'utente se chiudere una connessione.</span><span class="sxs-lookup"><span data-stu-id="a8f7b-147">**RequestClose** allows a container application to prompt the user about whether to close a connection.</span></span> <span data-ttu-id="a8f7b-148">Per ulteriori informazioni, vedere [**IMsTscAxEvents:: OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span><span class="sxs-lookup"><span data-stu-id="a8f7b-148">For more information, see [**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span></span>

<span data-ttu-id="a8f7b-149">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a8f7b-149">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8f7b-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8f7b-150">Requirements</span></span>



| <span data-ttu-id="a8f7b-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8f7b-151">Requirement</span></span> | <span data-ttu-id="a8f7b-152">Valore</span><span class="sxs-lookup"><span data-stu-id="a8f7b-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8f7b-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8f7b-153">Minimum supported client</span></span><br/> | <span data-ttu-id="a8f7b-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8f7b-154">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a8f7b-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8f7b-155">Minimum supported server</span></span><br/> | <span data-ttu-id="a8f7b-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8f7b-156">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a8f7b-157">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a8f7b-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="a8f7b-158"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8f7b-158"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a8f7b-159">DLL</span><span class="sxs-lookup"><span data-stu-id="a8f7b-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8f7b-160"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8f7b-160"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a8f7b-161">IID</span><span class="sxs-lookup"><span data-stu-id="a8f7b-161">IID</span></span><br/>                      | <span data-ttu-id="a8f7b-162">IID \_ IMsRdpClient è definito come 92b4a539-7115-4B7C-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="a8f7b-162">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="a8f7b-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8f7b-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8f7b-164">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="a8f7b-164">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="a8f7b-165">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="a8f7b-165">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="a8f7b-166">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="a8f7b-166">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="a8f7b-167">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="a8f7b-167">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="a8f7b-168">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="a8f7b-168">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="a8f7b-169">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="a8f7b-169">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="a8f7b-170">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="a8f7b-170">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="a8f7b-171">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="a8f7b-171">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="a8f7b-172">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="a8f7b-172">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="a8f7b-173">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="a8f7b-173">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="a8f7b-174">**IMsTscAxEvents::OnConfirmClose**</span><span class="sxs-lookup"><span data-stu-id="a8f7b-174">**IMsTscAxEvents::OnConfirmClose**</span></span>](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[<span data-ttu-id="a8f7b-175">**IMsTscAxEvents:: disconnected**</span><span class="sxs-lookup"><span data-stu-id="a8f7b-175">**IMsTscAxEvents::OnDisconnected**</span></span>](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

