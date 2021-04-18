---
title: Proprietà ConnectedStatusText di IMsRdpClient2
description: Contiene il testo visualizzato nell'area client del controllo mentre il controllo è nello stato connesso.
ms.assetid: c3d8433b-2fb0-413d-88a3-667149f858ba
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà ConnectedStatusText
- Servizi Desktop remoto proprietà ConnectedStatusText, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà ConnectedStatusText
- Servizi Desktop remoto proprietà ConnectedStatusText, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà ConnectedStatusText
- Servizi Desktop remoto proprietà ConnectedStatusText, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà ConnectedStatusText
- Servizi Desktop remoto proprietà ConnectedStatusText, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà ConnectedStatusText
- Servizi Desktop remoto proprietà ConnectedStatusText, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà ConnectedStatusText
- Servizi Desktop remoto proprietà ConnectedStatusText, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà ConnectedStatusText
- Servizi Desktop remoto proprietà ConnectedStatusText, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà ConnectedStatusText
- Servizi Desktop remoto proprietà ConnectedStatusText, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà ConnectedStatusText
- Servizi Desktop remoto proprietà ConnectedStatusText, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, proprietà ConnectedStatusText
topic_type:
- apiref
api_name:
- IMsRdpClient2.ConnectedStatusText
- IMsRdpClient2.get_ConnectedStatusText
- IMsRdpClient2.put_ConnectedStatusText
- IMsRdpClient3.ConnectedStatusText
- IMsRdpClient3.get_ConnectedStatusText
- IMsRdpClient3.put_ConnectedStatusText
- IMsRdpClient4.ConnectedStatusText
- IMsRdpClient4.get_ConnectedStatusText
- IMsRdpClient4.put_ConnectedStatusText
- IMsRdpClient5.ConnectedStatusText
- IMsRdpClient5.get_ConnectedStatusText
- IMsRdpClient5.put_ConnectedStatusText
- IMsRdpClient6.ConnectedStatusText
- IMsRdpClient6.get_ConnectedStatusText
- IMsRdpClient6.put_ConnectedStatusText
- IMsRdpClient7.ConnectedStatusText
- IMsRdpClient7.get_ConnectedStatusText
- IMsRdpClient7.put_ConnectedStatusText
- IMsRdpClient8.ConnectedStatusText
- IMsRdpClient8.get_ConnectedStatusText
- IMsRdpClient8.put_ConnectedStatusText
- IMsRdpClient9.ConnectedStatusText
- IMsRdpClient9.get_ConnectedStatusText
- IMsRdpClient9.put_ConnectedStatusText
- IMsRdpClient10.ConnectedStatusText
- IMsRdpClient10.get_ConnectedStatusText
- IMsRdpClient10.put_ConnectedStatusText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd6ee2ac155aa3fc4873ee1a5eb890774b50978
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301227"
---
# <a name="imsrdpclient2connectedstatustext-property"></a><span data-ttu-id="cebf8-122">Proprietà IMsRdpClient2:: ConnectedStatusText</span><span class="sxs-lookup"><span data-stu-id="cebf8-122">IMsRdpClient2::ConnectedStatusText property</span></span>

<span data-ttu-id="cebf8-123">Contiene il testo visualizzato nell'area client del controllo mentre il controllo è nello stato connesso.</span><span class="sxs-lookup"><span data-stu-id="cebf8-123">Contains the text that is displayed in the client area of the control while the control is in the connected state.</span></span>

<span data-ttu-id="cebf8-124">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="cebf8-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cebf8-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cebf8-125">Syntax</span></span>


```C++
HRESULT put_ConnectedStatusText(
  [in]  BSTR newVal
);

HRESULT get_ConnectedStatusText(
  [out] BSTR *pConnectedStatusText
);
```



## <a name="property-value"></a><span data-ttu-id="cebf8-126">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="cebf8-126">Property value</span></span>

<span data-ttu-id="cebf8-127">La proprietà **ConnectedStatusText** contiene il testo visualizzato nell'area client del controllo mentre il controllo è nello stato connesso.</span><span class="sxs-lookup"><span data-stu-id="cebf8-127">The **ConnectedStatusText** property contains the text that is displayed in the client area of the control while the control is in the connected state.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cebf8-128">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="cebf8-128">Error codes</span></span>

<span data-ttu-id="cebf8-129">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="cebf8-129">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="cebf8-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="cebf8-130">Remarks</span></span>

<span data-ttu-id="cebf8-131">Testo da visualizzare nell'area client del controllo mentre il controllo è nello stato connesso.</span><span class="sxs-lookup"><span data-stu-id="cebf8-131">Text to display in the client area of the control while the control is in the connected state.</span></span> <span data-ttu-id="cebf8-132">Si tratta del testo visibile, ad esempio quando l'utente passa il controllo alla modalità schermo intero in un Web browser, uno scenario che lascia una parte del controllo ospitata nel browser.</span><span class="sxs-lookup"><span data-stu-id="cebf8-132">This is the text that is visible, for example, when the user switches the control to the full-screen mode in a web browser, a scenario that leaves a portion of the control hosted in the browser.</span></span>

<span data-ttu-id="cebf8-133">Il metodo **get \_ ConnectedStatusText** alloca la memoria necessaria per il buffer a cui punta il parametro *pConnectedStatusText* .</span><span class="sxs-lookup"><span data-stu-id="cebf8-133">The **get\_ConnectedStatusText** method allocates the memory required for the buffer pointed to by the *pConnectedStatusText* parameter.</span></span> <span data-ttu-id="cebf8-134">La chiamata di applicazioni C/C++ deve liberare la memoria con una chiamata alla funzione [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="cebf8-134">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="cebf8-135">Questa operazione non è necessaria per Visual Basic e client di scripting.</span><span class="sxs-lookup"><span data-stu-id="cebf8-135">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="cebf8-136">Impossibile impostare questa proprietà quando il controllo è connesso.</span><span class="sxs-lookup"><span data-stu-id="cebf8-136">This property cannot be set when the control is connected.</span></span> <span data-ttu-id="cebf8-137">È possibile verificare se il controllo è connesso chiamando il metodo [**IMsTscAx:: Get \_ Connected**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="cebf8-137">You can check if the control is connected by calling the [**IMsTscAx::get\_Connected**](imstscax-connected.md) method.</span></span>

<span data-ttu-id="cebf8-138">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="cebf8-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cebf8-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cebf8-139">Requirements</span></span>



| <span data-ttu-id="cebf8-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="cebf8-140">Requirement</span></span> | <span data-ttu-id="cebf8-141">Valore</span><span class="sxs-lookup"><span data-stu-id="cebf8-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cebf8-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cebf8-142">Minimum supported client</span></span><br/> | <span data-ttu-id="cebf8-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cebf8-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="cebf8-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cebf8-144">Minimum supported server</span></span><br/> | <span data-ttu-id="cebf8-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cebf8-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="cebf8-146">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="cebf8-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="cebf8-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cebf8-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="cebf8-148">DLL</span><span class="sxs-lookup"><span data-stu-id="cebf8-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cebf8-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cebf8-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="cebf8-150">IID</span><span class="sxs-lookup"><span data-stu-id="cebf8-150">IID</span></span><br/>                      | <span data-ttu-id="cebf8-151">IID \_ IMsRdpClient2 è definito come e7e17dc4-3b71-4ba7-A8E6-281ffadca28f</span><span class="sxs-lookup"><span data-stu-id="cebf8-151">IID\_IMsRdpClient2 is defined as e7e17dc4-3b71-4ba7-a8e6-281ffadca28f</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="cebf8-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cebf8-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cebf8-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="cebf8-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="cebf8-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="cebf8-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="cebf8-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="cebf8-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="cebf8-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="cebf8-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="cebf8-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="cebf8-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="cebf8-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="cebf8-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="cebf8-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="cebf8-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="cebf8-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="cebf8-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="cebf8-161">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="cebf8-161">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

