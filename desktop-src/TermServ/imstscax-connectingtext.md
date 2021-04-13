---
title: Proprietà ConnectingText di IMsTscAx
description: Specifica il testo visualizzato al centro del controllo mentre è in corso la connessione del controllo.
ms.assetid: 9bc82074-988f-491b-80e3-00c3f7ba437a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà ConnectingText
- Servizi Desktop remoto proprietà ConnectingText, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, proprietà ConnectingText
- Servizi Desktop remoto proprietà ConnectingText, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà ConnectingText
- Servizi Desktop remoto proprietà ConnectingText, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà ConnectingText
- Servizi Desktop remoto proprietà ConnectingText, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà ConnectingText
- Servizi Desktop remoto proprietà ConnectingText, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà ConnectingText
- Servizi Desktop remoto proprietà ConnectingText, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà ConnectingText
- Servizi Desktop remoto proprietà ConnectingText, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà ConnectingText
- Servizi Desktop remoto proprietà ConnectingText, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà ConnectingText
- Servizi Desktop remoto proprietà ConnectingText, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà ConnectingText
- Servizi Desktop remoto proprietà ConnectingText, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà ConnectingText
topic_type:
- apiref
api_name:
- IMsTscAx.ConnectingText
- IMsTscAx.get_ConnectingText
- IMsTscAx.put_ConnectingText
- IMsRdpClient.ConnectingText
- IMsRdpClient.get_ConnectingText
- IMsRdpClient.put_ConnectingText
- IMsRdpClient2.ConnectingText
- IMsRdpClient2.get_ConnectingText
- IMsRdpClient2.put_ConnectingText
- IMsRdpClient3.ConnectingText
- IMsRdpClient3.get_ConnectingText
- IMsRdpClient3.put_ConnectingText
- IMsRdpClient4.ConnectingText
- IMsRdpClient4.get_ConnectingText
- IMsRdpClient4.put_ConnectingText
- IMsRdpClient5.ConnectingText
- IMsRdpClient5.get_ConnectingText
- IMsRdpClient5.put_ConnectingText
- IMsRdpClient6.ConnectingText
- IMsRdpClient6.get_ConnectingText
- IMsRdpClient6.put_ConnectingText
- IMsRdpClient7.ConnectingText
- IMsRdpClient7.get_ConnectingText
- IMsRdpClient7.put_ConnectingText
- IMsRdpClient8.ConnectingText
- IMsRdpClient8.get_ConnectingText
- IMsRdpClient8.put_ConnectingText
- IMsRdpClient9.ConnectingText
- IMsRdpClient9.get_ConnectingText
- IMsRdpClient9.put_ConnectingText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 433da7d159f1fe5bf44114a0b76ed9b4d807046f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400785"
---
# <a name="imstscaxconnectingtext-property"></a><span data-ttu-id="75ab7-124">Proprietà IMsTscAx:: ConnectingText</span><span class="sxs-lookup"><span data-stu-id="75ab7-124">IMsTscAx::ConnectingText property</span></span>

<span data-ttu-id="75ab7-125">Specifica il testo visualizzato al centro del controllo mentre è in corso la connessione del controllo.</span><span class="sxs-lookup"><span data-stu-id="75ab7-125">Specifies the text that appears centered in the control while the control is connecting.</span></span>

<span data-ttu-id="75ab7-126">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="75ab7-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="75ab7-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="75ab7-127">Syntax</span></span>


```C++
HRESULT put_ConnectingText(
  [in]  BSTR newVal
);

HRESULT get_ConnectingText(
  [out] BSTR *pConnectingText
);
```



## <a name="property-value"></a><span data-ttu-id="75ab7-128">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="75ab7-128">Property value</span></span>

<span data-ttu-id="75ab7-129">Nuovo testo visualizzato.</span><span class="sxs-lookup"><span data-stu-id="75ab7-129">The new display text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="75ab7-130">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="75ab7-130">Error codes</span></span>

<span data-ttu-id="75ab7-131">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="75ab7-131">Return **S\_OK** if successful.</span></span>

<span data-ttu-id="75ab7-132">Restituisce un valore **HRESULT** diverso da zero se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="75ab7-132">Return a nonzero **HRESULT** if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="75ab7-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="75ab7-133">Remarks</span></span>

<span data-ttu-id="75ab7-134">Un esempio di testo della connessione è "connessione al server...".</span><span class="sxs-lookup"><span data-stu-id="75ab7-134">An example of connection text is "Connecting to server ...".</span></span>

<span data-ttu-id="75ab7-135">L'impostazione della proprietà **ConnectingText** è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="75ab7-135">Setting the **ConnectingText** property is optional.</span></span> <span data-ttu-id="75ab7-136">Se non è impostato, il controllo appare vuoto prima che venga stabilita una connessione.</span><span class="sxs-lookup"><span data-stu-id="75ab7-136">If it is not set, the control appears blank before a connection is established.</span></span>

<span data-ttu-id="75ab7-137">Questa proprietà può essere impostata solo se il controllo non è nello stato connesso.</span><span class="sxs-lookup"><span data-stu-id="75ab7-137">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="75ab7-138">Restituisce **e ha \_ esito negativo** se viene chiamato quando il controllo è connesso.</span><span class="sxs-lookup"><span data-stu-id="75ab7-138">It returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="75ab7-139">È possibile verificare se il controllo è connesso rispondendo agli eventi di connessione in [**IMsTscAxEvents**](imstscaxevents-interface.md) o esaminando la proprietà [**connessa**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="75ab7-139">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="75ab7-140">Il metodo della proprietà **get \_ ConnectingText** alloca la memoria necessaria per il buffer a cui punta il parametro *pConnectingText* .</span><span class="sxs-lookup"><span data-stu-id="75ab7-140">The **get\_ConnectingText** property method allocates the memory required for the buffer pointed to by the *pConnectingText* parameter.</span></span> <span data-ttu-id="75ab7-141">La chiamata di applicazioni C/C++ deve liberare la memoria con una chiamata alla funzione [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="75ab7-141">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="75ab7-142">Questa operazione non è necessaria per Visual Basic e client di scripting.</span><span class="sxs-lookup"><span data-stu-id="75ab7-142">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="75ab7-143">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="75ab7-143">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="75ab7-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75ab7-144">Requirements</span></span>



| <span data-ttu-id="75ab7-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="75ab7-145">Requirement</span></span> | <span data-ttu-id="75ab7-146">Valore</span><span class="sxs-lookup"><span data-stu-id="75ab7-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="75ab7-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75ab7-147">Minimum supported client</span></span><br/> | <span data-ttu-id="75ab7-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75ab7-148">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="75ab7-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75ab7-149">Minimum supported server</span></span><br/> | <span data-ttu-id="75ab7-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75ab7-150">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="75ab7-151">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="75ab7-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="75ab7-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75ab7-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="75ab7-153">DLL</span><span class="sxs-lookup"><span data-stu-id="75ab7-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75ab7-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75ab7-154"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="75ab7-155">IID</span><span class="sxs-lookup"><span data-stu-id="75ab7-155">IID</span></span><br/>                      | <span data-ttu-id="75ab7-156">IID \_ IMsTscAx è definito come 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="75ab7-156">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="75ab7-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75ab7-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75ab7-158">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="75ab7-158">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="75ab7-159">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="75ab7-159">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="75ab7-160">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="75ab7-160">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="75ab7-161">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="75ab7-161">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="75ab7-162">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="75ab7-162">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="75ab7-163">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="75ab7-163">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="75ab7-164">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="75ab7-164">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="75ab7-165">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="75ab7-165">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="75ab7-166">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="75ab7-166">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="75ab7-167">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="75ab7-167">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

