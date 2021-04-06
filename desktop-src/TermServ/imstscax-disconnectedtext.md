---
title: Proprietà DisconnectedText di IMsTscAx
description: Specifica il testo visualizzato al centro del controllo prima che venga terminata una connessione.
ms.assetid: ec7efe7a-8fb9-4c45-8e16-78951365de13
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà DisconnectedText
- Servizi Desktop remoto proprietà DisconnectedText, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, proprietà DisconnectedText
- Servizi Desktop remoto proprietà DisconnectedText, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà DisconnectedText
- Servizi Desktop remoto proprietà DisconnectedText, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà DisconnectedText
- Servizi Desktop remoto proprietà DisconnectedText, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà DisconnectedText
- Servizi Desktop remoto proprietà DisconnectedText, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà DisconnectedText
- Servizi Desktop remoto proprietà DisconnectedText, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà DisconnectedText
- Servizi Desktop remoto proprietà DisconnectedText, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà DisconnectedText
- Servizi Desktop remoto proprietà DisconnectedText, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà DisconnectedText
- Servizi Desktop remoto proprietà DisconnectedText, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà DisconnectedText
- Servizi Desktop remoto proprietà DisconnectedText, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà DisconnectedText
topic_type:
- apiref
api_name:
- IMsTscAx.DisconnectedText
- IMsTscAx.get_DisconnectedText
- IMsTscAx.put_DisconnectedText
- IMsRdpClient.DisconnectedText
- IMsRdpClient.get_DisconnectedText
- IMsRdpClient.put_DisconnectedText
- IMsRdpClient2.DisconnectedText
- IMsRdpClient2.get_DisconnectedText
- IMsRdpClient2.put_DisconnectedText
- IMsRdpClient3.DisconnectedText
- IMsRdpClient3.get_DisconnectedText
- IMsRdpClient3.put_DisconnectedText
- IMsRdpClient4.DisconnectedText
- IMsRdpClient4.get_DisconnectedText
- IMsRdpClient4.put_DisconnectedText
- IMsRdpClient5.DisconnectedText
- IMsRdpClient5.get_DisconnectedText
- IMsRdpClient5.put_DisconnectedText
- IMsRdpClient6.DisconnectedText
- IMsRdpClient6.get_DisconnectedText
- IMsRdpClient6.put_DisconnectedText
- IMsRdpClient7.DisconnectedText
- IMsRdpClient7.get_DisconnectedText
- IMsRdpClient7.put_DisconnectedText
- IMsRdpClient8.DisconnectedText
- IMsRdpClient8.get_DisconnectedText
- IMsRdpClient8.put_DisconnectedText
- IMsRdpClient9.DisconnectedText
- IMsRdpClient9.get_DisconnectedText
- IMsRdpClient9.put_DisconnectedText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4768e639cbfb1543e06c03f2d9e6566d0adb147e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742127"
---
# <a name="imstscaxdisconnectedtext-property"></a><span data-ttu-id="339d5-124">IMsTscAx::D Proprietà isconnectedText</span><span class="sxs-lookup"><span data-stu-id="339d5-124">IMsTscAx::DisconnectedText property</span></span>

<span data-ttu-id="339d5-125">Specifica il testo visualizzato al centro del controllo prima che venga terminata una connessione.</span><span class="sxs-lookup"><span data-stu-id="339d5-125">Specifies the text that appears centered in the control before a connection is terminated.</span></span>

<span data-ttu-id="339d5-126">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="339d5-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="339d5-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="339d5-127">Syntax</span></span>


```C++
HRESULT put_DisconnectedText(
  [in]  BSTR newVal
);

HRESULT get_DisconnectedText(
  [out] BSTR *pDisconnectedText
);
```



## <a name="property-value"></a><span data-ttu-id="339d5-128">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="339d5-128">Property value</span></span>

<span data-ttu-id="339d5-129">Nuovo testo visualizzato.</span><span class="sxs-lookup"><span data-stu-id="339d5-129">The new display text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="339d5-130">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="339d5-130">Error codes</span></span>

<span data-ttu-id="339d5-131">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="339d5-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="339d5-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="339d5-132">Remarks</span></span>

<span data-ttu-id="339d5-133">L'impostazione della proprietà **DisconnectedText** è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="339d5-133">Setting the **DisconnectedText** property is optional.</span></span> <span data-ttu-id="339d5-134">Se non viene specificato, il controllo appare vuoto prima che venga stabilita una connessione.</span><span class="sxs-lookup"><span data-stu-id="339d5-134">If it is not specified the control appears blank before a connection is established.</span></span>

<span data-ttu-id="339d5-135">Questa proprietà può essere impostata solo se il controllo non è nello stato connesso.</span><span class="sxs-lookup"><span data-stu-id="339d5-135">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="339d5-136">Il metodo restituisce **E ha \_ esito negativo** se viene chiamato dopo la connessione del controllo.</span><span class="sxs-lookup"><span data-stu-id="339d5-136">The method returns **E\_FAIL** if it is called after the control is connected.</span></span> <span data-ttu-id="339d5-137">È possibile verificare se il controllo è connesso rispondendo agli eventi di connessione in [**IMsTscAxEvents**](imstscaxevents-interface.md) o esaminando la proprietà [**connessa**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="339d5-137">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="339d5-138">Questo metodo alloca la memoria necessaria per il buffer a cui punta il parametro *pDisconnectedText* .</span><span class="sxs-lookup"><span data-stu-id="339d5-138">This method allocates the memory required for the buffer pointed to by the *pDisconnectedText* parameter.</span></span> <span data-ttu-id="339d5-139">La chiamata di applicazioni C/C++ deve liberare la memoria con una chiamata alla funzione [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="339d5-139">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="339d5-140">Questa operazione non è necessaria per Visual Basic e client di scripting.</span><span class="sxs-lookup"><span data-stu-id="339d5-140">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="339d5-141">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="339d5-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="339d5-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="339d5-142">Requirements</span></span>



| <span data-ttu-id="339d5-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="339d5-143">Requirement</span></span> | <span data-ttu-id="339d5-144">Valore</span><span class="sxs-lookup"><span data-stu-id="339d5-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="339d5-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="339d5-145">Minimum supported client</span></span><br/> | <span data-ttu-id="339d5-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="339d5-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="339d5-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="339d5-147">Minimum supported server</span></span><br/> | <span data-ttu-id="339d5-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="339d5-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="339d5-149">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="339d5-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="339d5-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="339d5-150"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="339d5-151">DLL</span><span class="sxs-lookup"><span data-stu-id="339d5-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="339d5-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="339d5-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="339d5-153">IID</span><span class="sxs-lookup"><span data-stu-id="339d5-153">IID</span></span><br/>                      | <span data-ttu-id="339d5-154">IID \_ IMsTscAx è definito come 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="339d5-154">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="339d5-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="339d5-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="339d5-156">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="339d5-156">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="339d5-157">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="339d5-157">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="339d5-158">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="339d5-158">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="339d5-159">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="339d5-159">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="339d5-160">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="339d5-160">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="339d5-161">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="339d5-161">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="339d5-162">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="339d5-162">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="339d5-163">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="339d5-163">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="339d5-164">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="339d5-164">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="339d5-165">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="339d5-165">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

